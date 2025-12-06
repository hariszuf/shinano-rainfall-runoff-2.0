# shinano-rainfall-runoff-2.0
# Shinano River Rainfall–Runoff Modelling (2025)

This repository contains a modern, fully reproducible rainfall–runoff modelling workflow
for the Shinano River system in Japan. It integrates:

- JMA meteorological data (rainfall, temperature, snow)
- MLIT river discharge data
- Basin shapefiles for hydrological delineation
- NeuralHydrology deep learning framework (LSTM, GRU, Transformer)
- A clean CS-style data pipeline for scientific reproducibility

This is Version 2.0 of my original 2022 proof-of-concept project completed during my
Overseas Industry Immersion Programme at NIT Nagano College.

The 2025 version focuses on correctness, reproducibility, hydrological realism, and
benchmarking modern neural rainfall–runoff architectures.

---

## Project Workflow

1. Collect JMA & MLIT raw data → `data_raw/`
2. Clean & standardize units → `scripts/03_clean_jma.py`, `04_clean_mlit.py`
3. Aggregate rainfall by basin → `scripts/05_extract_basin_rainfall.py`
4. Build NeuralHydrology forcing + discharge files → `scripts/06_build_forcing_files.py`
5. Train models using `nh_configs/*.yml`
6. Save metrics + hydrographs → `results/`

---

## Repository Structure

(Include the tree here)

---

## Requirements

- Python 3.10+
- Conda (recommended)
- NeuralHydrology
- xarray, rioxarray, geopandas, rasterstats
- pandas, numpy, matplotlib

Install with:
conda env create -f environment.yml
conda activate shinano


---

## Future Work

- Snow-aware modelling
- Multi-basin training
- Transfer experiments
- Hybrid physics–ML rainfall–runoff model

---

## Acknowledgements

Data:
- JMA AMeDAS meteorological observations
- MLIT river discharge archives

Research context inspired by hydrology work conducted during OIIP (NIT Nagano).

