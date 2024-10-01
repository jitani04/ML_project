
# README

## Overview
This project demonstrates a binary classification task, predicting whether an individual is likely to be a homeowner based on various features like income, age, and workclass. The notebook carries out the following steps:

1. **Data Preparation:** Creation of features and labels for the machine learning model.
2. **Model Training & Evaluation:** Use of Logistic Regression and Random Forest models to train and evaluate the data.
3. **Model Optimization:** Application of techniques such as Grid Search for hyperparameter tuning to optimize the performance of the Logistic Regression model.
4. **Comparison & Analysis:** Visualization of performance metrics using precision-recall and ROC curves, followed by feature importance analysis using Random Forest.

## Key Components

### 1. Data Preparation
- A new binary label, `homeowner`, was created based on the combination of income, age, and workclass features.
- The dataset is split into training and testing sets.
  
### 2. Model Training & Evaluation
- **Logistic Regression:** 
  - A default Logistic Regression model was trained and evaluated.
  - Metrics such as accuracy, log loss, and confusion matrix were computed to assess the model’s performance.
  
- **Random Forest Classifier:** 
  - A Random Forest model was trained and evaluated.
  - Accuracy and log loss were also computed for comparison with the Logistic Regression model.

### 3. Model Optimization
- **Grid Search with Cross-Validation:** 
  - Hyperparameter tuning was performed on the Logistic Regression model using `GridSearchCV` to identify the best regularization parameter `C`.
  
- **Feature Selection & Regularization:**
  - The best Logistic Regression model was selected based on cross-validation performance.
  
### 4. Model Comparison & Visualization
- **Precision-Recall Curve & ROC Curve:** 
  - Plots of precision-recall and ROC curves were created to visually compare the performance of the default and optimized Logistic Regression models.
  
- **Feature Importance:**
  - For the Random Forest model, feature importance was plotted to highlight the impact of different features on the prediction.

## Performance Metrics
- **Logistic Regression:**
  - Default Model Accuracy: 84.14%
  - Log Loss: 0.3754
  - Optimized Model Accuracy: Same as default
  - Precision-Recall and ROC curves show similar performance.
  
- **Random Forest Classifier:**
  - Accuracy: 89.10%
  - Log Loss: 0.4420
  - The Random Forest model showed a slight improvement in accuracy compared to Logistic Regression.

## Results Summary
- The Logistic Regression model, while simpler and optimized via grid search, did not show a significant performance improvement over the default configuration.
- The Random Forest model achieved higher accuracy, though with a higher log loss, indicating a tradeoff between complexity and interpretability.

## How to Run
1. Ensure all necessary libraries are installed, such as `sklearn`, `pandas`, `numpy`, `matplotlib`, and `seaborn`.
2. Load the dataset, and ensure it has all the necessary features.
3. Run the cells sequentially, which will split the data, train the models, perform optimization, and generate visualizations.
