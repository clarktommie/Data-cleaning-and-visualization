# Salary Prediction Model Analysis

## Overview
This project aims to build a predictive model for estimating total yearly compensation based on various features such as stock grant value, years of experience, bonus, job title, location, and education level. The goal is to predict salary (total yearly compensation) using different machine learning techniques. 

The dataset includes information about employees' compensation, roles, and qualifications, and the primary target variable is the salary (total yearly compensation). Several machine learning models were used to predict this variable and analyze the relationship between features and compensation.

## Data Overview
The dataset contains the following features:
- **totalyearlycompensation**: Target variable (salary). 
- **stockgrantvalue**: Stock grant value.
- **yearsofexperience**: Number of years of experience.
- **bonus**: Bonus received.
- **job title**: Various titles such as Product Designer, Software Engineer, etc.
- **education**: Education level (e.g., Bachelor's, Master's, or PhD).
- **location**: Geographical location (e.g., New York, San Francisco).

## Data Preprocessing
Several preprocessing steps were taken to prepare the dataset:
- **Categorical features**: One-hot encoding was applied to categorical features like job title and location.
- **Null values**: Missing values were handled appropriately.
- **Multicollinearity**: Features with high multicollinearity were identified and reduced to avoid overfitting.

## Feature Selection
To enhance model performance and reduce complexity, feature selection methods were applied:
- **Variance Threshold**: Removed features with low variance.
- **Correlation Analysis**: Removed features highly correlated with each other.
- **Statistical Tests (SelectKBest)**: Selected the most relevant features based on statistical significance.
- **Forward Selection**: Used linear regression to add features sequentially.
- **Recursive Feature Elimination (RFE)**: Eliminated non-important features using a decision tree regressor.

  ![image](https://github.com/user-attachments/assets/c1ef3d37-99e7-4475-a005-a656ca1cca21)

## Correlation Analysis
A correlation matrix was generated to examine relationships between features and the target variable. Key observations include:
- Stock grant value and total yearly compensation had a strong positive correlation (0.87).
- Years of experience showed a moderate positive correlation (0.43) with total yearly compensation.
- Job titles such as Software Engineering Manager and Technical Program Manager had moderate correlations with total compensation.

  ![image](https://github.com/user-attachments/assets/0d6189d5-b18d-4f95-ac5d-6a2d56c1688d)

## Model Development
Multiple machine learning models were developed to predict total yearly compensation. The models were evaluated using metrics such as R-squared (R²), Mean Squared Error (MSE), and Root Mean Squared Error (RMSE).

### 1. OLS (Ordinary Least Squares) Regression
- **R-squared (R²)**: 0.912, indicating that the model explains 91.2% of the variance in total yearly compensation.
- **Significant predictors**: Stock grant value, years of experience, bonus, and location.
- **P-values**: Most features had p-values below 0.05, suggesting they are statistically significant.

### 2. Lasso Regression
- **R²**: 0.9015, indicating good predictive accuracy.
- **MSE**: 334,948,969, showing the error between predicted and actual values.
- **Impactful features**: Stock grant value, years of experience, and bonus were the most important features.

## Model Evaluation
The performance of the models was assessed using both training and test datasets:
- **Training R²**: 0.9144, indicating excellent fit to the training data.
- **Test R²**: 0.9015, showing strong generalization to new data.
- **Training MSE**: 270,059,102, the error when predicting on training data.
- **Test MSE**: 334,953,490, indicating a slight increase in error when applied to unseen data.

These results suggest that the model performs robustly but may slightly overfit the training data, as seen from the gap between training and test performance.

## Conclusion
- The predictive model for total yearly compensation performs well with an R² of 0.91.
- Key predictors include stock grant value, years of experience, and bonus.
- The model could be further improved by addressing slight overfitting, potentially through more advanced regularization techniques or feature engineering.

## Key Skills and Techniques Demonstrated:
- Data preprocessing and feature engineering.
- Feature selection and dimensionality reduction.
- Application of statistical tests and machine learning models (OLS, Lasso).
- Model performance evaluation using R², MSE, and RMSE.

This project demonstrates my ability to build, evaluate, and refine predictive models, leveraging modern machine learning techniques. The insights gained can be valuable for HR departments and financial analysts when determining fair compensation based on employee characteristics.
