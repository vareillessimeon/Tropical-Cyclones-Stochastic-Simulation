# Stochastic Tropical Cyclone Model (IRIS Foundations)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Status](https://img.shields.io/badge/Status-Academic_Research-orange)

**Author:** Siméon Vareilles  
**Institution:** Imperial College London (Space and Atmospheric Physics Group)  
**Supervisor:** Prof. Ralf Toumi  
**Project:** MSc Dissertation (Awarded Distinction)

---

## 🌪️ Overview

This repository contains the source code for the **Stochastic Tropical Cyclone Model**, developed to assess cyclone risk by generating synthetic storms based on historical statistics and physical constraints.

Unlike purely statistical models, this approach integrates the **Maximum Potential Intensity (MPI)** theory. It uses historical data from the past 40 years to extract decay characteristics and generates new tracks that respect the physics of energy limits over ocean and land.

**Key Features:**
* **Stochastic Generation:** Uses Markov Chains (`XX` matrices) to determine storm intensity changes.
* **Physics-Aware:** Constrained by MPI fields derived from climatology.
* **Decay Modeling:** Simulates intensity decay upon landfall using probabilistic decay factors.
* **Validation:** Includes tools to compare synthetic return periods against historical IBTrACS data.

---

## 📂 Repository Structure

```text
Tropical-Cyclone-Stochastic-Model/
├── data/                       # Contains all statistical matrices and track databases
│   ├── LMItracks.pkl           # Historical storm tracks
│   ├── XX, XX_fs, XX_nr...     # Transition probability matrices
│   ├── mix_lognorm_ratio...    # Ratio distributions (Near Land/Sea)
│   └── mpi_out/                # FOLDER: Contains NetCDF MPI maps 
├── analysis/                   # Validation and Profiling
│   ├── Intensity_Decay_Validation.ipynb
│   ├── RMW_R34_distributions.ipynb
│   └── Wind_Rain_Profile_Analysis.ipynb
├── Final_Model.ipynb           # CORE: The main simulation engine
├── requirements.txt            # Python dependencies
└── README.md                   # This file
