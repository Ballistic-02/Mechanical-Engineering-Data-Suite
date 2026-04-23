# Predictive Maintenance: Turbofan Engine RUL Prediction
## Project Overview
This project applies Machine Learning to industrial reliability engineering. Using the NASA C-MAPSS (Commercial Modular Aero-Propulsion System Simulation) dataset, I built a predictive model to estimate the Remaining Useful Life (RUL) of jet engines based on multi-sensor telemetry data.

By forecasting the exact cycle of failure, this tool enables Condition-Based Maintenance (CBM)—moving away from "fix it when it breaks" toward "fix it before it fails."

## Key Results
* Training RMSE: ~28.86 cycles (Achieved using Random Forest Regressor).

* Data Source: NASA FD001 (100 engines for training, 100 for testing).

* Visual Proof: Successfully mapped sensor degradation curves (e.g., Sensor 11) showing clear upward trends as failure approaches.

## Technical Skills Applied
* Feature Engineering: Calculated RUL using "Run-to-Failure" logic; performed feature selection by removing constant-value sensors with zero variance.
* Data Preprocessing: Handled raw .txt files with custom Pandas pipelines, applied StandardScaler to normalize sensor readings (Pressure, Temperature, Fan Speed).
* Machine Learning: Implemented a Random Forest Regressor to handle non-linear sensor relationships.
* Visualization: Created trend plots using Seaborn to identify the most critical sensors for failure prediction.

## Repository Structure
* Untitled.ipynb: Full end-to-end Jupyter Notebook with data cleaning, EDA, and modeling.
* CMaps/: Folder containing the raw NASA dataset files (train_FD001.txt, test_FD001.txt, etc.).
* README.md: Project documentation and overview.

# Setup & Installation

* Install dependencies:

Bash

`pip install pandas numpy scikit-learn matplotlib seaborn`

* Run the analysis: Open the notebook in VS Code and run all cells.
