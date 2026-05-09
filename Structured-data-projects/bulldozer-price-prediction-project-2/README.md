# Bulldozer Price Prediction

A regression project that predicts the future sale price of bulldozers at auction using historical equipment and sales data (time series).

---

## What the project does

Given a bulldozer's specs, machine age, usage history, configuration, and sale details, the model predicts what it will sell for at auction. The target is a continuous sale price, so this is a regression problem.

---

## Dataset

Historical Bluebook bulldozer auction data. It's messy by nature like missing values, dates stored as strings, and high-cardinality categoricals. Most of the actual work in this project happened before any model was trained.

Features include:
- Sale date and location
- Machine age and product size
- Model and configuration info
- Usage characteristics
- Product group

---

## Approach

- Dates were broken into usable features: year, month, day, and machine age at time of sale
- Missing values handled properly before modelling
- Categorical variables encoded
- Random Forest Regressor trained and tuned after preprocessing

Metrics used for evaluation:
- **RMSLE** as the primary metric, since it penalises large relative errors
- **MAE** and **R²** tracked alongside

---

## Project Structure

```bash
bulldozer-price-prediction-project-2/
│
├── assets/images/
├── data/
├── .gitattributes
├── end-to-end-bluebook-bulldozer-price-regression.ipynb
└── environment.yml
```

---

## Stack

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square&logo=python&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
