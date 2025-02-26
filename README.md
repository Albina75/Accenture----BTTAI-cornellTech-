# Accenture----BTTAI-cornellTech- (ML Model to Predict Credit Score)

## Introduction:

Credit score plays a pivotal role in determining one's financial health. An accurate and high score opens doors to faster approvals to loans, lower interest rates, and can influence rental terms, insurance etc. It essentially becomes easier for pepole to afford things and make their expenses manageable. And it becomes easier for people as well as financial establishments(banks/vendors) streamline the process if they have a way to know a person's future credit score from their present fiancial habit.
As part of the Break Through tech AI program, I, along with my team, got an opportunity to work with couple of data scientists from Accenture to on this very issue. We were provided a dataset with 28 columns and 100,000 rows of data. The dataset includes a person's credit related information like occupation, annual income, monthly inhand salary, SSN, credit history age, number of bank accounts, credit mix, number of credit cards, payment behavior, monthly balance etc. for eight months (January to August)

#### **_The task is to build a Machine Learning Model to predict the credit score of an individual based on the financial information provided in dataset._**

## The Process:
### 1. Understanding Credit Scores:

Before starting the technical aspects of the project, we first explored the business context and the potential impact of predicting credit scores accurately. We learned how the banking and credit card system operates and what factors influence credit scores.
A credit score is primarily determined by five key factors:

+ **Payment History (35%)** – This is the most critical factor and reflects whether an individual has made past credit payments on time.

+ **Amounts Owed (30%)** – Represents the total debt and credit utilization.

+ **Length of Credit History (15%)** – Measures how long a person has had credit accounts.

+ **Types of Credit (10%)** – Having a mix of credit types such as credit cards, home loans, and auto loans is beneficial.

+ **New Credit (10%)** – Opening several new credit accounts in a short time can lower the score.

While our dataset did not contain these factors directly, this understanding helped us identify key variables to focus on, such as Credit History Age, Number of Credit Inquiries, Monthly Balance, and Credit Utilization Ratio, rather than demographic attributes like occupation, age, or annual income.

### 2. Data Cleaning 

After establishing domain knowledge, we started cleaning and preparing the data. This was a rigorous process due to significant outliers, null values, absurd values, and inconsistent formats. Major steps included:

+ **Handling Missing Values**: Used forward and backward filling for continuous variables, while categorical values were replaced with mode.

+ **Feature Encoding**: Categorical features like occupation and payment behavior were converted into numerical values using label encoding and one-hot encoding.

+ **Outlier Treatment**: Outliers in income, outstanding debt, and delayed payments were handled using capping and transformation techniques.

+ **Feature Engineering**: Transformed "Credit History Age" into numerical values and extracted insights from multi-categorical attributes such as loan types.

### 3. Model Selection & Training

We stuck to classification as we wanted the predicted score to be in 'Good', 'Poor', 'Standard' format as the orginal 'credit score' column has this format instead of numerical score. So, because of time constraint, we decided to keep the format of the orginal credit score column, rather than having a numerical range for each credit score status.

In context of our dataset, we have chosen three classification models to experimented with: 

Random Forest----------Works better with diverse data

Gradient boosting------Gradually improves overall performance, 

K-NN-------------------Sensitive to patterns in data

#### 1. Random Forest Classifier

+ Accuracy: 80.51%

+ Best in precision and recall for standard and good credit scores

+ Confusion Matrix & Classification Report used for evaluation

#### 2. Gradient Boosting Classifier

+ Accuracy: 70.34%

+ Showed lower performance due to imbalanced data but effective for interpretability

#### 3. K-Nearest Neighbors (KNN)

+ Accuracy: 79.23%

+ Performed well but required high computational resources

### 4. Performance Evaluation

+ The Random Forest model emerged as the best-performing classifier with an accuracy of 80.51%.

+ The F1-score for predicting different credit score categories was balanced, indicating robustness in classification.

+ Feature importance analysis revealed that Credit Utilization Ratio, Outstanding Debt, and Payment Behavior were the top predictors of credit scores.

** _Therefore, We have decided to choose Random Forest as our final model._**

### 5. Area of Improvements

+ Better CPU could have reduced training time, giving us more chance to test complex models
+ Mathematical formulas to precisely calculate the credit score -- is someting to be explored
+ Implementation of better hyperparameter tuning .
+ Exploration of deep learning model to get a more accurate predictions.

## Conclusion:

This project showcases my ability to handle large datasets, clean and preprocess data, and build effective machine learning models. Predicting credit scores accurately can aid financial institutions in making better lending decisions, thereby reducing financial risk


