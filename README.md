# Smart Outcome Predictor – Supervised Learning Project

## Project Overview

The **Smart Outcome Predictor** is a supervised machine learning project that uses student learning data to predict academic outcomes.

The project applies different ensemble learning techniques to improve prediction performance. It includes classification and regression tasks to understand how machine learning models can be used to analyze student performance.

## Objectives

The main objectives of this project are:

- To understand and apply ensemble learning techniques.
- To predict student course completion status using classification models.
- To predict students' final scores using regression models.
- To compare Bagging, Boosting, Voting, and Stacking approaches.
- To evaluate model performance using suitable metrics.
- To identify the best-performing model for the given dataset.

## Dataset Description

The dataset contains approximately **5,200 student records** with information related to course participation, learning activity, and academic performance.

### Target Variables

| Target Variable | Task | Description |
|---|---|---|
| `completion_status` | Classification | Predicts whether a student completes the course. |
| `final_score` | Regression | Predicts the student's final score. |

The `student_id` column is used as an identifier and is not included as a predictive feature.

## Technologies Used

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- LightGBM
- XGBoost

## Project Workflow

### 1. Data Loading and Understanding

- Load the dataset using Pandas.
- Inspect the dataset using `head()`, `info()`, and `describe()`.
- Identify missing values and duplicate records.
- Understand the dataset's features and target variables.

### 2. Data Preprocessing

- Remove duplicate records.
- Handle missing numerical and categorical values.
- Remove the identifier column.
- Convert the course start date into useful features such as month and day.
- Apply scaling to numerical features.
- Apply one-hot encoding to categorical features.

### 3. Train-Test Split

The dataset is divided into training and testing sets.

- Training data: 80%
- Testing data: 20%

The training dataset is used to build the models, while the testing dataset is used to evaluate their performance.

### 4. Ensemble Learning Techniques

The project explores the following ensemble learning methods:

#### Bagging

Bagging, or Bootstrap Aggregating, trains multiple models on different samples of the training data and combines their predictions.

Models explored:
- Bagging Classifier
- Bagging Regressor

#### Boosting

Boosting builds models sequentially, where each new model attempts to improve upon the errors of previous models.

Models explored:
- AdaBoost Classifier
- AdaBoost Regressor
- Gradient Boosting Classifier
- Gradient Boosting Regressor
- LightGBM Classifier and Regressor
- XGBoost Classifier and Regressor

#### Voting and Stacking

Voting combines predictions from multiple models to produce a final prediction.

Stacking uses predictions from multiple base models as input to another model, called a meta-model.

These techniques are explored to compare their performance with other ensemble methods.

## Model Evaluation

### Classification Metrics

The classification models are evaluated using:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### Regression Metrics

The regression models are evaluated using:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

For regression, lower MAE and RMSE values indicate better performance, while a higher R² score indicates better explanatory performance.

## Results and Comparison

Different ensemble learning models are compared using their evaluation metrics.

The comparison helps identify which model performs better for:

- Predicting course completion status.
- Predicting students' final scores.

The final best model is selected based on the evaluation results obtained in the notebook.

## Conclusion

This project demonstrates how supervised machine learning and ensemble learning techniques can be used to predict student academic outcomes.

Both classification and regression approaches are applied to the dataset. Different ensemble methods are trained and evaluated, and their results are compared using appropriate performance metrics.

The project provides practical experience in data preprocessing, model training, evaluation, and comparison. It also helps in understanding how ensemble learning techniques can improve predictive performance.

The best-performing model is determined based on the final model comparison results.

## How to Run the Project

1. Download or clone this repository.
2. Make sure Python and Jupyter Notebook are installed.
3. Install the required libraries:

   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn lightgbm xgboost
   ```

4. Place the dataset in the project folder.
5. Open Jupyter Notebook.
6. Open the project notebook.
7. Run all cells from top to bottom.

## Project Files

```text
Smart-Outcome-Predictor/
│
├── Smart_Outcome_Predictor.ipynb
├── Smart_Outcome_Predictor_Dataset_5200.csv
├── README.md
└── requirements.txt
```
