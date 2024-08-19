# Breast Cancer Detection
This repository contains a machine learning project aimed at detecting breast cancer using logistic regression. The project is structured around a Jupyter Notebook that demonstrates the data preprocessing, model training, evaluation steps.

# Project Overview

Breast cancer is one of the most common types of cancer among women worldwide. Early detection is crucial for effective treatment and can significantly increase survival rates. This project leverages machine learning techniques to build a model that can classify whether a given sample of breast tissue is malignant or benign based on various features.

# Dataset

The dataset used in this project is the Breast Cancer Wisconsin (Diagnostic)(https://www.kaggle.com/datasets/uciml/breast-cancer-wisconsin-data) Data Set. It includes 569 instances with 30 features, which are computed from a digitized image of a fine needle aspirate (FNA) of a breast mass.

# Features

Radius (mean of distances from center to points on the perimeter)

Texture (standard deviation of gray-scale values)

Perimeter

Area

Smoothness (local variation in radius lengths)

Compactness (perimeter^2 / area - 1.0)

Concavity (severity of concave portions of the contour)

Concave points (number of concave portions of the contour)

Symmetry

Fractal dimension ("coastline approximation" - 1)

The target variable is binary:

### 0: Benign

### 1: Malignant

# Steps
## 1. Data Preprocessing

### Normalization:  
The features were normalized using standard scaling to ensure that they were on a similar scale, which is crucial for the convergence of the Logistic Regression model.

### Data Splitting: 
The dataset was split into training and testing sets with a 70-30 ratio, ensuring that the model was trained on a sufficient amount of data while preserving a separate set for evaluation.

## 2. Model Training
Logistic Regression algorithm was selected as the primary model for its simplicity and effectiveness in binary classification.

## 3. Model Evaluation
The performance of the Logistic Regression model was evaluated on the test set using various metrics:

### Accuracy: 
The model achieved an accuracy of 98.24%, indicating that it correctly classified 98.24% of the instances in the test set.
### Precision: 
The precision of 97% shows the percentage of correctly identified malignant cases out of all cases predicted as malignant.
### Recall: 
The recall of 98% indicates the model's ability to correctly identify malignant cases out of all actual malignant cases.
### F1-Score: 
The F1-score, which balances precision and recall, was 98%, reflecting the overall effectiveness of the model.
### Learning Curve Analysis
The learning curve for the Logistic Regression model provides valuable insights into the model's performance as the size of the training data increases.

#### Training Score:
The training score has started very high, close to 1.0, when the model has been trained on a small subset of the data. This has indicated that the model has fit the training data extremely well. As the training set size has increased, the training score has decreased slightly, stabilizing at a high level. This slight drop has been normal and expected as the model has encountered more varied data. The consistently high training score has suggested that the model has not underfitted.

#### Cross-Validation Score:
The cross-validation score has begun at a lower value, reflecting the model's difficulty in generalizing from a small training set. As more data has been used for training, the cross-validation score has improved significantly and has eventually plateaued, indicating that the model's generalization ability has been enhanced with more data.

The narrowing gap between the training score and the cross-validation score as the training size has increased has indicated that the model has overcome initial overfitting and has achieved a good balance between bias and variance. The learning curve has suggested that the Logistic Regression model has been well-suited for this classification task, and with sufficient data, it can generalize effectively to new, unseen data.
## 4. Key Insights

### Class Imbalance: 
The model handled the class imbalance well, with only a slight bias towards the benign class, which was the majority class.
### Feature Importance: 
Logistic Regression provided coefficients that indicate the importance of each feature in predicting the target class. Features such as mean radius, texture, and perimeter had significant contributions to the model's predictions.

## 5. Conclusion
The Logistic Regression model performed well on the breast cancer detection task, providing a reliable and interpretable method for classifying tumors as malignant or benign. While there is always room for improvement, especially in handling borderline cases, the model's results are promising for aiding in early detection and diagnosis.
