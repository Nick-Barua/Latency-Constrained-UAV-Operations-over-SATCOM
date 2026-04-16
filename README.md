# Latency-Constrained UAV Operations over SATCOM

## 📌 Overview
This repository provides supporting materials for the research study:

**“Latency-Constrained UAV Operations over SATCOM: A System-Level Analytical Framework”** **Nick Barua (2026)**

This work presents a system-level framework for analyzing and mitigating communication latency in satellite-enabled unmanned aerial vehicle (UAV) operations. The study transitions from descriptive analysis to a quantitative, latency-aware modeling approach, with direct implications for Beyond Visual Line of Sight (BVLOS) safety and autonomy.

---

## 🎨 Graphical Abstract
![Graphical Abstract](docs/images/Latency-Constrained%20UAV%20Operations%20over%20SATCOM%20-GA.png)

---

## 🖼️ Figure Gallery

### Figure 1: SATCOM Communication Loop Decomposition
![Figure 1](docs/images/Latency-Constrained%20UAV%20Operations%20Fig-1.png)

### Figure 2: Normalized Control Effectiveness vs. Latency
![Figure 2](docs/images/Latency-Constrained%20UAV%20Operations%20Fig-2.png)

### Figure 3: Mission Envelope Map (Safety Zones)
![Figure 3](docs/images/Latency-ConstrainedUAVOperationsFig-3.png)

### Figure 4: AACF State Transition Logic
![Figure 4](docs/images/Latency-ConstrainedUAVOperationsFig-4.png)

---

## 📐 Mathematical Framework

The total deterministic communication latency is defined as:

$$T_{total} = T_{uplink} + T_{satellite} + T_{downlink} + T_{processing}$$

For LEO systems, the model incorporates stochastic jitter ($\mathcal{J}$) to define the total reaction time:

$$T_{reaction} = (T_{total} + \mathcal{J}) + T_{human}$$

---

## 🖼️ Figure Gallery

### Figure 1: SATCOM Communication Loop Decomposition
![Figure 1](docs/images/Latency-Constrained%20UAV%20Operations%20Fig-1.png)

### Figure 2: Normalized Control Effectiveness vs. Latency
![Figure 2](docs/images/Latency-Constrained%20UAV%20Operations%20Fig-2.png)

### Figure 3: Mission Envelope Map (Safety Zones)
![Figure 3](docs/images/Latency-ConstrainedUAVOperationsFig-3.png)

### Figure 4: AACF State Transition Logic
![Figure 4](docs/images/Latency-ConstrainedUAVOperationsFig-4.png)

---

## 📊 Data Description

The following representative latency ranges are used to parameterize the analytical models:

| Mode | Uplink (ms) | Downlink (ms) | Total Latency (ms) |
| :--- | :--- | :--- | :--- |
| **5G** | 5–10 | 5–10 | 10–20 |
| **LEO SATCOM** | 10–50 | 15–90 | 25–140 |
| **GEO SATCOM** | 250–350 | 290–400 | 540–750 |

---

## 📂 Repository Structure

* **`src/`**: Core implementation scripts for latency models and AACF logic.
* **`data/`**: Standardized parameter sets for various mission scenarios.
* **`docs/images/`**: High-resolution figures and graphical assets.
* **`figures/`**: Python scripts for generating manuscript visuals.

---

## ⚙️ Usage

### Prerequisites
Ensure you have Python 3.8+ and the following libraries installed:
```bash
pip install matplotlib numpy scipy
