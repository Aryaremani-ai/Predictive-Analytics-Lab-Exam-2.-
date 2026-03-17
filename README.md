# Predictive Analytics Lab Exam-2

## Project Overview

This project is developed as part of a predictive analytics lab exam focusing on a **binary classification task**. The objective is to analyze the dataset, build classification models, visualize decision boundaries, and evaluate model performance.

---

## Dataset Description

* Total Records: **1020**
* Features:

  * **Feature1** (continuous)
  * **Feature2** (continuous)
* Target Variable:

  * **Target (Yes/No)** → converted to (1/0)

---

## Exploratory Data Analysis (EDA)

* Checked dataset structure using `.info()` and `.describe()`
* Identified **20 missing values** in target → removed
* Detected **class imbalance** (more "No" than "Yes")
* Found **outliers in Feature1** → removed for better model performance
* Visualized:

  * Class distribution
  * Feature relationships using scatter plot

---

##  Data Preprocessing

* Removed missing values from target column
* Removed extreme outliers
* Converted categorical target into numerical format (Yes → 1, No → 0)
* Selected relevant features for model training

---

## Models Used

### 1. Logistic Regression

* Initially used for classification
* Performance was poor due to class imbalance
* Failed to predict minority class effectively

### 2. Decision Tree (Final Model)

* Handles **non-linear relationships**
* Works better with **imbalanced data**
* Applied `class_weight='balanced'` to improve performance

---

## Decision Boundary

* Plotted using Feature1 and Feature2
* Decision Tree creates **non-linear, rectangular regions**
* Clearly shows separation between classes

---

##  Model Evaluation

### Logistic Regression (Initial Model)

* Accuracy: ~77%
* Failed to classify minority class (Yes)

### Decision Tree (Final Model)

* Accuracy: **93%**
* Confusion Matrix:

  ```
  [[144  14]
   [  0  42]]
  ```
* Key Observations:

  * Successfully identified all "Yes" instances (Recall = 1.00)
  * Balanced performance across classes
  * Significant improvement over Logistic Regression

---

## Key Insights

* Accuracy alone can be misleading in imbalanced datasets
* Decision Tree performs better for this dataset due to:

  * Non-linear decision boundaries
  * Better handling of minority class
* Class imbalance must be addressed for reliable predictions

---

##  Tools & Libraries

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

---

##  How to Run

1. Install dependencies:

   ```
   pip install -r requirements.txt
   ```

2. Run the model:

   ```
   python model.py
   ```

## 📌Conclusion

The Decision Tree model significantly improved classification performance compared to Logistic Regression. It effectively handled class imbalance and captured complex patterns in the dataset, resulting in higher accuracy and better detection of the minority class.

