# Task 5: Sales Prediction Using Python

Regression project that predicts product **sales** from advertising spend on **TV, Radio and Newspaper**.

**Author:** Dharani

## Dataset
`Advertising.csv` (200 rows: TV, Radio, Newspaper spend and Sales). No missing values. Included in this repository.

## What I did
- EDA: null check, descriptive statistics, pairplot
- Scatter plots of Sales vs each channel, and a correlation heatmap
- 80/20 train/test split
- Trained 3 models: Linear Regression (baseline), Polynomial Regression (degree 2), Random Forest Regressor
- Evaluated with MAE, RMSE and R2
- Residual analysis for the best model
- Channel impact using standardised coefficients and Random Forest feature importance

## Results
| Model | MAE | RMSE | R2 |
|---|---|---|---|
| Polynomial Regression (deg 2) | 0.53 | 0.64 | 0.987 |
| Random Forest | 0.63 | 0.76 | 0.982 |
| Linear Regression | 1.46 | 1.78 | 0.899 |

**Best model: Polynomial Regression (degree 2).**

## Key findings
- **TV** has the highest impact on sales, followed by **Radio**.
- **Newspaper** has almost no effect.
- The polynomial model beats the linear baseline because TV and Radio work better together (interaction effect).

## How to run
1. Put `Dharani_Task5.ipynb` and `Advertising.csv` in the same folder (or upload both to Google Colab).
2. Click **Run All**.

## Tech stack
Python, pandas, scikit-learn, matplotlib, seaborn, Jupyter Notebook
