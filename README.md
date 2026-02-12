# 60 GHz Frequency Selective Surface (FSS) Design and Analysis

This repository contains the design, simulation, and electromagnetic analysis of a **Frequency Selective Surface (FSS)** operating at the 60 GHz (Millimeter Wave) frequency band. The project focuses on a ring resonator geometry, evaluated for its performance in radar radome and RCS (Radar Cross Section) management applications.

---

## 🛠 Technical Specifications

The design utilizes a high-frequency substrate and a gold-plated (PEC) ring resonator.

### 1. Substrate Properties (Arlon AD 300D)
- **Dielectric Constant ($\epsilon_r$):** 2.94
- **Loss Tangent ($tan\delta$):** 0.0021 @ 10 GHz
- **Thickness ($h$):** 0.1 mm
- **Thermal Conductivity:** 0.37 W/K/m

### 2. Geometry & Unit Cell Parameters
- **Unit Cell Size ($a$):** 2.0 mm x 2.0 mm
- **Outer Radius ($orad$):** 0.9 mm
- **Inner Radius ($irad$):** 0.7 mm
- **Metal Thickness ($Mt$):** 0.05 mm

---

## 📡 Simulation & Methodology

### Computation Strategy
- **Solver:** Frequency Domain Solver (F-Solver)
- **Boundary Conditions:** Unit Cell (Periodic) boundaries in XY planes.
- **Excitation:** Floquet ports for plane wave analysis.
- **Mesh Type:** Tetrahedral Mesh

### Computational Complexity & Optimization
To balance accuracy and hardware constraints, the following mesh configuration was used:
- **Total Tetrahedrons:** 115,637
- **Mesh Adaptation:** Adaptive Mesh Refinement (Pass 4 completed)
- **Hardware Optimization:** Resolved "Not enough memory" errors by optimizing mesh density and transitioning to a unit-cell based array factor calculation.

---

## 📊 Results & Observations

### 1. Radar Cross Section (RCS) Analysis
The simulation at 60 GHz reveals the following bistatic scattering metrics:
- **Maximum RCS:** -24.8 dB(m²)
- **Total ACS:** -63.92 dB(m²)
- **Total RCS:** -37.91 dB(m²)



### 2. Farfield Radiation Pattern
The 3D farfield plot confirms the scattering characteristics of the FSS array. The main lobe direction and angular width (32.4°) demonstrate the filtering and reflective capabilities of the surface.



