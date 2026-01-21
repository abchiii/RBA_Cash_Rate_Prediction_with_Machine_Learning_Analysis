# RBA Cash Rate Prediction with Machine Learning Analysis

**Author:** Ching-Ting Huang (Collaborated with 3 team members)  

**Course:** ECOM90025 Advanced Data Analysis, University of Melbourne

## Project Overview
This project investigates the predictability of the Reserve Bank of Australia (RBA) cash rate decisions using a hybrid machine learning approach. Unlike traditional econometric forecasting which often relies on linear assumptions, this study compares parametric (Multinomial Logistic Regression) and non-parametric (Random Forest, Decision Trees, XGBoost) models to capture non-linear market dynamics.

Using a dataset of 26 macroeconomic indicators (based on Vasnev et al., 2011) covering domestic and international factors, we aim to identify the most effective predictive framework for Australian monetary policy trends.

## Research Questions
1.  **Model Performance:** Which model achieves the highest accuracy in predicting RBA cash rate decisions?
2.  **Key Drivers:** What are the most important economic indicators (e.g., inflation, GDP) that influence the RBA's decisions?
3.  **Complexity vs. Performance:** Does using more complex machine learning models (like Random Forest or XGBoost) actually provide better results than a standard logistic regression?

## Methodology
The analysis is conducted in **Python** using a rigorous data science workflow:

### 1. Data Preprocessing & Selection
* **Variable Selection:** 26 key variables were selected with 3 lags based on economic literature, categorided into Domestic Economic Indicators, Foreign Financial Variables, and Domestic Financial Markets.
* **Hybrid Feature Selection:**
    * **Lasso Regression (L1):** Used for initial dimensionality reduction and regularisation.
    * **Random Forest Feature Importance:** Applied to refine the variable set and identify non-linear contributors.
    * **Interaction Refinement:** Pairwise interactions were generated for selected features to capture complex dependencies.

### 2. Model Development
Five distinct classification models were trained and evaluated:
* **Model 1 & 2:** Multinomial Logistic Regression (Comparing Interaction Sets).
* **Model 3:** Random Forest Classifier.
* **Model 4:** Decision Tree.
* **Model 5:** XGBoost.

### 3. Evaluation Metrics
* **Performance:** Models were assessed using Accuracy, Confusion Matrices, and Classification Reports.
* **Validation:** Cross-validation was employed to minimise overfitting and ensure out-of-sample robustness.

## Key Findings
Our empirical results suggest that machine learning offers significant advantages in policy forecasting:

* **Best Performing Model:** The Random Forest achieved the highest predictive accuracy of 73%, outperforming the logistic regression baseline.
* **Drivers of Policy:** The analysis identified 'Annual Growth in CPI' and 'Inflation Expectation' as the most significant predictors of RBA decisions.
* **Non-Linearity:** The superior performance of tree-based models (Random Forest/XGBoost) confirms that the relationship between macroeconomic indicators and central bank decisions is highly non-linear.

## Repository Structure
* `Forecasting_RBA_Monetary_Policy.ipynb`: The comprehensive end-to-end analysis notebook, containing the project introduction, full data pipeline, model implementations, and final comparative conclusions.
* `data/`: Folder containing the dataset used for training and testing.
* `README.md`: Project documentation.

## Libraries Used
* **Machine Learning:** `scikit-learn`, `xgboost`.
* **Data Manipulation:** `pandas`, `numpy`.
* **Visualization:** `matplotlib`, `seaborn`, `graphviz`.

---
*This project was completed as part of the Master of Applied Econometrics curriculum.*
