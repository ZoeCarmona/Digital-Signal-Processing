# Digital-Signal-Processing
This repository contains code, reports, and materials developed for the **Digital Signal Processing (DSP)** course.

Its main purpose is to organize practical assignments, experiments, and resources related to signal analysis, filtering, frequency-domain transformations, and DSP applications.

## Contents

- **Homework 1:**  
  In this task, we studied fundamental discrete-time signal operations in Digital Signal Processing (DSP). The theoretical part included concepts such as periodicity, energy and power signals, mean and RMS, time shifting, and time reversal. All exercises were first solved manually to understand the mathematical reasoning behind each operation.

  In the Colab notebook, the same problems were implemented computationally using explicit loops and index mapping (without built-in shortcuts), allowing verification through numerical results and graphical visualization. This practice reinforced both the theoretical foundations and their practical implementation in Python.

- **Homework 2:**  
  In this task, we implemented the **Discrete Fourier Series (DFS)** for three periodic discrete-time signals: a square wave (N=16), a triangle wave (N=32), and a sum of sinusoids (N=64). The theoretical part included manual derivation of DFS coefficients using geometric series and Euler's identity, analysis of magnitude and phase spectra, and verification of the spectral symmetry property of real signals.
  
  In the Colab notebook, custom `dfs()` and `idfs()` functions were implemented from scratch using `np.dot` (no FFT functions allowed), producing stem plots for each signal's spectrum and reconstruction. All three signals achieved perfect reconstruction with RMSE ≈ 10⁻¹⁵.

## Notes

- This repository will be updated progressively throughout the course.
- Each practice may include source code, documentation, plots, and results.

---

**Digital Signal Processing Course**
