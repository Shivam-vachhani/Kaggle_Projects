Best Model : XGBoost (scale_pos_weight)
ROC-AUC   : 0.822
Recall    : 0.73 (catches 73% of churners)
Key Features: MonthlyCharges, Tenure, Contract Type

Lesson learned: SMOTE helps linear models but hurts
tree-based models — use scale_pos_weight for XGBoost