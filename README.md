# FUTURE_ML_02
Bank Customer Churn Prediction Project
Overview
This project uses machine learning to predict which bank customers are at risk of churning. The pipeline involves comprehensive data preparation, rigorous model development, insightful evaluation, and business-focused dashboard visualization. All code and analysis are implemented in Python, with results presented in Power BI.

Detailed Project Steps
1. Data Loading and Cleaning
Loaded the bank churn dataset from CSV.

Inspected and cleaned missing values and irrelevant fields.

Performed label encoding and one-hot encoding on categorical features.

2. Feature and Target Preparation
Separated input features from target churn columns (e.g., Actual, Actual_Binary).

Excluded prediction-relevant columns from analysis features.

3. Train-Test Split and Imbalance Handling
Performed stratified train-test split to maintain churn class balance.

Utilized SMOTE to address class imbalance in training data.

4. Model Building & Training
Trained an XGBoost classifier with optimized hyperparameters (using RandomizedSearchCV).

Trained a Random Forest classifier for model comparison and feature importance analysis.

5. Prediction and Results Export
Generated churn probabilities and both default and optimal threshold predictions.

Exported results containing actual churn status, predicted labels, probabilities, and important features to bank_churn_results_final.csv.

6. Model Evaluation
Evaluated models using metrics: accuracy, precision, recall, F1-score, and ROC-AUC.

Generated and visualized confusion matrices, ROC curves, precision-recall curves, and classification reports.

7. Threshold Optimization
Calculated precision and recall at varying probability thresholds.

Optimized threshold for maximum F1-score and regenerated predictions at this threshold.

Re-evaluated and visualized model performance at the new threshold.

8. Error Analysis
Identified false positives (customers predicted to churn but didn't) and false negatives (customers not predicted to churn but did).

Explored samples to understand prediction errors and business impact.

9. Feature Importance Analysis
Visualized key driving features using importance scores from both XGBoost and Random Forest models.

10. Visualization and Dashboard Development
Created distribution plots (e.g., churn probability histogram), actual vs predicted churn counts, and confusion matrix heatmaps in Matplotlib/Seaborn.

Built an interactive Power BI dashboard, featuring:

KPI cards for total, actual, predicted churn counts.

Slicers for filtering churn status.

Histograms and bar charts to compare churn probabilities and counts.

Visualization of feature importances if exported.

How to Run
Python Script / Notebook

Clone this repository or download notebook/script.

Install required libraries:

text
pip install pandas scikit-learn xgboost imbalanced-learn matplotlib seaborn
Execute Python code to generate bank_churn_results_final.csv.

Power BI Dashboard

Open Power BI Desktop.

Import bank_churn_results_final.csv.

Build visuals as guided above, or use the provided dashboard template if available.

Project Structure
text
├── data/
│   └── bank_churn_results_final.csv
├── churn_modeling.ipynb
├── churn_dashboard.py 
├── visuals/
│   └── *.png (matplotlib charts)
└── README.md
Results
Model achieved high predictive accuracy and recall for churn detection

Feature importance analysis highlighted key customer attributes

License
This project is open for academic, learning, and professional demonstration purposes.

Contact:
For queries or collaborations, reach out via GitHub Issues or LinkedIn.
