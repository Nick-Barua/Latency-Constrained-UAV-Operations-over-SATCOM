# Latency-Constrained UAV Operations over SATCOM

## Overview
This repository provides supporting materials for the research study:

**“Latency-Constrained UAV Operations over SATCOM”**  
Nick Barua (2026)

The work presents a system-level framework for analyzing and mitigating communication latency in satellite-enabled unmanned aerial vehicle (UAV) operations. The study transitions from descriptive analysis to a quantitative, latency-aware modeling approach, with direct implications for Beyond Visual Line of Sight (BVLOS) safety and autonomy.

---

## Research Contribution

This repository accompanies a manuscript that introduces the following key contributions:

- **Deterministic Latency Decomposition**  
  Formal breakdown of end-to-end communication delay into operational components.

- **Stochastic Jitter Modeling (𝒥)**  
  Representation of latency variability in Low Earth Orbit (LEO) SATCOM environments.

- **Risk-Aware Formulation**  
  Probabilistic modeling of latency-induced control degradation and threshold breach risk.

- **Adaptive Autonomy Control Framework (AACF)**  
  A control strategy that dynamically adapts UAV autonomy levels based on latency conditions.

- **System-Level Integration**  
  Alignment with real-world UAV communication architectures and regulatory considerations.

---

## Mathematical Framework

The total communication latency is defined as:

\[
T_{total} = T_{uplink} + T_{satellite} + T_{downlink} + T_{processing}
\]

Where:

- \(T_{uplink}\): Ground-to-satellite transmission delay  
- \(T_{satellite}\): Satellite transponder processing delay  
- \(T_{downlink}\): Satellite-to-UAV transmission delay  
- \(T_{processing}\): Ground system processing and routing delay  

For LEO systems, the model incorporates stochastic jitter:

\[
T_{reaction} = (T_{total} + \mathcal{J}) + T_{human}
\]

This formulation enables evaluation of latency-induced performance degradation and safety risk.

---

## Repository Structure
