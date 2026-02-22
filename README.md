# CCPP Power Output Prediction

This project predicts hourly net electrical energy output (MW) of a Combined Cycle Power Plant (CCPP) using supervised regression models in Python.

## Problem Statement

Given environmental conditions:
- Ambient Temperature (AT)
- Exhaust Vacuum (V)
- Ambient Pressure (AP)
- Relative Humidity (RH)

Predict the net hourly electrical energy output (PE).

This problem demonstrates:
- Regression modeling
- Cross-validation
- Model comparison
- Feature importance analysis
- Practical ML evaluation using MAE

---

## Modeling Approach

1. Baseline: Linear Regression
2. Model comparison: Random Forest Regressor
3. 5-fold Cross-Validation used for robust evaluation
4. Evaluation metric: Mean Absolute Error (MAE)

---

## Results

| Model | Test MAE | Test R² |
|--------|-----------|-----------|
| Linear Regression | 3.60 MW | 0.93 |
| Random Forest | **2.31 MW** | **0.964** |

Random Forest reduced prediction error by ~36% compared to the linear baseline.

---

## Key Insights

- Ambient Temperature is the dominant predictor (~90% feature importance in RF).
- The relationship between environmental variables and power output is nonlinear.
- Cross-validation confirmed strong model stability.

---

## Reproducibility

To recreate the environment:

### Option 1: Conda
conda env create -f environment.yml
conda activate course1

### Option 2: Using pip
pip install -r requirements.txt


Then run the notebook:
AI-PM-Course1.ipynb

## Tools Used
 - Python
 - pandas
 - scikit-learn
 - matplotlib
 - seaborn
 - Jupyter Notebook

