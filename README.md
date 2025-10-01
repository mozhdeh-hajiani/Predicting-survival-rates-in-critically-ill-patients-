# Predicting-survival-rates-in-critically-ill-patients-
This project focuses on creating a machine learning model to **predict whether critically ill patients will survive or pass away** within a specified timeframe. Accurate predictions are vital for modern healthcare, as they influence clinical decisions, improve patient quality of life, and optimize resource allocation.

The goal is to facilitate decision-making and planning processes to minimize instances of prolonged suffering during end-of-life stages.

## Dataset

The model was built using a dataset comprising **9105 records of critically ill patients** from five medical centers in the United States, collected between 1989–1991 and 1992–1994. Each record represents a hospitalized patient who met criteria related to nine disease categories, including acute respiratory failure, liver disease, and various forms of cancer and organ system failure. The features include **physiologic, demographics, and disease severity information**.

## Methodology

### 1. Data Preprocessing

Data preprocessing was crucial for handling a large amount of missing values and preparing the features for modeling.

* **Missing Value Imputation:**
    * **Numerical features** were imputed using the **K-Nearest Neighbors (KNN) imputer** for more accurate estimation based on similarity between data points.
    * **Categorical features** were imputed using the **most frequent category**.
* **Categorical Encoding:** Categorical features were converted into numerical format using **one-hot encoding**.
* **Feature Scaling:** Numerical features were scaled using **StandardScaler** to ensure they have a mean of 0 and a standard deviation of 1, preventing features with larger ranges from dominating the training process.


### 2. Model Building and Hyperparameter Tuning

The problem was framed as a binary classification task. Multiple ensemble methods were employed and evaluated using the **F1 score**, a metric suitable for imbalanced datasets.

The final optimized model used a **Voting Classifier** to combine predictions from two powerful models:

1.  **Random Forest Classifier** 
2.  **Gradient Boosting Classifier** 

**Hyperparameter tuning** was performed using **GridSearchCV** to optimize parameters like the number of estimators and maximum tree depth, leading to improved model performance.

## Results

The models were evaluated on the test set, and the best hyperparameters were selected. The evaluation metric used was the **F1 Score**:

