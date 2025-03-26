# Credit Score Classification
# About the Data:
The dataset consists of all the basic bank details of the customers, containing both categorical and numerical variables. It has missing values and anomalies. The dataset consists of customers’ banking and financial details collected over the years, allowing for detailed exploration. The data is split into Train and Test datasets. The Train dataset is used to build and test the model, while the Test dataset is used for predictions.
# Problem Statement:
You are working as a data scientist in a global finance company. Over the years, the company has collected various banking and credit-related details. The management aims to develop an intelligent system that categorizes individuals into different credit score brackets, reducing manual effort and improving efficiency.
# Objective:
The objective of this project is to explore the dataset to identify patterns that influence a person’s credit score (Good, Standard, or Poor) and to develop a machine learning model capable of predicting the credit score category accurately.
# Steps to be Followed:
- Understand the business problem.
- Import necessary libraries and set up dependencies.
- Load and inspect the train and test datasets.
- Fix incorrect data types.
- Convert Credit History Age into months.
- Handle missing values using appropriate imputation methods.
- Perform Univariate, Bivariate, and Multivariate analysis.
- Analyze the statistical significance of features affecting the target variable.
- Encode categorical variables and map target variable classes as (Poor = 0, Standard = 1, Good = 2).
- Scale numerical features (optional).
- Split the Train dataset into training and validation sets.
- Build a baseline model and analyze its performance.
- Experiment with multiple machine learning models and select the best one.
- Perform feature selection using various techniques.
- Optimize the model using hyperparameter tuning (Grid Search, Randomized Search, etc.).
- Conduct cross-validation to ensure model robustness.
- Use the Test dataset for final predictions and generate output.
- Summarize business insights based on findings.
# Model Performance Summary:
## Basic Model Performance

| Model Name                    | Train Accuracy | Test Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|--------------------------------|---------------|--------------|-----------|--------|----------|---------|
| Logistic Regression           | 0.631         | 0.632        | 0.641     | 0.632  | 0.629    | 0.793   |
| KNeighborsClassifier          | 0.837         | 0.736        | 0.735     | 0.736  | 0.735    | 0.877   |
| MultinomialNB                 | 0.576         | 0.576        | 0.565     | 0.576  | 0.559    | 0.739   |
| DecisionTreeClassifier        | 1.000         | 0.725        | 0.725     | 0.725  | 0.725    | 0.775   |
| BaggingClassifier             | 0.988         | 0.789        | 0.789     | 0.789  | 0.788    | 0.907   |
| RandomForestClassifier        | 1.000         | 0.819        | 0.820     | 0.819  | 0.819    | 0.932   |
| AdaBoostClassifier            | 0.631         | 0.633        | 0.633     | 0.633  | 0.633    | 0.804   |
| GradientBoostingClassifier    | 0.720         | 0.715        | 0.720     | 0.715  | 0.716    | 0.867   |
| XGBClassifier                 | 0.842         | 0.761        | 0.762     | 0.761  | 0.761    | 0.903   |
| LGBMClassifier                | 0.769         | 0.741        | 0.744     | 0.741  | 0.742    | 0.891   |
| CatBoostClassifier            | 0.818         | 0.763        | 0.764     | 0.763  | 0.764    | 0.902   |

## Random Forest Model Performance Comparison

| Model Name                          | Train Accuracy | Test Accuracy | Precision | Recall | F1-Score | AUC-ROC |
|--------------------------------------|---------------|--------------|-----------|--------|----------|---------|
| RandomForestClassifier              | 1.000         | 0.819        | 0.820     | 0.819  | 0.819    | 0.932   |
| RandomForest with Feature Importance | 1.000         | 0.797        | 0.797     | 0.797  | 0.797    | 0.921   |
| RandomForest with RFE                | 1.000         | 0.797        | 0.797     | 0.797  | 0.797    | 0.921   |
| RandomForest with Best Parameters    | 0.947         | 0.811        | 0.811     | 0.811  | 0.811    | 0.927   |
| Final Model                          | 0.947         | 0.811        | 0.811     | 0.811  | 0.811    | 0.927   |

# Insights:
1. The RandomForestClassifier provided the best test accuracy of **81.9%**, showing a strong ability to classify credit scores.
2. Feature selection using RFE and feature importance did not significantly improve the model's performance.
3. Hyperparameter tuning improved the model's generalizability, leading to an **optimized accuracy of 81.1%**.
4. Key factors affecting credit scores include **number of delayed payments, outstanding debt, credit utilization ratio, and income levels**.
5. The model can be further improved by incorporating **alternative credit data sources** such as transaction history and social behavior analysis.
# Conclusion:
The **Credit Score Classifier** project successfully built a predictive model to classify individuals into different credit score categories based on their financial behavior. The dataset was preprocessed to handle missing values, anomalies, and incorrect data types. Feature engineering, statistical analysis, and exploratory data analysis helped uncover critical insights into credit behavior.
Multiple machine learning models were evaluated, with **RandomForestClassifier** emerging as the best performer. Hyperparameter tuning further optimized the model, achieving a final accuracy of **81.1% on the test data**. This model provides financial institutions with a reliable method to assess customer creditworthiness, reducing manual efforts.
Future improvements could involve **deep learning techniques, explainable AI models, and integration of additional financial data sources**. By refining feature selection and incorporating real-world financial patterns, this project has the potential to enhance risk assessment strategies for credit lenders, making it a valuable tool in the finance sector.
