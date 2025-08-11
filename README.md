# Heart Disease Prediction using Decision Tree & Random Forest

## Overview

This project applies **Decision Tree** and **Random Forest** classification models to predict heart disease presence based on patient health data. It demonstrates data preprocessing, hyperparameter tuning, model evaluation, and visualization techniques to compare model performances.

---

## Dataset

* **Source**: `heart.csv`
* **Target Variable**: `target` (0 = No Disease, 1 = Disease)
* **Features**: Various patient attributes such as age, sex, cholesterol levels, blood pressure, etc.
* **Cleaning Step**: Removed duplicate rows.

---

## Project Workflow

### 1. Data Preprocessing

* Dropped duplicates from the dataset.
* Separated features (`X`) and target (`y`).
* Performed an 80-20 train-test split with **stratification**.

### 2. Cross-Validation Setup

* Used **Stratified K-Fold** (10 splits) to maintain class distribution across folds.

### 3. Model Training & Hyperparameter Tuning

* **Decision Tree Classifier**:

  * Parameters tuned: `criterion`, `max_depth`, `min_samples_split`, `min_samples_leaf`
* **Random Forest Classifier**:

  * Parameters tuned: `n_estimators`, `max_depth`, `min_samples_split`, `min_samples_leaf`, `criterion`
* **GridSearchCV** used with `roc_auc` as the scoring metric.

### 4. Model Evaluation

* **Metrics**:

  * Classification Report (Precision, Recall, F1-score)
  * ROC-AUC Score
  * Precision-Recall AUC
* **Plots**:

  * ROC Curve
  * Precision-Recall Curve

### 5. Model Visualization

* **Decision Tree Plot**: Graphical representation of the best Decision Tree.
* **Feature Importance**: Bar charts showing the most influential features for both models.

### 6. Learning Curves

* Plotted **Learning Curves** for both models to assess bias-variance tradeoff.

### 7. Model Comparison

* **Cross-Validation Accuracy** compared using boxplots.
* Printed mean and standard deviation of accuracy for both models.

---

## Key Insights

* **Random Forest** generally achieved higher and more stable performance compared to a single Decision Tree.
* Feature importance analysis reveals which patient attributes are most predictive of heart disease.
* Learning curves show the effect of training size on performance.

---

## Visualizations Included

* ROC & Precision-Recall Curves
* Decision Tree Diagram
* Feature Importances
* Learning Curves
* Model Performance Boxplot

---

## How to Run

1. Place `heart.csv` in the same directory as `Task-5.ipynb`.
2. Run all cells in the notebook.
3. Check printed metrics and plots.

---

## Conclusion

This project demonstrates a comprehensive supervised learning workflow for classification tasks, encompassing data preparation, model training, evaluation, and comparison. Random Forest outperformed Decision Tree in this case, offering better generalization and robustness.

---

## Author

Jenish Allen Immanuel J 💙
