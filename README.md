# Spaceship Titanic Prediction - Kaggle Competition

This project contains a solution for the [Spaceship Titanic competition](https://www.kaggle.com/competitions/spaceship-titanic) on Kaggle.

## Main Objective
The goal of this competition was to predict whether a passenger was transported to an alternate dimension during the **Spaceship Titanic's** collision with a spacetime anomaly.

## Steps of the Data Science Process:

1. Understand the Original Data
2. Data Cleaning
3. Data Exploration
4. Feature Engineering
5. Model Selection and Training
6. Model Evaluation
7. Submission File

## Data

- **train.csv**: Personal records for ~8700 passengers (used for training). Includes:
  - `PassengerId`: Unique identifier for each passenger.
  - `HomePlanet`: The planet the passenger is from.
  - `CryoSleep`: Whether the passenger was in cryosleep during the voyage.
  - `Cabin`: The cabin number where the passenger is staying.
  - `Destination`: The planet the passenger will be debarking to.
  - `Age`: The age of the passenger.
  - `VIP`: Whether the passenger paid for VIP service.
  - `RoomService`, `FoodCourt`, `ShoppingMall`, `Spa`, `VRDeck`: Amount spent on luxury amenities.
  - `Name`: First and last name of the passenger.
  - `Transported`: Whether the passenger was transported to another dimension (target column).

- **test.csv**: Personal records for ~4300 passengers (used for testing).
  - Contains similar columns as `train.csv`, but no `Transported` column.

- **sample_submission.csv**: The submission file format. Includes:
  - `PassengerId`: Unique identifier for each passenger in the test set.
  - `Transported`: Predicted value for whether the passenger was transported to another dimension (True/False).

## Kaggle Notebook

Check out my notebook for the project on Kaggle: [Spaceship Titanic Notebook](https://www.kaggle.com/code/laurasaraiva/spaceship-titanic/notebook)

## Approach

1. **Data Preprocessing**:
   - Handled missing values and encoded categorical features.
   - Normalized numerical features using **StandardScaler**.

2. **Modeling**:
   - Experimented with different models like **Gradient Boosting** and **Neural Networks**.
   - Used **GridSearchCV** for hyperparameter tuning to optimize model performance.

3. **Evaluation**:
   - Performance metrics: **Accuracy**, **Log Loss**, **ROC-AUC**, **Precision**, **Recall**, **F1-score**.
   - Final results:
     - **Accuracy**: 0.79
     - **Log Loss**: 0.4145
     - **F1-Score**: 0.7989