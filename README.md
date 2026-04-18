# Automated Design & Verification of a Common-Source Amplifier

This repository contains a high-precision design and automated verification framework for a Common-Source Amplifier using the VN2222LL MOSFET. The project bridges theoretical circuit synthesis with industrial-grade simulation practices using Python and LTspice.

## Key Features
- **High-Precision Synthesis:** Component derivation using 64-bit floating-point precision to minimize numerical drift.
- **Automated SPICE Pipeline:** Integration of `PyLTSpice` for headless simulation execution and data extraction.
- **Multi-Phase Verification:** Six-stage testing suite covering DC Bias, Transient Response, Spectral Analysis (Bode), Impedance Verification, and Device Characterization.
- **Real-World Modeling:** Quantitative analysis of Gain degradation caused by output loading and resistive parasitics (ESR & Trace Resistance).

## Design Specifications
| Parameter | Target Value |
|-----------|--------------|
| Topology  | Common-Source (Source Degenerated) |
| Voltage Gain ($A_v$) | 10 V/V (20 dB) |
| Input Resistance ($R_{in}$) | 27 kΩ |
| Output Resistance ($R_{out}$) | 1.5 kΩ |
| Supply Voltage ($V_{DD}$) | 12.0 V |

## Project Structure
- `CS_Amplifier_Automated_Verification.ipynb`: The primary computational engine and documentation.
- `schematic.asc`: The LTspice source file used for automated simulations.
- `exports/`: Generated plots (Bode, Transient, IV Curves, and Parasitic Analysis).

## Methodology
The workflow follows a **Progressive Verification Plan**, starting from an idealized Baseline characterization to a non-ideal system model that accounts for PCB-level parasitic effects.

---
*Developed as part of the EL2205 Major Assignment - Electrical Engineering, Bandung Institute of Technology (ITB).*