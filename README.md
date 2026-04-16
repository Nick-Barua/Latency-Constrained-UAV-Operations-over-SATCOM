# Latency-Constrained UAV Operations over SATCOM

## 📌 Overview
This repository provides supporting materials for the research study:

**“Latency-Constrained UAV Operations over SATCOM: A System-Level Analytical Framework”** **Nick Barua (2026)**

This work presents a system-level framework for analyzing and mitigating communication latency in satellite-enabled unmanned aerial vehicle (UAV) operations. The study transitions from descriptive analysis to a quantitative, latency-aware modeling approach, with direct implications for Beyond Visual Line of Sight (BVLOS) safety and autonomy.

---

## 🚀 Research Contributions

This repository accompanies a manuscript that introduces the following key contributions:

* [cite_start]**Deterministic Latency Decomposition**: Formal breakdown of end-to-end communication delay into operational components[cite: 10, 67].
* [cite_start]**Stochastic Jitter Modeling ($\mathcal{J}$)**: Representation of latency variability in Low Earth Orbit (LEO) SATCOM environments[cite: 11, 88].
* [cite_start]**Risk-Aware Formulation**: Probabilistic modeling of latency-induced control degradation and threshold breach risk ($P_{breach}$) [cite: 96-97].
* [cite_start]**Adaptive Autonomy Control Framework (AACF)**: A control strategy that dynamically adapts UAV autonomy levels based on real-time latency conditions[cite: 12, 145].
* [cite_start]**System-Level Integration**: Alignment with real-world UAV communication architectures and regulatory considerations[cite: 13, 192].

---

## 📐 Mathematical Framework

The total communication latency is defined as:

$$T_{total} = T_{uplink} + T_{satellite} + T_{downlink} + T_{processing}$$

Where:
* [cite_start]$T_{uplink}$: Ground-to-satellite transmission delay[cite: 69].
* [cite_start]$T_{satellite}$: Satellite transponder processing delay[cite: 69].
* [cite_start]$T_{downlink}$: Satellite-to-UAV transmission delay[cite: 71].
* [cite_start]$T_{processing}$: Ground system processing and routing delay[cite: 70].

For LEO systems, the model incorporates stochastic jitter ($\mathcal{J}$):

$$T_{reaction} = (T_{total} + \mathcal{J}) + T_{human}$$

[cite_start]This formulation enables the evaluation of latency-induced performance degradation and safety risk [cite: 91-93].

---

## 📂 Repository Structure

This repository is organized to support **Computational Reproducibility**. All analytical models and data parameters presented in the manuscript are implemented as follows:

* **`src/`**: Core implementation and analytical scripts.
    * `latency_models.py`: Implementation of the deterministic $T_{total}$ decomposition and the stochastic $T_{reaction}$ jitter model.
    * `aacf_engine.py`: Logic for the **Adaptive Autonomy Control Framework (AACF)** and the dynamic velocity arbitrator (Equation 9).
    * `plot_figures.py`: Automated generation of the mission envelope maps and control effectiveness curves.
* **`data/`**: Standardized parameter sets used for mission scenario analysis.
    * `comm_parameters.json`: Comprehensive latency and jitter values for 5G, LEO, and GEO communication modes.
    * `mission_scenarios.csv`: Velocity and safety distance parameters for Urban, Inspection, and Disaster Response scenarios.
* **`docs/`**: Supplemental documentation and high-resolution visual assets.
    * `graphical_abstract.png`: The end-to-end logic pipeline of the research framework.
    * `validation_protocol.md`: Detailed experimental roadmap and **Flight Performance Indicator (FPI)** definitions.
* **`requirements.txt`**: Minimalist dependency list (NumPy, SciPy, Matplotlib) to ensure environment parity.
* **`LICENSE`**: MIT License, ensuring transparency for academic and commercial research integration.

---

## ⚖️ License
Distributed under the MIT License. See `LICENSE` for more information.

## ✉️ Contact
**Nick Barua** – [s.nick.barua@gmail.com](mailto:s.nick.barua@gmail.com)  
*Chairman & CEO, AN Holdings Co.* *Visiting Professor, Shiga University of Medical Science; Kobe Gakuin University*
