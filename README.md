# Logistic Regression Project Tutorial
* Understand a new dataset.
* Process it by applying exploratory data analysis (EDA).
* Model the data using logistic regression.
* Analyze the results and optimize the model.

## Banking Marketing Campaign

***Business Insight***

> Long-term deposits allow banks to hold money for a specific period of time, allowing the bank to use that money to enhance its investments. Marketing campaigns for this product are based on phone calls. If a user is not available at a given time, then they will be called back at another time.

***Description of the problem***

> The Portuguese bank is experiencing a decline in revenue, so they want to be able to identify existing customers who are more likely to take out a long-term deposit. This will allow the bank to focus their marketing efforts on those customers and avoid wasting money and time on customers who are unlikely to sign up.

> To address this problem we will create a ranking algorithm to help predict whether or not a customer will sign up for a long-term deposit.

### Step 1: Loading the dataset
The dataset can be found in this project folder under the name bank-marketing-campaign-data.csv. You can load it into the code directly from the link (https://raw.githubusercontent.com/4GeeksAcademy/logistic-regression-project-tutorial/main/bank-marketing-campaign-data.csv) or download it and add it by hand in your repository. In this dataset you will find the following variables:

1. `age`. Age of customer (numeric)
2. `job`. Type of job (categorical)
3. `marital`. Marital status (categorical)
4. `education`. Level of education (categorical)
5. `default`. do you currently have credit (categorical)
6. `housing`. do you have a housing loan (categorical)
7. `loan`. Do you have a personal loan? (categorical)
8. `contact`. Type of contact communication (categorical)
9. `month`. Last month in which you have been contacted (categorical)
10. `day_of_week`. Last day on which you have been contacted (categorical)
11. `duration`. Duration of previous contact in seconds (numeric)
12. `campaign`. Number of contacts made during this campaign to the customer (numeric)
13. `pdays`. Number of days that elapsed since the last campaign until the customer was contacted (numeric)
14. `previous`. Number of contacts made during the previous campaign to the customer (numeric)
15. `poutcome`. Result of the previous marketing campaign (categorical).
16. `emp.var.rate.` Employment variation rate. Quarterly indicator (numeric)
17. `cons.price.idx.` Consumer price index. Monthly indicator (numeric)
18. `cons.conf.idx.` Consumer confidence index. Monthly indicator (numeric)
19. `euribor3m`. EURIBOR 3-month rate. Daily indicator (numeric)
20. `nr.employed.` Number of employees. Quarterly indicator (numeric)
21. `y`. TARGET. Whether the customer takes out a long-term deposit or not

### Step 2: Perform a full EDA
This second step is vital to ensure that we keep the variables that are strictly necessary and eliminate those that are not relevant or do not provide information. Use the example Notebook we worked on and adapt it to this use case.

Be sure to conveniently divide the data set into train and test as we have seen in previous lessons.

### Step 3: Build a logistic regression model
You do not need to optimize the hyperparameters. Start by using a default definition and improve it in the next step.

### Step 4: Optimize the previous model
After training the model, if the results are not satisfactory, optimize it using one of the techniques seen above.