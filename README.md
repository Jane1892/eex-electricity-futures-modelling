# Smoothing the Curve: Forward Curve Construction and Factor Dynamics in German Electricity Futures

**Authors:** Cora Abelseth and Jana Ondicova
**Programme:** Master in Quantitative Finance
**Institution:** BI Norwegian Business School   
**Supervisor:** Alessandro Graniero
**Year:** 2026

## Overview

This repository contains the code and data to reproduce the results of the thesis, covering data processing, forward curve and synthetic futures prices construction, PCA-based factor analysis, and parametric market model estimation in German electricity futures.

## Repository Structure

```
├── code.ipynb              # Main notebook - run top to bottom to reproduce all results
├── environment.yml         # Conda environment (recommended)
├── requirements.txt        # pip alternative
├── Data/
│   └── Raw/                # Original raw data files (from Montel), never modified
│   └── Processed/          # Cleaned data and synthetic panels (generated in the notebook)
└── Results/                # All output figures and tables (generated in notebook)
```

## Reproducing the Results

### 1. Set up the environment

Using conda (recommended):

```bash
conda env create -f environment.yml
conda activate thesis-env
```

Using pip:

```bash
pip install -r requirements.txt
```

### 2. Run the notebook

Open `code.ipynb` and run all cells from top to bottom. Export switches at the top of the notebook control whether intermediate data and results are saved.

## Reproducibility Warning

> **Results are operating system- and version-sensitive.**

Numerical results were produced on **Windows 11** with **Python 3.13.9** and the exact package versions in `environment.yml`. Results may differ on macOS or Linux even with identical package versions, because different operating systems implement floating-point operations in different order, leading to small numerical differences that compound through iterative optimisation routines (e.g. curve fitting in `scipy.optimize`).

To reproduce results exactly, use the conda environment on **Windows** with the pinned versions in `environment.yml`.


## Requirements

| Package    | Version |
|------------|---------|
| Python     | 3.13.9  |
| numpy      | 2.3.4   |
| scipy      | 1.16.3  |
| pandas     | 2.3.3   |
| matplotlib | 3.10.6  |
| openpyxl   | 3.1.5   |
