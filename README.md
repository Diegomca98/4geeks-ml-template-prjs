# Linear Regression Project Tutorial

## Predicting the cost of health insurance for a person
> The important insurance company 4Geeks Insurance S.L. wants to calculate, based on physiological data of its customers what will be the premium (cost) to be borne by each of them. To do this, it has assembled a whole team of doctors and based on data from other companies and a particular study have managed to gather a set of data to train a predictive model.

### Step 1: Loading the dataset
The dataset can be found in this project folder under the name medical_insurance_cost.csv. You can load it into the code directly from the link (https://raw.githubusercontent.com/4GeeksAcademy/linear-regression-project-tutorial/main/medical_insurance_cost.csv) or download it and add it by hand in your repository. In this dataset you will find the following variables:

1. `age`. Age of primary beneficiary (numeric)
2. `sex`. Gender of the primary beneficiary (categorical)
3. `bmi`. Body mass index (numeric)
4. `children`. Number of children/dependents covered by health insurance (numeric)
5. `smoker`. smoker (categorical)
6. `region`. Beneficiary's residential area in the U.S.: northeast, southeast, southwest, northwest (categorical)
7. `charges`. Health insurance premium (numerical)

### Step 2: Perform a full EDA
This second step is vital to ensure that we keep the variables that are strictly necessary and eliminate those that are not relevant or do not provide information. Use the example Notebook we worked on and adapt it to this use case.

Be sure to conveniently divide the data set into train and test as we have seen in previous lessons.

### Step 3: Build a linear regression model
You do not need to optimize the hyperparameters. Start by using a default definition and improve it in the next step.

### Step 4: Optimize the previous model
After training the model, if the results are not satisfactory, optimize it if possible.