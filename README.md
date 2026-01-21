# Tropical Cyclones Stochastic Simulation
This repository contains a probabilistic model for simulating **Tropical Cyclone (TC)** tracks and intensity evolution. It uses historical data from **IBTrACS** and environmental parameters (Maximum Potential Intensity) to generate synthetic storm trajectories and model their wind speed decay upon landfall.

## Key Features
* **Stochastic Track Generation:** Simulates storm deviations and trajectories based on historical statistics.
* **Intensity Modeling:** Implements wind speed decay models considering land interaction (using `global_land_mask`).
* **Data Integration:** Combines IBTrACS best-track data with MPI (Maximum Potential Intensity) climatology.

## Repository Structure
* **`Final_Model.ipynb`**: The core simulation kernel. Loads historical tracks, fits statistical distributions (Beta, Lognormal, Burr), and generates synthetic storm realizations.

## Setup & Usage

### 1. Prerequisites
Install the required Python scientific libraries:
```bash
pip install -r requirements.txt
