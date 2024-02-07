# Credit-Risk-Classification

## Overview of the Analysis

The purpose of this analysis was to apply machine learning techniques to predict the creditworthiness of borrowers using borrower data. The primary goal was to classify loans into two categories: "healthy" (0) and "high-risk" (1), based on various borrower-related attributes.

The dataset comprised several features related to borrowers' financial information, including `loan_size`, `interest_rate`, `borrower_income`, `debt_to_income`, `num_of_accounts`, `derogatory_marks`, and `total_debt`. The target variable was `loan_status`, which indicates whether a loan is healthy or has a high risk, with 0 for healthy loans and 1 for high-risk loans.

## The analysis followed these key stages:

### Data Preparation
- Reading the dataset, splitting it into features (X) and the target label (y), and then further splitting into training and testing sets. The default split ratio is approximately 75% of the data for training and 25% for testing when using the `train_test_split` function to split the dataset.

### Model Training
- Using the Logistic Regression model to train on the training data.

### Model Evaluation
- Evaluating model performance with a confusion matrix and classification report to assess accuracy, precision, recall, and F1-score.

For this challenge, the primary machine learning method used was `LogisticRegression` due to its effectiveness in binary classification problems.

## Results

The confusion matrix is as follows:

| Actual\Predicted | Healthy Loan | High Risk Loan |
|------------------|--------------|----------------|
| Healthy Loan     | 18663        | 102            |
| High Risk Loan   | 56           | 563            |





This means that the logistic regression model:
- Correctly predicted a loan as healthy 18,663 times when it was indeed a healthy loan in reality.
- Incorrectly predicted a loan as high risk 102 times when, in fact, it was a healthy loan.
- Mistakenly predicted a loan as healthy on 56 occasions when it was actually a high-risk loan.
- Accurately identified a loan as high risk 563 times, confirming its ability to correctly classify high-risk loans.

### Classification Report:
- **Accuracy = 99%**

#### Healthy Loan (0)
- **Precision = 100%**
- **Recall = 99%**
- **F1-Score = 1.00**

#### High Risk Loan (1)
- **Precision = 85%**
- **Recall = 91%**
- **F1-Score = 0.88**

## Summary

The model accuracy is 99%, indicating a very high level of correctness in its predictions, showcasing its effectiveness.

### About Healthy Loans:
- The precision is perfect, meaning when the model predicts a loan as healthy, it is correct every time.
- The recall is 99%, indicating it captures the vast majority of healthy loans, missing very few.

### About High Risk Loans:
- The precision is 85%, indicating that when a loan is predicted as high risk, it is accurate 85% of the time, with a 15% chance of being incorrect.
- The recall of 91% shows the model is quite effective at identifying high-risk loans, though there is a small chance of missing some.

The model performs excellently in predicting healthy loans and well in identifying high-risk loans, though there is room for improvement in the precision of high-risk loan predictions. Further model refinement could focus on enhancing the accuracy of high-risk loan predictions to achieve even better performance.
