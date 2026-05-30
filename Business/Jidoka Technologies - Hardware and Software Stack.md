---
type: Sales-Resource
status: Active
tags: [sales, technical-stack, software-architecture, hardware-design, computer-vision, AI, MERN]
Date: 2026-05-28
---

# Technical Stack Analysis: Jidoka Technologies

## Executive Summary
Jidoka Technologies utilizes a hybrid hardware-software architecture optimized for high-speed edge computing. By coupling deep learning frameworks (**TensorFlow/NVIDIA CUDA**) with robust local messaging systems (**ZeroMQ/C++**) and containerized deployment (**Docker**), they ship localized visual inspection systems to factory floors. 

This document details their software codebase layers, MLOps, edge compute processing, optical hardware, and PLC integration methods.

---

## 1. The Software & Development Stack (Per Product)

### A. AI & Model Layer (KOMPASS™ & NAGARE™)
*   **Programming Language:** Python.
*   **Deep Learning Frameworks:** **TensorFlow** (primary framework for training convolutional neural networks (CNNs) and deep vision models).
*   **Hardware Acceleration:** **NVIDIA CUDA** and cuDNN (enables rapid parallel GPU computing, essential for keeping model inference times below 10-15 milliseconds per part).

### B. Communication & System Integration Layer
*   **Languages:** **C++** (used for high-performance camera frame grabbing, memory buffer management, and physical PLC input/output commands).
*   **Inter-Process Communication (IPC):** **ZeroMQ (ZMQ)**. This acts as the high-throughput, low-latency messaging queue connecting:
    *   The C++ camera driver layer (capturing images).
    *   The Python AI layer (running inference on captured frames).
    *   The Node.js backend (receiving OK/NOK status and sending commands to PLC reject gates).

### C. Operator Interface & Management Layer (The GUI)
*   **The MERN Stack:**
    *   *Frontend:* **React.js** (provides the local plant operator interface for displaying real-time OK/NOK flags, error logs, and defect labeling tools).
    *   *Backend:* **Node.js** and **Express.js** (manages configuration parameters, database queries, and runs the local API).
    *   *Database:* **MongoDB** (stores local inspection logs, defect classifications, and system performance metrics).

### D. Packaging & Shipping Architecture (MLOps & DevOps)
*   **Operating System:** Ubuntu Linux (flashed on all industrial edge computer nodes).
*   **Containerization:** **Docker**. Jidoka ships its platforms containerized. This allows them to package the KOMPASS software, trained model files, ZeroMQ queues, and MERN GUI into discrete containers that deploy onto edge hardware without environment conflicts.
*   **SKU Management:** Custom in-house MLOps tools to manage, version, and load different product SKU model files to the edge when lines switch products.

---

## 2. The Hardware & Optics Stack (Per Rig)

Jidoka's modular vision hardware (MVH) is designed to create a controlled optical environment (eliminating ambient factory light shifts):

### A. Edge Computing & Processing Units
*   **Industrial PCs (IPCs):** Fanless, ruggedized edge computers built to withstand heat, dust, and vibration.
*   **GPU Modules:** Dedicated NVIDIA GPUs (such as NVIDIA Jetson edge modules for low-power stations, or discrete NVIDIA RTX series cards for heavy multi-camera setups) to drive CUDA acceleration.

### B. Optical & Sensor Hardware
*   **Industrial Cameras:** GigE Vision and USB3 Vision area scan and line scan cameras (supporting high frame rates and precise sensor sizes).
*   **Lenses:** Variable focal length and telecentric lenses (to eliminate perspective distortion on high-precision dimensional measurements).
*   **Industrial Lighting:** Custom-controlled LED arrays (dome lights for reflective metals, ring lights for surface scratch detection, and coaxial lighting).

### C. Mechanical Enclosures & Motion Platforms
*   **Huron (Rotary Table System):** Uses mechanical rotary index tables to spin cylindrical components, allowing cameras to capture a 360° profile.
*   **Tigris (Dual Conveyor & Flipper):** Implements twin conveyor belts with an integrated mechanical flipping unit, enabling dual-sided top/bottom inspection.
*   **Miyake (Manual Station):** A stationary light box enclosure with discrete inputs (push-buttons) for manual part placement.

---

## 3. Industrial PLC Integration (How it connects to the Line)

*   **PLC Brands:** Siemens, Allen-Bradley, Mitsubishi.
*   **Connection Method:** Standard industrial communication protocols (EtherNet/IP, PROFINET, Modbus TCP) or direct discrete digital I/O.
*   **The Loop:**
    1.  The product passes a physical photoelectric sensor on the conveyor.
    2.  The sensor triggers the PLC.
    3.  The PLC sends a trigger signal to Jidoka's C++ camera driver.
    4.  The camera captures the frame, ZeroMQ passes it to the Python TensorFlow model, and the model classifies it.
    5.  If categorized as "NOK" (Defect), the Node.js backend sends a command to the PLC.
    6.  The PLC activates a pneumatic reject arm to push the defective part off the line.
