# California Housing Price Prediction

Implementing the same linear-regression workflow in **two languages** to compare the process and
the results. The goal is to predict the median house value (`MedHouseVal`) of California districts
from eight socioeconomic and geographic features.

- Python notebook: [`housing_price_regression_python.ipynb`](housing_price_regression_python.ipynb) (pandas, scikit-learn, matplotlib)
- R notebook: [`housing_price_regression_r.ipynb`](housing_price_regression_r.ipynb) (dplyr, caret, ggplot2)

## Workflow (both notebooks)

1. Import libraries.
2. Load the California Housing dataset.
3. Show the first five rows.
4. Check for missing data.
5. Impute missing values with the mean.
6. Scale the features (StandardScaler / `scale`).
7. Train/test split (80/20).
8. Train a linear regression model.
9. Predict on the test set.
10. Evaluate with R² and MSE.
11. Display the learned weights and bias.
12. Plot predicted vs actual house prices.

## Results

| Language | R² | MSE |
|----------|------|------|
| Python   | 0.576 | 0.556 |
| R        | 0.592 | 0.564 |

The two languages give consistent results; small differences come from the different train/test
partition routines.

## Running it

```bash
# Python
pip install numpy pandas matplotlib scikit-learn
# R
install.packages(c("dplyr", "ggplot2", "caret"))
```

Open either notebook with the matching Jupyter kernel.

## Files

| File | Description |
|------|-------------|
| `housing_price_regression_python.ipynb` | Full Python implementation and analysis |
| `housing_price_regression_r.ipynb` | Full R implementation and analysis |
| `california_housing.csv` | Dataset (exported from scikit-learn; used by the R notebook) |
| `PROJECT_BRIEF.pdf` | Project brief (goals, objectives, outcomes) |
