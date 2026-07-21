# Medical Insurance Cost Prediction - Multiple Linear Regression

## Assignment-1 | AI-ML Course

---

## Objective

To develop a Multiple Linear Regression model that predicts medical insurance charges based on personal and health-related features such as age, sex, BMI, number of children, smoking status, and region.

---

## Dataset Link

- **Kaggle Dataset:** [Medical Cost Personal Datasets](https://www.kaggle.com/datasets/mirichoi0218/insurance)
- **Source:** Machine Learning with R by Brett Lantz (public domain)
- **Rows:** 1,338
- **Columns:** 7 (age, sex, bmi, children, smoker, region, charges)

---

## Libraries Used

| Library | Purpose |
|---------|---------|
| `pandas` | Data loading and manipulation |
| `numpy` | Numerical computations |
| `matplotlib` | Data visualization |
| `seaborn` | Statistical plots |
| `scikit-learn` | Model building, preprocessing, evaluation |

---

## Methodology

1. **Data Understanding:** Loaded the dataset, displayed first 5 records, and identified numerical features (`age`, `bmi`, `children`), categorical features (`sex`, `smoker`, `region`), and target variable (`charges`).

2. **Data Preprocessing:** 
   - Checked for missing values (none found)
   - Encoded categorical variables using Label Encoding (`sex`, `smoker`) and One-Hot Encoding (`region`)
   - Split data into 80% training and 20% testing sets

3. **Model Development:** Built a Multiple Linear Regression model using all features to predict insurance charges.

4. **Model Evaluation:** Computed MAE, MSE, and R² Score. Created an Actual vs Predicted scatter plot.

---

## Results

| Metric | Value |
|--------|-------|
| Mean Absolute Error (MAE) | $4,181.19 |
| Mean Squared Error (MSE) | 33,596,915.85 |
| R² Score | **0.7836** |

### Key Findings:
- **Smoking status** is the most influential factor (coefficient ≈ 23,651)
- **BMI** and **Age** are the next most significant predictors
- **Region** has minimal impact on insurance charges
- The model explains ~78.4% of variance in charges

---

## Conclusion

The Multiple Linear Regression model achieved an R² score of 0.7836, effectively capturing the relationship between personal/health features and insurance charges. Smoking status dominates as the primary cost driver. However, Linear Regression's linearity assumption limits its ability to model interaction effects (e.g., age × smoking) and non-linear patterns, especially for high-cost outliers. Advanced models like Polynomial Regression or Random Forest could improve prediction accuracy for extreme values.

---

## How to Run

```bash
# Install dependencies
pip install pandas numpy matplotlib seaborn scikit-learn

# Run the script
python Assignment-1.py
```

---

## Author

*Submitted for AI-ML Assignment-1*
