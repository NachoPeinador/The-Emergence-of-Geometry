# $\pi$ as the Optimal Phase in Modular Quantum Superselection

[![JPA](https://img.shields.io/badge/Paper-Read_PDF-B31B1B?style=flat&logo=latex&logoColor=white)](https://github.com/NachoPeinador/The-Emergence-of-Geometry/blob/main/Paper/π_as_the_Optimal_Phase_in_MQS.pdf)
[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.18703610.svg)](https://doi.org/10.5281/zenodo.18703610)
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NachoPeinador/The-Emergence-of-Geometry/blob/main/Notebooks/PYTHON_PRA_π_as_the_Optimal_Phase_in_MQS.ipynb)
[![Open Lean 4 Colab](https://img.shields.io/badge/Lean_4-Certified_0_Axioms-purple?style=flat&logo=lean)](https://colab.research.google.com/github/NachoPeinador/The-Emergence-of-Geometry/blob/main/Notebooks/LEAN_PRA_π_as_the_Optimal_Phase_in_MQS.ipynb)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
[![Python 3.9+](https://img.shields.io/badge/python-3.9+-blue.svg)](https://www.python.org/downloads/)
[![ORCID](https://img.shields.io/badge/ORCID-0009--0008--1822--3452-A6CE39?style=flat&logo=orcid&logoColor=white)](https://orcid.org/0009-0008-1822-3452)
[![X](https://img.shields.io/badge/X-%40todos__lumpen-000000?style=flat&logo=x&logoColor=white)](https://twitter.com/todos_lumpen)

> **"In discrete modular quantum substrates, phase $\pi$ is not merely a geometric constant; it is the optimal parity shield against decoherence under $\mathbb{Z}/6\mathbb{Z}$ superselection."**

This repository contains the complete replication package, formal proof scripts, and numerical simulation suite for the paper submitted to **Physical Review A**: *$\pi$ as the Optimal Phase in Modular Quantum Substrates*.

---

## 📄 Abstract

We identify the constant $\pi$ as the optimal relative phase for stabilizing chiral quantum channels under $\mathbb{Z}/6\mathbb{Z}$ superselection rules. Within a modular substrate governed by the quotient ring $\mathbb{Z}/6\mathbb{Z}$, we prove that the relative phase shift $\phi_2 = \pi$ uniquely maximizes the fidelity of the $\mathcal{C}_5$ chiral channel (residue class $5 \pmod 6$) relative to the $\mathcal{C}_1$ channel. 

This result follows from the exact $\mathbb{Z}_2$ symmetry of the unit group $(\mathbb{Z}/6\mathbb{Z})^\times \cong \mathbb{Z}_2$ and the elementary parity transformation of symmetric noise operators:

$$\sin(\theta + \pi) = -\sin(\theta)$$

Via high-precision master equation numerical simulations (Lindblad dynamics) and Qiskit circuit implementations, we demonstrate that chiral interference under this phase suppresses parity-symmetric Gaussian Unitary Ensemble (GUE) noise by **45.2%**, yielding a net signal-to-noise ratio (SNR) gain of **6.07 dB**. 

The entire algebraic core—including the optimal phase theorem and parity transformations—is formally certified in the **Lean 4 proof assistant with zero omitted axioms**.

<div align="center">
  <img src="Images/DSP_Polyphase_Filter.pdf" alt="Topological Shielding and Noise Collapse" width="100%">
</div>

<div align="center">
  <em><b>Figure 1:</b> Topological noise shielding via $\pi$-phase chiral interference and $M=6$ polyphase filtering. <b>(Top)</b> Raw unshielded register signal submerged in GUE noise. <b>(Bottom)</b> Reconstructed spectrum showing how constructive interference doubles peak amplitudes while symmetric noise undergoes destructive cancellation, yielding a +6.07 dB SNR gain.</em>
</div>

---

## 📐 Key Theoretical & Quantitative Results

<div align="center">

### 🎯 The Optimal Phase Core Relation
# $$\huge \boxed{ \phi_2 = \pi \implies \max_{\phi} \mathcal{F}\left(\mathcal{C}_5(\phi), \mathcal{C}_1\right) }$$

</div>

| Metric / Parameter | Value / Finding | Verification Method |
| :--- | :--- | :--- |
| **Algebraic Substrate** | $\mathbb{Z}/6\mathbb{Z}$ Quotient Ring | Formalized in Lean 4 |
| **Unit Group Symmetry** | $(\mathbb{Z}/6\mathbb{Z})^\times \cong \mathbb{Z}_2$ | Formalized in Lean 4 |
| **Optimal Relative Phase** | $\phi_2 = \pi$ | Analytical Proof + Qiskit |
| **GUE Noise Reduction** | **$-45.2\%$** | Lindblad Master Equation (`mpmath` / `scipy`) |
| **Net SNR Gain** | **$+6.07\text{ dB}$** | DSP Polyphase Filter Analysis |
| **Formal Mechanization** | **0 Omitted Axioms** (`sorry`-free) | Lean 4 / Mathlib Kernel |

---

## 🔬 Formal Verification & Simulation Architecture

The repository combines rigorous interactive theorem proving with numerical quantum dynamics:

### 1. Formal Proofs (Lean 4)
* Mechanized proofs certifying that the multiplicative group of units $(\mathbb{Z}/6\mathbb{Z})^\times$ induces an exact $\mathbb{Z}_2$ involution.
* Rigorous derivation showing that parity-symmetric noise operators cancel constructively under $\pi$-phase shifts without relying on external unproven axioms.

### 2. Quantum Master Equation Simulations (Python)
* Integration of Lindblad open quantum systems subjected to Gaussian Unitary Ensemble (GUE) environmental noise.
* High-precision evaluation of channel fidelity trajectories $\mathcal{F}(t)$ using standard numerical precision and arbitrary-precision floating-point arithmetic (`mpmath`).

---

## 🛠️ Scientific Reproducibility & Executable Validation

You can audit the complete replication package in three ways:

### Interactive Browser Audit (Google Colab)
Run the master quantum simulation notebook directly in your browser:
[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/NachoPeinador/The-Emergence-of-Geometry/blob/main/Notebooks/PYTHON_PRA_π_as_the_Optimal_Phase_in_MQS.ipynb)
[![Open Lean 4 Colab](https://img.shields.io/badge/Lean_4-Certified_0_Axioms-purple?style=flat&logo=lean)](https://colab.research.google.com/github/NachoPeinador/The-Emergence-of-Geometry/blob/main/Notebooks/LEAN_PRA_π_as_the_Optimal_Phase_in_MQS.ipynb)

---

## 📜 License

* **Code & Formal Proofs:** [MIT License](https://www.google.com/search?q=LICENSE)
* **Manuscript & Dataset:** [Creative Commons Attribution 4.0 International (CC-BY 4.0)](https://creativecommons.org/licenses/by/4.0/)

---

## 📚 Citation

If this work or codebase contributes to your research, please cite it as follows:

```bibtex
@article{peinador2026pi_optimal_phase,
  title={$\pi$ as the Optimal Phase in Modular Quantum Superselection},
  author={Peinador Sala, Jos{\'e} Ignacio},
  journal={Submitted to Journal of Physics A: Mathematical and Theoretical},
  note={Manuscript ID: JPhysA-125419},
  year={2026},
  month={July},
  doi={10.5281/zenodo.18703610},
  url={https://github.com/NachoPeinador/The-Emergence-of-Geometry}
}

```

---

## ✉️ Contact & Author

**Dr. José Ignacio Peinador Sala**

*Independent Researcher — Valladolid, Spain*

---

📌 Publication Status: Submitted to *Journal of Physics A: Mathematical and Theoretical* in July 2026 - Manuscript ID: JPhysA-125419.
