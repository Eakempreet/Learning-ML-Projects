# Heart Disease Prediction

A binary classification project that predicts whether a patient has heart disease based on clinical data.
Built as part of my ML learning, the goal was to go through the full pipeline properly, not just fit a model and call it done.

---

## What the project does

Given a set of medical attributes, things like age, cholesterol, chest pain type, resting blood pressure, and max heart rate — the model predicts:

- `1` → Heart disease present  
- `0` → No heart disease

---

## Approach

Started with data loading and a thorough EDA to understand the features before touching any model. Trained three classifiers 
- Logistic Regression,
- KNN,
- and Random Forest
then tuned and evaluated each one using accuracy, precision, recall, F1, confusion matrix, and ROC curve. The best model was saved for reuse.

---

## Project Structure

```bash
Heart-Disease-Project-1/
│
├── assets/images/
├── dataset/
├── Heart-Disease-LR-Model
├── commands.ipynb
├── end-to-end-heart-disease-classification.ipynb
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
