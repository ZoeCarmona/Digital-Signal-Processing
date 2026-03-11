# Practice 2 — Discrete Fourier Series (DFS)

## Overview
This assignment focuses on the **Discrete Fourier Series (DFS)** for periodic discrete-time signals, combining theoretical analysis and computational implementation.

The objective was to first analyze each signal manually (deriving coefficients step by step using mathematical definitions), and then verify the results through a Google Colab notebook using Python.

---

## Topics Covered

The practice includes the following core DSP concepts:

- Discrete Fourier Series (DFS) definition and properties
- Complex exponential basis functions
- DFS analysis (forward transform)
- DFS synthesis (inverse transform)
- Magnitude and phase spectra
- Signal reconstruction and reconstruction error (RMSE)
- Spectral symmetry of real signals

---

## Signals Analyzed

Three periodic discrete-time signals were implemented and analyzed, each with a different period:

| Signal | Type | Period |
|--------|------|--------|
| A | Square wave | N₁ = 16 |
| B | Triangle wave | N₂ = 32 |
| C | Sum of sinusoids | N₃ = 64 |

---

## Theoretical Component

Each signal was analyzed manually to:

- Define the signal over exactly one period.
- Apply the DFS analysis formula using geometric series and Euler's identity.
- Compute DFS coefficients X[k] step by step.
- Explain why certain coefficients are zero (even harmonics) and others are not (odd harmonics).
- Interpret the magnitude and phase spectra.
- Verify the spectral symmetry property: |X[k]| = |X[N−k]| for real signals.

This ensured conceptual understanding before coding.

---

## Computational Component (Google Colab)

The same problems were implemented in Python using:

- Manual summation via `np.dot` (no FFT functions allowed)
- Explicit loop over each frequency index k
- Custom `dfs()` and `idfs()` functions from scratch

The notebook includes:

- Signal generation for all three signals
- DFS coefficient computation without `np.fft.fft` or any FFT helper
- Graphical visualization using stem plots
- Numerical verification of theoretical results

---

## Deliverables (per signal)

For each of the three signals the following were produced:

1. Plot of the signal over one period: $x[n]$, $n = 0..N-1$
2. Stem plot of the magnitude spectrum: $|X[k]|$
3. Plot of the phase spectrum: $\angle X[k]$
4. Plot comparing original $x[n]$ vs reconstructed $\hat{x}[n]$
5. RMSE value and interpretation

---

## Key Results

- **Signal A (Square wave):** Non-zero coefficients only at odd harmonics (k=1,3,5,...), magnitude decays as 1/k. RMSE ≈ 10⁻¹⁵.
- **Signal B (Triangle wave):** Non-zero coefficients only at odd harmonics, magnitude decays as 1/k² (faster than square wave due to smoother shape). RMSE ≈ 10⁻¹⁵.
- **Signal C (Sum of sinusoids):** Only 6 non-zero coefficients (k=1,2,3 and their mirror images k=61,62,63). Phase values reflect exactly the +0.3 and −0.8 offsets defined in the signal. RMSE ≈ 10⁻¹⁵.
- In all three cases, using all N coefficients yields **perfect reconstruction**.

---

## Restrictions Followed

- Only `numpy` and `matplotlib` were used
- Summations computed using `np.sum` / `np.dot`
- `np.fft.fft`, `np.fft.ifft`, or any FFT helper were NOT used

---

## Learning Outcomes

This practice reinforced:

- Understanding of the DFS as a tool to decompose periodic signals into frequency components
- Relationship between signal smoothness and spectral decay rate
- Spectral symmetry property of real signals
- The difference between signals with many active harmonics (square, triangle) vs. few (sum of sinusoids)
- The importance of using all N coefficients to achieve perfect reconstruction (RMSE ≈ 0)

---

## Tools Used

- Python
- NumPy
- Matplotlib
- Google Colab
