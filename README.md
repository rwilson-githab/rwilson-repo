# HARMPI GRMHD: SANE and MAD accretion experiments

Research workflow by Robert Wilson Joute. This repository documents and reproduces the supplied HARMPI notebook, not an exotic compact object echo simulation.

## Overview
The workflow builds the upstream [HARMPI](https://github.com/atchekho/harmpi) C code at revision `d2673a9`, edits a torus problem, runs a short baseline and compares longer simulations with two magnetic-field prescriptions. The labels SANE and MAD denote intended configurations, not verified physical classifications.

| Parameter | Value |
|---|---|
| N1, N2 | 64, 64 |
| Adiabatic index | 13/9 |
| Dimensionless spin | 0.9375 |
| Inner torus radius | 10 M |
| Pressure maximum radius | 20 M |
| Outer radius | 1000 M |
| Baseline end time | 200 M |
| Comparison end time | 1000 M |

## Getting started
1. Fork this repository using the GitHub Fork button.
2. Open the notebook in Google Colab (CPU runtime).
3. Run the cells in order; use a fresh runtime for a new experiment. The original workflow deletes previous simulation dumps in its working directories.
4. Inspect build logs and wait for both simulations to finish before comparing their outputs.
5. Archive results separately from Git; the optional Drive export requires authorization.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/rwilson-githab/rwilson-repo/blob/main/notebooks/harmpi_wilson.ipynb)

## Physics and diagnostics
The notebook plots density and poloidal magnetic field contours, plasma beta, magnetization, horizon mass accretion rate and normalized magnetic flux. See [methods](docs/methods.md) and [validation](docs/validation.md).

## Reproducibility status
The notebook was inspected but the C solver and long simulations have not been executed or scientifically validated during repository preparation. No observational or publication-ready result is claimed. HARMPI is an external dependency; credit its developers and check its upstream license before redistribution. No new license is asserted for the submitted notebook pending the owner's choice.

## Citation
See CITATION.cff for project attribution. Cite the upstream HARMPI software and relevant scientific literature separately.
