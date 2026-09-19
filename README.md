# Breast Cancer Classification

A machine learning project for classifying breast cancer samples as **Benign (B)** or **Malignant (M)** using numerical features from the Wisconsin Diagnostic Breast Cancer dataset.

## Project Overview

The goal of this project is to build and evaluate machine learning classification models that can learn patterns from breast-cell nucleus measurements and classify samples into two categories:

- **B** — Benign
- **M** — Malignant

This project covers the complete machine learning workflow, from data exploration and preprocessing to model training, tuning, evaluation, and prediction.

## Dataset

The dataset contains:

- **569 samples**
- **30 numerical features**
- **1 target variable:** `diagnosis`
- 357 benign samples
- 212 malignant samples

The original dataset also contained an `id` column and an empty `Unnamed: 32` column, which were removed during preprocessing.

## Machine Learning Models

Four classification algorithms were explored:

- Logistic Regression
- Decision Tree
- K-Nearest Neighbors (KNN)
- Support Vector Machine (SVM)

The data was split into training and testing sets using an 80/20 split with stratification.

Feature scaling was applied where appropriate, particularly for Logistic Regression, KNN, and SVM.

## Model Tuning

The models were also tested with selected hyperparameter changes.

The tuned Logistic Regression model achieved:

- **Test Accuracy: 98.25%**
- **Malignant Recall: 95%**
- **Malignant F1-score: 98%**
- **False Negatives: 2**

The final confusion matrix was:

| | Predicted B | Predicted M |
|---|---:|---:|
| Actual B | 72 | 0 |
| Actual M | 2 | 40 |

## Prediction Example

The final model was tested on a sample from the test set.

**Predicted:** B (Benign)  
**Actual:** B (Benign)

The model's predicted probabilities for this sample were approximately:

- Benign: 99.43%
- Malignant: 0.47%

## Model Saving

The final Logistic Regression model and the StandardScaler were saved using Joblib so they can be loaded and reused without retraining.

## Tools & Libraries

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## Project File

The complete step-by-step implementation is available in:

`BreastCancer_prediction.ipynb`

## Disclaimer

This project is an educational machine learning project. The results are based on the dataset and test split used in this notebook and should not be considered a substitute for clinical diagnosis or medical validation.
