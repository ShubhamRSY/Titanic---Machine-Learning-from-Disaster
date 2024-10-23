# Titanic - Machine Learning from Disaster

This repository contains my work on the **Titanic: Machine Learning from Disaster** competition hosted on Kaggle. The objective of this project is to predict passenger survival based on demographic and socio-economic features.

This challenge serves as an introduction to classification problems, allowing me to apply a variety of machine learning algorithms while gaining familiarity with the Kaggle platform. The dataset is derived from actual Titanic passenger data, and the challenge is to build models that can predict survival outcomes based on features such as gender, age, class, and fare.

## Problem Statement

The competition revolves around binary classification: predicting whether a passenger survived or not (0 = No, 1 = Yes). The challenge is to create a predictive model using the training dataset, which contains both features and corresponding survival labels. The model is then tested on an unseen dataset for which the survival outcome is unknown.

## Dataset Overview

The dataset is split into the following files:

- **train.csv**: Contains features and survival outcomes (ground truth) for each passenger. This is used to train the models.
- **test.csv**: Contains features without the survival outcomes. This is used to evaluate the model’s predictions.
- **gender_submission.csv**: A simple baseline model that predicts all female passengers survived, provided as an example of the submission format.

## Data Dictionary

| Feature   | Description                                           | Key                               |
|-----------|-------------------------------------------------------|-----------------------------------|
| survival  | Survival (dependent variable)                         | 0 = No, 1 = Yes                  |
| pclass    | Passenger class (proxy for socio-economic status)      | 1 = 1st, 2 = 2nd, 3 = 3rd         |
| sex       | Gender of the passenger                               | Male, Female                     |
| age       | Age in years (fractional for children)                | Continuous                       |
| sibsp     | Number of siblings/spouses aboard                     | Integer                          |
| parch     | Number of parents/children aboard                     | Integer                          |
| fare      | Passenger fare                                        | Continuous                       |
| cabin     | Cabin number                                          | Categorical                      |
| embarked  | Port of embarkation                                   | C = Cherbourg, Q = Queenstown, S = Southampton |

## Model Implementation

I developed two models using common machine learning algorithms:

- **Perceptron**: A binary classification algorithm that updates its weights iteratively during training. This is a straightforward linear classifier and an efficient starting point for binary classification.
- **Linear Regression**: Although primarily used for regression tasks, I implemented a linear regression model here to predict survival probabilities. The continuous output was later thresholded to classify survival (0 or 1).

## Model Performance

After training and evaluating these models, I submitted the results to Kaggle and achieved the following accuracy scores:

- **Perceptron**: 76.55%
- **Linear Regression**: 75.60%

These models provide a solid foundation, but there is room for improvement, particularly through feature engineering and by exploring more advanced algorithms.

## Future Work

I am actively exploring additional machine learning models and techniques to enhance performance, including:

- **Random Forests**: For handling non-linearity and complex feature interactions.
- **Support Vector Machines (SVM)**: For potential improvements in decision boundary classification.
- **Gradient Boosting**: To capture complex patterns and improve prediction accuracy.
- **Feature Engineering**: To create new features that may improve the predictive power of the model (e.g., combining family size, fare bands, etc.).

## Repository Structure

- **msbapm_Fall2024_lr.csv**: Linear regression model outputs.
- **msbapm_Fall2024_ppm.csv**: Perceptron model outputs.
- **train.csv**: Training dataset.
- **test.csv**: Test dataset (unseen labels for evaluation).
- **gender_submission.csv**: Example submission file.

## Conclusion

This project demonstrates my initial steps into machine learning on a well-known dataset. Moving forward, I plan to refine these models, apply advanced techniques, and explore model interpretability to better understand the features contributing to survival predictions. As a data scientist, I am continuously seeking ways to improve model performance through data-driven insights and experimentation.
