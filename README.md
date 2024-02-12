# Linear Regression Project Tutorial

* Understand a new dataset.
* Process it by applying exploratory data analysis (EDA).
* Model the data using logistic regression.
* Analyze the results and optimize the model.

## US county-level sociodemographic and health resource data (2018-2019).
> Sociodemographic and health resource data have been collected by county in the United States and we want to find out if there is any relationship between health resources and sociodemographic data.
>
> To do this, you need to set a target variable (health-related) to conduct the analysis.

### Step 1: Loading the dataset
The dataset can be found in this project folder under the name demographic_health_data.csv. You can load it into the code directly from the link [Demographic Health Data](https://raw.githubusercontent.com/4GeeksAcademy/regularized-linear-regression-project-tutorial/main/demographic_health_data.csv) or download it and add it by hand in your repository. In this dataset you will find a large number of variables, which you will find defined here.

### Step 2: Perform a full EDA
This second step is vital to ensure that we keep the variables that are strictly necessary and eliminate those that are not relevant or do not provide information. Use the example Notebook we worked on and adapt it to this use case.

Be sure to conveniently divide the data set into train and test as we have seen in previous lessons.

### Step 3: Build a regression model
Start solving the problem by implementing a linear regression model and analyze the results. Then, using the same data and default attributes, build a Lasso model and compare the results with the baseline linear regression.

Analyze how $R^2$ evolves when the hyperparameter of the Lasso model changes (you can for example start testing from a value of 0.0 and work your way up to a value of 20). Draw these values in a line diagram.

### Step 4: Optimize the previous model
After training the Lasso model, if the results are not satisfactory, optimize it using one of the techniques seen above.