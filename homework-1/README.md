# Practice 1 — Discrete-Time Signal Operations

## Overview

This assignment focuses on fundamental concepts of **Discrete-Time Signal Processing (DSP)**, combining theoretical analysis and computational implementation.

The objective was to first solve each problem manually (paper-based reasoning), and then verify the results through a Google Colab notebook using Python.

---

## Topics Covered

The practice includes the following core DSP concepts:

- Continuous vs. discrete signals
- Periodic vs. aperiodic signals
- Energy and power signals
- Nyquist sampling criterion
- Time shifting and time reversal
- Signal transformations
- Mean value and RMS
- Energy of exponential sequences
- Autocorrelation and cross-correlation

---

## Theoretical Component

Each exercise was solved manually to:
- Apply mathematical definitions.
- Analyze signal behavior through index manipulation.
- Determine properties such as periodicity, causality, energy, and power.
- Compute mean, RMS, and correlation values step by step.

This ensured conceptual understanding before coding.

---

## Computational Component (Google Colab)

The same problems were implemented in Python using:

- Explicit loops
- Index mapping
- Zero padding for finite signals
- Custom implementations (without using shortcut functions such as `np.flip`, `np.roll`, or `np.correlate`)

The notebook includes:
- Signal generation
- Graphical visualization using stem plots
- Numerical verification of theoretical results
- Validation of periodicity and energy calculations

---

## Key Results

- Verified periodicity of \( x[n] = \cos\left(\frac{5\pi}{6}n\right) \) with fundamental period \( N_0 = 12 \)
- Computed energy of exponential signals using geometric series
- Confirmed RMS ≠ 0 even when mean = 0
- Obtained:
  - Autocorrelation: \( \{1,4,6,4,1\} \)
  - Cross-correlation: \( \{-1,-2,0,2,1\} \)

---

## Learning Outcomes

This practice reinforced:

- Understanding of discrete-time signal transformations
- Relationship between mathematical definitions and computational implementation
- Careful index handling in correlation and shifting operations
- Conceptual difference between energy and power signals
- The importance of validating manual results programmatically

---

## Tools Used

- Python
- NumPy
- Matplotlib
- Google Colab

