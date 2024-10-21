# README for Machine Power Optimization Project

## Objective
The objective of this exercise is to:
1. Learn the power usage of physical machines as a function of three inputs.
2. Formulate and solve an optimization problem to reduce the overall power consumption of the machines running together and save energy.

## Project Structure
- data/: This folder contains the datasets for the two types of machines (`machine1.csv` and `machine2.csv`).
- jupyter_notebook/: This folder contains the Jupyter Notebook files where the analysis, model training and optimization are performed.
- models/: This folder stores the saved KNN models for both machine types (`knn_machine1_model.pkl`, `knn_machine2_model.pkl`).
- output/: This folder contains the output Excel file (`machine_power_data.xlsx`) with the calculated power data for each machine.
- conclusion/: This folder contains the conclusion and explanation of methodologies used in the project.
- extras/: Optional folder containing additional content.

## Setup Instructions
To run this project, please ensure you have the following software installed:

1. Python: Make sure you have Python (version 3.6 or higher) installed on your system.
2. Required Libraries: Install the necessary Python libraries by running the following command:
   pip install -r requirements.txt


## Usage Instructions
1. Place the datasets (`machine1.csv` and `machine2.csv`) in the data/ folder.
2. Open a terminal and navigate to the jupyter_notebook/ folder.
3. Start Jupyter Notebook by running:
   jupyter notebook
4. Open the relevant `.ipynb` files to execute the code step-by-step:
   - Step 1: Learn the power usage using KNN regression.
   - Step 2: Optimize the goods production per hour (GPH) for the machines.

## Assumptions
- The 'check' column in the datasets is used to filter valid data points, and only rows with values between 90 and 110 are considered for model training.
- The models assume a linear relationship between GPH and power usage, as learned from the training data.

## Limitations
- The optimization problem is solved using linear programming, which may not capture non-linear relationships between GPH and power usage.
- The models trained are based on the provided datasets, and their accuracy may vary with different data distributions or external factors affecting machine performance.

## Rationale for Decisions
- KNN was chosen for its simplicity and effectiveness in regression tasks, for predicting power usage based on GPH inputs.
- The optimization approach focuses on balancing power consumption while meeting production targets, which aligns with energy-saving objectives in industrial settings.
