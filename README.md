# Accenture----BTTAI-cornellTech- (ML Model to Predict Credit Score)
As part of the Break Through tech AI program, I, along with my team, got an opportunity to work with Accenture. We were provoded a dataset with 28 columns and 100,000 rows of data. The dataset includes a person's credit related information like occupation, annual income, monthly inhand salary, SSN, credit history age, number of bank accounts, credit mix, number of credit cards, payment behavior, monthly balance etc. for eight months (January to August)

The task is to build a Machine Learning Model to predict the credit score of an individual based on the information provided in dataset.

The most difficult task was to clean the dataset as it has thousands of null values, absurd values, outliers in most of the columns. Also, we really had to dig in the financial side of the project to undersatand the process of credit score. 

We stuck to classification as we wanted the predicted score to be in 'Good', 'Poor', 'Standard' format because the orginal 'credit score' column has this format instead of numerical score. So, because of time constraint, we decided to keep the format of the orginal credit score column, rather than having a numerical range for each credit score status and use regression.

We tested out three moldes on the data -- Random Forest, Gradient Boosting and K-NN. Ultimately, Random Forest proved to be better than the other two with 80% accuracy.
