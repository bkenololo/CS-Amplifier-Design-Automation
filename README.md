# CS-Amplifier-Design-Automation
A high-precision, reproducible design framework for a Common-Source MOSFET Amplifier with Partial Source Degeneration, featuring automated E24 component selection and DC bias stability analysis.

# High-Precision Common-Source Amplifier Design

This repository contains a **reproducible design framework** for a Common-Source (CS) MOSFET Amplifier using the **VN2222LL** N-channel MOSFET. 

The project focuses on achieving strict analog specifications through automated computational design, bypassing traditional manual rounding errors by utilizing 64-bit floating-point precision.

## 🚀 Key Features
* **Reverse-Flow Design:** Calculations prioritize Output Resistance ($R_{out}$) and Gain ($A_v$) targets to derive optimal component values.
* **E24 Standardization:** Integrated logic to automatically map exact theoretical values to the closest standard E24 resistor series.
* **DC Bias Stability Analysis:** Automated solver for the quadratic $I_D$ equation to verify the "Auto-Correction" (Negative Feedback) capabilities of the source degeneration network.
* **Error Validation:** Real-time calculation of percentage errors between theoretical targets and E24-based physical reality.

## 📈 Design Targets
| Parameter | Specification |
| :--- | :--- |
| **Topology** | Common-Source with Partial Degeneration |
| **Voltage Gain ($A_v$)** | 10 V/V (20 dB) |
| **Input Resistance ($R_{in}$)** | 27 kΩ |
| **Output Resistance ($R_{out}$)** | 1.5 kΩ |
| **Supply Voltage ($V_{DD}$)** | 12.0 V |

## 🛠️ Usage
1. Open `Amplifier_Design.ipynb` in Jupyter Notebook or Google Colab.
2. Update the **Silicon Parameters** ($V_{th}$, $K_n$, $\lambda$) in the first cell based on your lab measurements.
3. Run all cells to generate the complete design table, including component values and stability tests.

## 📚 Technical Background
The design utilizes **Partial Source Degeneration**. This topology splits the source resistance into $R_{S1}$ (unbypassed for AC gain stability) and $R_{S2}$ (bypassed for DC biasing), allowing for independent control over transconductance linearization and maximum output swing.

---
*Developed as part of the EL2205 Electronics course at Bandung Institute of Technology (ITB).*
