# ml-ship-fuel-consumption
Machine Learning project – Ship fuel consumption prediction

# Machine Learning Project – Ship Fuel Consumption Prediction

This repository contains a machine learning project developed as part of the ESILV Machine Learning course.
The objective of the project is to predict ship fuel consumption based on operational and technical parameters
using supervised regression models.

The project emphasizes methodological rigor, model comparison, and critical analysis of data limitations.

---

## Business Objective

Fuel consumption is a key performance indicator in maritime engineering, with direct implications for operating
costs, energy efficiency, and environmental impact.
The goal of this project is to explore how machine learning models can be used to estimate ship fuel consumption
from operational data, and to analyze the trade-offs between model complexity, accuracy, and interpretability.

---

## Dataset

- File: `ship_fuel_efficiency.csv`
- Type: Structured tabular dataset
- Number of observations: 1,440
- Number of variables: 10
- Target variable: `fuel_consumption`

### Feature categories
- Identification variables: `ship_id`, `route_id`, `month`
- Operational variables: `distance`, `engine_efficiency`, `weather_conditions`
- Ship characteristics: `ship_type`
- Fuel-related variables: `fuel_type`, `CO2_emissions`

> ⚠️ Note: The dataset is synthetic or partially simulated. Strong correlations between some variables
(particularly fuel consumption and CO2 emissions) introduce target leakage risks and limit the effective
use of highly expressive models.

---

## Methodology

The project follows a standard machine learning workflow:
1. Exploratory data analysis and visualization
2. Data preprocessing (encoding, scaling, train–test split)
3. Baseline model training
4. Advanced model experimentation
5. Model evaluation and comparison
6. Critical analysis of limitations

All preprocessing and modeling steps are implemented using pipelines to prevent data leakage and ensure
reproducibility.

---

## Models Explored

### Baseline Models
- Linear Regression
- Ridge Regression

### Tree-Based Ensemble Models
- Random Forest Regressor

### Advanced Models (Experimental)
- XGBoost Regressor
- Multi-Layer Perceptron (MLP) Regressor

### Dimensionality Reduction
- Principal Component Analysis (PCA)

> Advanced models were tested experimentally. Their potential benefits were limited by dataset size,
synthetic structure, and strong feature correlations, which constrained generalization performance.

---

## Evaluation

Models are evaluated on an independent test set using the following metrics:
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² score

Random Forest achieved the best overall performance among the evaluated models, indicating the importance
of non-linear relationships between operational variables and fuel consumption.

---

## Results Summary

| Model               | MAE   | RMSE  | R²    |
|--------------------|-------|-------|-------|
| Linear Regression  | 880.4 | 1193.0| 0.947 |
| Ridge Regression   | 879.6 | 1192.9| 0.947 |
| Random Forest      | 651.4 | 1134.6| 0.952 |

> Metrics correspond to performance on the held-out test set.

---

## Limitations

- Synthetic or simulated dataset limits real-world applicability
- Strong correlations between certain variables (e.g., CO2 emissions and fuel consumption)
- Limited dataset size restricts effective use of highly complex models
- Evaluation based on a single train–test split

These limitations emphasize that model performance is constrained more by data quality than by algorithmic
complexity.

---

## Repository Structure

ml-ship-fuel-consumption/
│
├── Ship.consumption.ipynb
├── ship_fuel_efficiency.csv
├── report/
│ └── ml_project_report.pdf
└── README.md


---

## How to Run

1. Open `Ship.consumption.ipynb`
2. Restart the kernel
3. Run all cells from top to bottom

---

## References

- Géron, A. *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow*
- Chen, T., & Guestrin, C. (2016). XGBoost: A scalable tree boosting system.
- Scikit-learn documentation: https://scikit-learn.org
- ESILV Machine Learning course material

---

## Authors

- Léopold REHLINGER – ESILV

