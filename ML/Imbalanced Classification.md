
## **Workflow with Imbalanced class Data**

Step 1: Use stratified train-test split to maintain class proportions
Step 2: Encode categorical variables (e.g., One-Hot Encoding, Label Encoding).
Step 3: Check the class distribution in the training set (proportions will be preserved)
Step 4: Apply  oversampling/Under Sampling  only to the training set
Step 5: Scale the data using a technique like StandardScaler or MinMaxScaler.
Step 6: Check the new class distribution after oversampling
Step 7: Train the model on the resampled training set
Step 8: Evaluate the model on the original test set

### Best Practice:

1. **Use resampling techniques OR `class_weight='balanced'`, but not both**:
    - **If you resample** the data, then you do not need to use the `class_weight='balanced'` parameter. The model is already seeing a balanced dataset.
    - **If you don't resample**, then using `class_weight='balanced'` is a good option to address the class imbalance during model training.


   **Resampling techniques**:
    - **Oversampling**: Use `SMOTE` or `RandomOverSampler` to oversample the minority class.
    - **Undersampling**: Use `RandomUnderSampler` or `TomekLinks` to undersample the majority class.
     
     ## OR 
 
   **Class weights**: Many algorithms support `class_weight='balanced'`, which automatically adjusts for imbalanced classes.

### **Evaluation Metrics for Imbalanced Data**:

- **Accuracy** is not the best metric for imbalanced data. Instead, use:
    - **Precision, Recall, F1-Score**: From `sklearn.metrics`
    - **ROC-AUC Score**: To evaluate model performance across different thresholds.
    - **Confusion Matrix**: For understanding false positives and false negatives.


`multilabel_confusion_matrix`  should be used with classification tasks, not with regression or continuous output. Both `y_true` (true labels) and `y_pred` (predicted labels) need to be **binary** or **categorical**.


`cross_val_predict()` generates **out-of-fold predictions** based on cross-validation. However, it doesn't return probabilities by default; it returns **class labels**.

`model.predict_proba(X_test)` to compute probabilities.

Need probabilities (used for ROC AUC) and the class labels for accuracy, precision, recall, and F1 score.

From`cross_val_predict`to get probabilities (for ROC AUC score),
 `method='predict_proba'` within `cross_val_predict`


### **Focus on F1 Score and ROC-AUC for Imbalanced Data**:

For imbalanced datasets, you might want to **focus more on F1 Score** and **ROC-AUC** because:

- `F1 Score` balances precision and recall, which is essential for imbalanced datasets.
- `ROC-AUC` is less affected by class imbalance and gives a broader view of model performance across different classification thresholds.