# Pitch Playbook: Selling Computer Vision (CV) in Manufacturing

This guide outlines how to apply psychological and conversational sales triggers specifically for selling Computer Vision (CV) solutions (such as automated defect detection, PPE monitoring, and predictive visual analytics) to plant managers, operations directors, and QC heads who are naturally risk-averse and skeptical of "AI hype."

---

## 1. The Manufacturing Buyer Persona
Manufacturing decision-makers are characterized by:
- **Extreme Risk Aversion**: A single hour of assembly line downtime can cost tens of thousands of dollars.
- **Skepticism of AI jargon**: They care about reliability, repeatability (Six Sigma), and plant-floor practicality over neural network architectures.
- **Fear of Disruption**: They worry that installing cameras or software will disrupt production schedules or require months of worker retraining.

By understanding these bottlenecks, you can deploy the core principles from [[Psychological and Conversational Triggers That Increase a Prospect's Likelihood to Buy]] to bypass their defenses.

---

## 2. Core Psychological Triggers for CV Solutions

### 🧠 Trigger 1: Authority (Diagnostic Expertise over Technical Hype)
Plant managers do not care about "deep learning" or "YOLOv8." They care about precision, recall, and false-positive rates. Present yourself as an industrial engineer first and a software vendor second.

*   **How to apply it:**
    *   Do not pitch "AI." Pitch **Automated QC Inspection** or **Visual Safety Compliance**.
    *   Show deep understanding of their metrics: cycle times, scrap rates, PPM (Parts Per Million) defect levels, and false alarms.
    *   **Pattern Recognition Phrase:** *"In most metal stamping lines, we see manual inspection miss up to 15% of micro-cracks because of inspector fatigue at the end of an 8-hour shift. Is that aligned with what you see on Line 2?"*

### 🧠 Trigger 2: Reciprocity (The Zero-Impact Visual Audit)
Manufacturing buyers want to see the technology work on *their* parts, not on clean demo datasets. Give them a "small win" before asking for budget.

*   **How to apply it:**
    *   **The Diagnostic Offer:** Offer to perform a free "Visual Inspection Audit." 
    *   Ask them to send you 20-30 sample images or a 10-minute video feed of their typical "good" and "defective" parts.
    *   Run their files through your pre-trained models and present a **Model Performance Report** showing exactly which defects your system caught that manual inspectors might miss.
    *   By delivering this value upfront, you trigger reciprocity and prove the solution's viability risk-free.

### 🧠 Trigger 3: Problem Agitation (The Cost of the "Escaped Defect")
A plant manager's greatest fear is an "escaped defect"—a defective part that slips past quality control and reaches the customer (e.g., an OEM auto manufacturer). This causes warranty claims, penalties, and lost contracts.

*   **How to apply it:**
    *   Do not just discuss "efficiency." Agitate the consequences of QC failure.
    *   **Reflective Agitation Question:** *"If a component with a hairline fracture slips past QC and gets integrated into the final assembly at your client's plant, what is the protocol? What are the financial and reputational costs of that recall?"*
    *   Help them calculate the **Cost of Inaction**: `Cost of escapes (fines/rework) + Cost of manual inspection labor vs. Cost of CV automation`.

### 🧠 Trigger 4: Commitment & Consistency (The Single-Station Pilot)
A major roadblock is the fear of a complex, expensive, plant-wide IT overhaul. Break down the purchase decision into a sequence of small, low-risk agreements.

*   **How to apply it:**
    *   **The Upfront Agreement:** *"We don't expect you to roll this out across the whole plant today. Let's start by addressing your highest-scrap station."*
    *   Propose a **2-Week Single-Camera Pilot**. 
    *   **Low Friction Promise:** The pilot requires zero integration with their core MES (Manufacturing Execution System) or ERP. It simply runs on a single edge device next to the conveyor belt, logging defects to a local dashboard.
    *   Once they agree to this small, low-cost step and see it work, their psychological desire for consistency will make the full rollout a natural next step.

### 🧠 Trigger 5: Social Proof (Industry Benchmarks)
Manufacturing is a "fast-follower" industry. Nobody wants to be the first to test a technology, but nobody wants to be left behind their competitors.

*   **How to apply it:**
    *   Use case studies focused on concrete operational metrics, not tech milestones.
    *   **Framing:** *"We deployed a similar defect detection model for a tier-1 automotive supplier. They reduced their defect escape rate to zero and cut inspection cycle time by 42% within 30 days."*

---

## 3. Conversational Playbook: Opening to Close

### Phase 1: Lowering Defensiveness (The Two-Way Fit)
Start the meeting by neutralizing the pressure. Acknowledge that CV might not be suitable for every plant line.

> **Script:** 
> *"Thanks for having me. The goal today isn't to push a system on you. CV works incredibly well for high-speed, repeatable visual inspections, but if your production lines change configurations every hour or your lighting varies dramatically, it might not be a fit. Let's use today to figure out if your lines actually match our capabilities, and if not, we can part ways. Fair enough?"*

### Phase 2: Diagnostic Questions (Interaction over Interrogation)
Avoid asking yes/no questions about their tech stack. Use questions that reveal process friction.

*   *Instead of:* "Do you have quality control issues?"
*   *Ask:* **"When a defect occurs on the line, how far down the process does it typically travel before it is detected? What is the scrap cost at that point compared to catching it at the source?"**
*   *Instead of:* "Do you want to automate inspection?"
*   *Ask:* **"How do you currently manage inspector fatigue on high-speed lines, especially during night shifts? How does your defect rate change between Shift 1 and Shift 3?"**

### Phase 3: Decision Simplicity (The 3-Step Implementation Path)
To eliminate their fear of complex integration, lay out a dead-simple onboarding path.

1.  **Mount Camera**: We position a single industrial camera (or tap your existing CCTV feed) over the target line station.
2.  **Calibrate Model**: We feed 1 day of line data to calibrate the detection thresholds for your specific lighting and defect types.
3.  **Alert & Act**: The system sends a real-time signal (a light tower trigger, a PLC pulse, or a dashboard alert) to flag defective parts instantly.

---

## 4. Prep Checklist for Your Next Pitch
Use this template to prepare before stepping into the meeting room:

- [ ] **Research the Line Types**: What do they manufacture? (e.g., plastic injection molding, sheet metal, electronics). Identify the 3 most common defect types for this manufacturing process.
- [ ] **Define the Reciprocity Offer**: Prepare your proposal for the "Zero-Impact Visual Audit" (e.g., *"If you send us photos of 15 defective parts, we'll return a model detection breakdown within 48 hours"*).
- [ ] **Prepare the "Escape Defect" Question**: Tailor your agitation question to their target customer. (e.g., if they supply to automotive: *"What is your current OEM penalty for a batch return?"*).
- [ ] **De-risk the Hardware**: Have a clear response ready for: *"How do your cameras handle dust, grease, and vibrating environments?"* (Explain IP67 enclosures and optical filters).

---

*Related Checklists:*
- [[Sales Engagement Checklist Template]]
- [[Psychological and Conversational Triggers That Increase a Prospect's Likelihood to Buy]]
