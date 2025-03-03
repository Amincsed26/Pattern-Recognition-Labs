# Heart Failure Classification

## Problem Statement
Heart failure is a critical condition often caused by cardiovascular diseases (CVDs). Early prediction of heart failure can aid in timely medical intervention and improve patient outcomes. This project involves implementing classification models to predict heart failure based on clinical features.

## Dataset
We use the Heart Failure Prediction dataset from Kaggle, which consists of 918 samples, 11 features, and a binary classification label indicating the occurrence of heart failure.
[Download the dataset from Kaggle](https://www.kaggle.com/datasets/fedesoriano/heart-failure-prediction)

## Data Preparation
- **Fixed Random Seed**: We use a fixed seed (42) for reproducibility.
- **Train/Validation/Test Split**: The dataset is split into:
  - 70% training
  - 10% validation
  - 20% testing
  - Stratified splitting is used to maintain class balance.
- **Feature Preprocessing**:
  - Normalize or standardize features where necessary (especially for distance-based models like KNN and Neural Networks).
  - Encode categorical variables (if any) using one-hot encoding.

## Implementation Details
We implement three classification models from scratch:

### 1. Decision Tree Classifier
- Uses **Information Gain** for splitting nodes.
- Implements a recursive tree structure.
- Includes stopping criteria such as **max depth** and **minimum samples split** to prevent overfitting.

### 2. Bagging Ensemble
- Implements **Bootstrap Aggregating (Bagging)**.
- Trains multiple Decision Trees on bootstrap samples.
- Uses majority voting for final classification.

### 3. AdaBoost Classifier
- Sequentially trains weak learners (Decision Stumps/Small Decision Trees).
- Adjusts sample weights to focus on misclassified instances.
- Uses weighted voting for final predictions.

## Evaluation
Each model is evaluated using:
- **Accuracy**
- **F1-Score**
- **Confusion Matrix**

## Analysis & Comparison
- Compare Decision Tree vs. Ensemble methods (Bagging & AdaBoost).
- Identify strengths and weaknesses of each model.
- Analyze misclassification patterns using confusion matrices.

## Bonus Implementations
- **K-Nearest Neighbors (KNN)**
- **Logistic Regression**
- **Feedforward Neural Network (FNN) using PyTorch/Keras**

## Submission
- Python script or Jupyter Notebook.
- Well-documented report (Latex preferred).
- Ensure reproducibility by setting random seeds and structuring code properly.
