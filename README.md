# Predicting-survival-rates-in-critically-ill-patients-
This project focuses on creating a machine learning model to **predict whether critically ill patients will survive or pass away** within a specified timeframe. [cite_start]Accurate predictions are vital for modern healthcare, as they influence clinical decisions, improve patient quality of life, and optimize resource allocation[cite: 7, 8].

[cite_start]The goal is to facilitate decision-making and planning processes to minimize instances of prolonged suffering during end-of-life stages[cite: 13].

## Dataset

[cite_start]The model was built using a dataset comprising **9105 records of critically ill patients** from five medical centers in the United States, collected between 1989–1991 and 1992–1994[cite: 10]. [cite_start]Each record represents a hospitalized patient who met criteria related to nine disease categories, including acute respiratory failure, liver disease, and various forms of cancer and organ system failure[cite: 10]. [cite_start]The features include **physiologic, demographics, and disease severity information**[cite: 11].

## Methodology

### 1. Data Preprocessing

Data preprocessing was crucial for handling a large amount of missing values and preparing the features for modeling.

* **Missing Value Imputation:**
    * [cite_start]**Numerical features** were imputed using the **K-Nearest Neighbors (KNN) imputer** for more accurate estimation based on similarity between data points[cite: 32, 34].
    * [cite_start]**Categorical features** were imputed using the **most frequent category**[cite: 35].
* [cite_start]**Categorical Encoding:** Categorical features were converted into numerical format using **one-hot encoding**[cite: 38].
* [cite_start]**Feature Scaling:** Numerical features were scaled using **StandardScaler** to ensure they have a mean of 0 and a standard deviation of 1, preventing features with larger ranges from dominating the training process[cite: 43, 44].

[cite_start]A **Column Transformer** and **Pipeline** from `scikit-learn` were used to implement these steps[cite: 30, 64].

### 2. Model Building and Hyperparameter Tuning

The problem was framed as a binary classification task. [cite_start]Multiple ensemble methods were employed and evaluated using the **F1 score**, a metric suitable for imbalanced datasets[cite: 50, 52, 69].

The final optimized model used a **Voting Classifier** to combine predictions from two powerful models:

1.  [cite_start]**Random Forest Classifier** [cite: 53]
2.  [cite_start]**Gradient Boosting Classifier** [cite: 55]

[cite_start]**Hyperparameter tuning** was performed using **GridSearchCV** to optimize parameters like the number of estimators and maximum tree depth, leading to improved model performance[cite: 61, 62, 70].

## Results

The models were evaluated on the test set, and the best hyperparameters were selected. The evaluation metric used was the **F1 Score**:


***

This draft provides a good summary of your work. Do you have any code files or specific visualizations you would like to highlight or link to in the "How to Run" section?
