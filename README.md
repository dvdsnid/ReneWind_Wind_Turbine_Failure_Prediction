# ReneWind: Wind Turbine Failure Prediction

## Project overview

This project uses neural-network classification to predict generator failures in wind turbines. The goal is to help maintenance teams identify potential failures earlier and reduce the cost of unplanned component replacement.

The notebook explores the dataset, preprocesses numerical features, and compares several neural-network configurations. It focuses on **recall for the failure class**, because missing a real failure can be more costly than investigating a false alarm.

## What the notebook covers

- Data loading and exploratory data analysis
- Missing-value imputation and feature scaling
- Handling a strongly imbalanced target using class weights
- Comparing neural-network architectures and training choices, including:
  - A baseline network
  - Additional hidden layers
  - Dropout regularization
  - Class weighting
  - SGD and Adam optimizers
- Comparing training and validation metrics
- Selecting a model and evaluating it on the held-out test set
- Translating model results into maintenance recommendations

## Technology

- Python
- pandas and NumPy
- Matplotlib and Seaborn
- scikit-learn
- TensorFlow / Keras
- Google Colab (the notebook uses Google Drive to load data)

## Data requirements

The notebook expects two CSV files named `Train.csv` and `Test.csv` in the root of your Google Drive (`MyDrive`):

```text
MyDrive/
├── Train.csv
└── Test.csv
```

**The CSV datasets are not included in this repository.** Obtain them from the authorized project/course source and place them in the expected location, or update the notebook's file paths to match your setup.

## How to run

1. Open `notebooks/ReneWind_Wind_Turbine_Failure_Prediction.ipynb` in Google Colab.
2. Upload `Train.csv` and `Test.csv` to your Google Drive under `MyDrive`, or update the paths in the data-loading cell.
3. Run the notebook cells in order.
4. Review recall, precision, F1 score, and confusion matrices together. A high recall can come with more false alarms, so consider the operational cost of both missed failures and unnecessary inspections.

## Important note

This is an educational predictive-maintenance project. Model predictions should be validated against real operational data and engineering expertise before they are used in maintenance decisions.

## Repository structure

```text
ReneWind_Wind_Turbine_Failure_Prediction/
├── README.md
├── requirements.txt
├── .gitignore
└── notebooks/
    └── ReneWind_Wind_Turbine_Failure_Prediction.ipynb
```
