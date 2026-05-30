---
type: Sales-Resource
status: Active
tags: [sales, product-analysis, solutions, jidoka-technologies, computer-vision, AI, deep-learning]
Date: 2026-05-28
---

# Product & Solutions Analysis: Jidoka Technologies

## Executive Summary
Jidoka Technologies operates at the intersection of AI, computer vision, and industrial automation. Their product strategy centers on providing **"built-in quality"** by splitting quality assurance into two domains: **KOMPASS™** (cognitive product defect detection) and **NAGARE™** (operator process optimization). This software layer is coupled with custom physical hardware rigs (**Huron**, **Tigris**, **Miyake**) to deliver turnkey, high-throughput inline inspection.

This report evaluates Jidoka's product architecture, solution verticals, real-world client implementations, and strategic positioning.

---

## 1. Product Portfolio Deep-Dive

### A. KOMPASS™: Cognitive Product Inspection (Software)
KOMPASS is an AI-powered visual quality control platform designed to identify surface, dimensional, and cosmetic anomalies in real-time.
*   **Performance Metrics:** Processes up to **4,200 parts/minute (inferences)**, aligning with high-speed manufacturing lines without causing throughput delays.
*   **Key Capabilities:**
    *   *Real-time Edge Execution:* Deploys models locally to make sub-millisecond "OK/NOK" (Pass/Fail) sorting decisions.
    *   *Texture & Reflection Management:* Uses deep learning to analyze difficult surfaces (e.g., highly reflective polished metal automotive components, complex textures, or printed labeling).
    *   *Anomaly Detection:* Moves beyond traditional, rigid rule-based pixel-matching to identify unforeseen or organic defects.

### B. NAGARE™: Intelligent Process Optimization (Software)
NAGARE is a deep learning-based video analytics tool focused on operator compliance, process error-proofing, and logistics workflows.
*   **Performance Metrics:** Designed to run on pre-existing commodity CCTV/camera setups, reducing soft-deployment hardware costs.
*   **Key Capabilities:**
    *   *Real-Time SOP Compliance:* Monitors assembly lines to ensure manual operators follow precise sequences, flashing warnings if a step is skipped.
    *   *Poka-Yoke (Error Proofing):* Intercepts errors during packing, kitting, or assembly before the product moves down the line.
    *   *Warehouse Logistics Optimization:* Tracks material flow, pick-and-pack accuracy, and route compliance to minimize packing errors and cargo bottleneck times.

### C. Modular Vision Hardware (MVH)
To ensure optimal lighting, angle, and throughput, Jidoka bundles its software with pre-configured physical inspection rigs:
1.  **Huron:** A 360° high-speed rotational profiling unit designed for complex spherical or cylindrical parts (running up to 250 parts/minute).
2.  **Tigris:** Inline inspection units designed for conveyor belt operations (e.g., packaged foods, FMCG boxes).
3.  **Miyake:** Manual inspection stations where a human operator loads parts, and the AI system runs cognitive checks on demand.

---

## 2. Client Case Studies & Real-World Solutions

Jidoka has built a reference list of clients across key sectors:

### A. FMCG: Diageo (Beverages & Labeling)
*   **The Challenge:** High-speed bottle labeling often resulted in misaligned, torn, or bubbly label applications, damaging brand perception.
*   **Jidoka's Solution:** Integrated the **KOMPASS** software with **Tigris** conveyor hardware.
*   **Outcome:** Achieved **99%+ label inspection accuracy** in real-time under high line speeds, ensuring zero-defect packaging escapes.

### B. General Manufacturing: Hindustan Pencils (Stationery)
*   **The Challenge:** Inspecting wooden pencil slats for physical cracks, wood rot, or groove defects at extremely high speeds.
*   **Jidoka's Solution:** Configured high-speed cameras running KOMPASS to scan wood surfaces.
*   **Outcome:** Automated inspection to achieve **99% accuracy at 125 parts per minute**, reducing manual visual inspection fatigue.

### C. Automotive & Kitting: APA Engineering (Component Packaging)
*   **The Challenge:** Human packing errors during complex automotive kit assembly resulted in missing components, leading to customer complaints and returns.
*   **Jidoka's Solution:** Implemented **NAGARE** video analytics to watch the packing area.
*   **Outcome:** Eliminated kitting/packing errors (**zero-defect packing**) and increased overall assembly operator productivity by **35%**.

---

## 3. Product-Level Competitive Assessment

### Strategic Strengths
*   **Dual Product Focus (Product + Process):** Competing vision systems only inspect the finished product (KOMPASS-level). By adding NAGARE, Jidoka can upsell process compliance to the same manufacturing plant, preventing defects before they occur.
*   **Turnkey Comfort:** For traditional manufacturers lacking optical expertise, Jidoka's ability to supply the physical camera enclosure, lighting, and computing hardware simplifies purchasing.

### Strategic Weaknesses
*   **Edge Hardware Dependency:** Turnkey physical rigs (like Huron) restrict rapid global scaling. Every new deal requires mechanical engineering, shipping, and physical setup.
*   **Lack of No-Code Tools:** Unlike Lincode, Jidoka does not heavily promote a self-service, no-code model-building interface, meaning customers rely on Jidoka's engineering team to train and retrain AI models for new product SKUs.

---

## 4. Sales Enablement Strategy (How to Position Against Jidoka)

When selling against Jidoka's product portfolio, frame your offering around:
1.  **Agnostic Integration vs. Proprietary Hardware Locks:**
    *   *Pitch:* "Jidoka wants to sell you custom steel frames and proprietary rigs (like Huron). We use your existing standard cameras and line structures, keeping your capital expenditure low."
2.  **Self-Service SKU Training:**
    *   *Pitch:* "When your product lines change or you add new SKUs, Jidoka requires their engineers to retrain the models. Our no-code interface allows your plant floor team to train new models in hours without paying professional service fees."
3.  **Low-Latency Software vs. Physical Deployment Time:**
    *   *Pitch:* "Jidoka's deployment takes weeks or months due to physical shipping and custom fabrication. Our cloud-to-edge software can be deployed remotely on pre-existing lines in days."
