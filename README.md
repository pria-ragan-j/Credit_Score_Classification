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

| Model Name              | Train Accuracy | Test Accuracy | Precision | Recall   | F1-Score | AUC-ROC | Mean CV  | Std CV  |
|-------------------------|----------------|----------------|-----------|----------|----------|---------|----------|---------|
| Logistic Regression     | 0.631100       | 0.631867       | 0.640713  | 0.631867 | 0.628559 | 0.792580| 0.629657 | 0.006653|
| KNeighborsClassifier    | 0.836514       | 0.735667       | 0.734963  | 0.735667 | 0.734898 | 0.876567| 0.719829 | 0.005733|
| MultinomialNB           | 0.576286       | 0.575933       | 0.565478  | 0.575933 | 0.559136 | 0.739475| 0.575914 | 0.006086|
| DecisionTreeClassifier  | 1.000000       | 0.724900       | 0.724830  | 0.724900 | 0.724864 | 0.774505| 0.723586 | 0.004818|
| BaggingClassifier       | 0.987600       | 0.788567       | 0.788579  | 0.788567 | 0.788175 | 0.907397| 0.784000 | 0.005174|
| RandomForestClassifier  | 1.000000       | 0.819133       | 0.819751  | 0.819133 | 0.819191 | 0.932200| 0.814129 | 0.003653|
| AdaBoostClassifier      | 0.630629       | 0.632700       | 0.633101  | 0.632700 | 0.632766 | 0.804087| 0.631557 | 0.005993|
| GradientBoostingClassifier | 0.719786    | 0.714867       | 0.720383  | 0.714867 | 0.715822 | 0.867345| 0.713971 | 0.004026|
| XGBClassifier           | 0.842443       | 0.760967       | 0.761840  | 0.760967 | 0.760936 | 0.902677| 0.766929 | 0.006329|
| LGBMClassifier          | 0.768686       | 0.740933       | 0.744211  | 0.740933 | 0.741694 | 0.891150| 0.742614 | 0.005935|
| CatBoostClassifier      | 0.817986       | 0.763400       | 0.764343  | 0.763400 | 0.763688 | 0.902032| 0.764771 | 0.004572|


## Random Forest Model Performance Comparison

| Model Name                                      | Train Accuracy | Test Accuracy | Precision | Recall   | F1-Score | AUC-ROC | Mean CV  | Std CV  |
|--------------------------------------------------|----------------|----------------|-----------|----------|----------|---------|----------|---------|
| RandomForestClassifier                           | 1.000000       | 0.819133       | 0.819751  | 0.819133 | 0.819191 | 0.932200| 0.814129 | 0.003653|
| RandomForestClassifier with feature importance   | 1.000000       | 0.796533       | 0.797369  | 0.796533 | 0.796829 | 0.920672| 0.796857 | 0.003691|
| RandomForestClassifier with RFE feature selection| 1.000000       | 0.796533       | 0.797369  | 0.796533 | 0.796829 | 0.920672| 0.796857 | 0.003691|
| RandomForestClassifier with best parameters      | 0.946771       | 0.810667       | 0.811474  | 0.810667 | 0.810865 | 0.926892| 0.805814 | 0.003221|
| Final Model                                      | 0.946771       | 0.810667       | 0.811474  | 0.810667 | 0.810865 | 0.926892| 0.805814 | 0.003221|


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
