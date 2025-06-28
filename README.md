# Campus Placement Prediction Using ML Classifiers

## Objective

This project uses the Kaggle competition dataset from the "ML with Python Course Project" to predict campus recruitment outcomes. It includes preprocessing, EDA, feature engineering, and model training using classification algorithms such as Logistic Regression, Decision Tree, and K-Nearest Neighbors.

## Dataset

- Source: Kaggle – Campus Recruitment Dataset by Rashid Minhas (2020)
- Size: 215 records
- Target Variable: `status` (Placed / Not Placed)

Key features include:
- Academic scores: `ssc_p`, `hsc_p`, `degree_p`, `mba_p`
- Categorical attributes: `gender`, `ssc_b`, `hsc_b`, `hsc_s`, `degree_t`, `workex`, `specialisation`
- Test scores: `etest_p`
- Outcome: `status`, with optional `salary` for placed students

## Approach

1. Exploratory Data Analysis (EDA):
   - Checked feature distributions, missing values, and data types
   - Analyzed target imbalance and correlation with predictors

2. Preprocessing:
   - Encoded categorical variables
   - Split into train/test sets
   - Scaled numeric features post-split to avoid leakage

3. Model Training:
   Six classifiers were trained with balanced class weights where needed:
   - Logistic Regression
   - Decision Tree Classifier
   - Random Forest Classifier
   - Support Vector Machine (SVM)
   - K-Nearest Neighbors (KNN)
   - XGBoost Classifier

4. Model Evaluation:
   - Evaluated with Accuracy, Precision, Recall, and F1-Score
   - Cross-validation was applied
   - Confusion matrices and classification reports used for comparison

## Results

- All models performed decently, with ensemble models (Random Forest, XGBoost) outperforming linear ones.
- XGBoost and SVM achieved strong balance between precision and recall.
- Feature importance analysis showed `mba_p`, `etest_p`, and `degree_p` as influential predictors.

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/chawthinn/campus-placement-prediction.git
   cd campus-placement-prediction
   ```

2. Open the notebook in Jupyter or run on Kaggle.

3. Dataset is already embedded in the Kaggle competition environment:
   ```
   /kaggle/input/ml-with-python-course-project/
   ```

## Tech Stack

- Python 3.10+
- Pandas
- Scikit-learn
- XGBoost
- Seaborn
- Matplotlib
- Jupyter Notebook
