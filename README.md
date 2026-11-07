# Customer Churn Prediction & Analysis

Predicting which telecom customers are likely to churn, and finding out why, using the IBM Telco Customer Churn dataset (7,043 customers, 21 columns).

## Project Steps
1. Data cleaning (fixed TotalCharges, dropped customerID)
2. Exploratory data analysis
3. Preprocessing (one-hot encoding, 80/20 stratified split, scaling, class weights)
4. Modeling with Logistic Regression, Random Forest and XGBoost
5. Evaluation and churn driver analysis

## Results

| Model | Accuracy | Recall | F1 | ROC-AUC |
| --- | --- | --- | --- | --- |
| **Logistic Regression** | 0.726 | **0.797** | **0.608** | **0.835** |
| Random Forest | 0.790 | 0.503 | 0.560 | 0.819 |
| XGBoost | 0.748 | 0.634 | 0.572 | 0.798 |

Logistic Regression is the best model: it catches about 80% of churners and has the highest ROC-AUC.

## Key Findings
- Customers on month-to-month contracts churn far more than those on one or two year contracts.
- Churners have much shorter tenure, with a median of about 10 months.
- Fiber optic internet is the strongest driver of churn.
- Tenure and longer contracts protect against churn.

## Charts
<img src="eda_charts%20(1).png" width="700">
<img src="churn_drivers%20(1).png" width="700">
<img src="roc_curve%20(1).png" width="500">

## Files
- `Customer_Churn_Prediction.ipynb`: full notebook with code and outputs

## Tech Stack
Python, pandas, scikit-learn, XGBoost, matplotlib, seaborn

## Dataset
[IBM Telco Customer Churn](https://github.com/IBM/telco-customer-churn-on-icp4d/tree/master/data)
