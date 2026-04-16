# Latency-Constrained UAV Operations over SATCOM

## 📌 Overview
This repository provides supporting materials for the research study:

**“Latency-Constrained UAV Operations over SATCOM: A System-Level Analytical Framework”** **Nick Barua (2026)**

This work presents a system-level framework for analyzing and mitigating communication latency in satellite-enabled unmanned aerial vehicle (UAV) operations. The study transitions from descriptive analysis to a quantitative, latency-aware modeling approach, with direct implications for Beyond Visual Line of Sight (BVLOS) safety and autonomy.

---

## 🚀 Research Contributions

This repository accompanies a manuscript that introduces the following key contributions:

* **Deterministic Latency Decomposition**: A formal breakdown of end-to-end communication delay into operational components.
* **Stochastic Jitter Modeling ($\mathcal{J}$)**: Representation of latency variability in Low Earth Orbit (LEO) SATCOM environments arising from orbital handovers.
* **Risk-Aware Formulation**: Probabilistic modeling of latency-induced control degradation and the Probability of Safety Breach ($P_{breach}$) metric.
* **Adaptive Autonomy Control Framework (AACF)**: A dynamic control strategy that adjusts UAV autonomy levels and velocity based on real-time latency conditions.

---

## 📐 Mathematical Framework

The total deterministic communication latency is defined as:

$$T_{total} = T_{uplink} + T_{satellite} + T_{downlink} + T_{processing}$$

For LEO systems, the model incorporates stochastic jitter ($\mathcal{J}$) to define the total reaction time:

$$T_{reaction} = (T_{total} + \mathcal{J}) + T_{human}$$

This formulation allows for the calculation of $P_{breach}$, representing the risk that stochastic delays exceed safe operational margins.

---

## 📊 Data Description

The following representative latency ranges are used to parameterize the analytical models and generate comparative results:

| Mode | Uplink (ms) | Downlink (ms) | Total Latency (ms) |
| :--- | :--- | :--- | :--- |
| **5G** | 5–10 | 5–10 | 10–20 |
| **LEO SATCOM** | 10–50 | 15–90 | 25–140 |
| **GEO SATCOM** | 250–350 | 290–400 | 540–750 |

---

## 📂 Repository Structure

* **`src/`**: Core implementation scripts.
    * `latency_models.py`: Implementation of deterministic and stochastic equations.
    * `aacf_engine.py`: Logic for the dynamic velocity arbitrator and state transitions.
* **`data/`**: Standardized parameter sets for Urban, Inspection, and Disaster Response scenarios.
* **`docs/`**: Supplemental documentation, including high-resolution visuals.
* **`figures/`**: Python scripts for generating manuscript visuals.

---

## ⚙️ Usage

### Prerequisites
Ensure you have Python 3.8+ and the following libraries installed:
```bash
pip install matplotlib numpy scipy
