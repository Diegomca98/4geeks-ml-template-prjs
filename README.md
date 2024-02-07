# Random Forest Project Tutorial
* Use the data you have analyzed in the previous project.
* Continue with the development to find a model that fits better.

## Predicting diabetes
>In the previous project we saw how we could use a decision tree to predict data sets related to classification and regression. However, did you know that we can improve the prediction of a tree by using a random forest?
>
> As we have studied, a random forest is a grouping of trees generated with random portions of the data and with random criteria. This view would allow us to improve the effectiveness of the model when an individual tree is not sufficient.
> 
> In this project you will focus on this idea by training the dataset to improve the `accuracy`

### Step 1: Loading the dataset
Load the processed dataset from the previous project (split into training and test samples and analyzed with EDA).

### Step 2: Build a random forest
One way to optimize and improve the results when using decision trees is to generate a random forest with enough trees so that there is the necessary variety to enrich the prediction. Train it and analyze its results. Try modifying the two hyperparameters that define the tree with different values and analyze their impact on the final accuracy and plot the conclusions.

### Step 3: Save the model
Store the model in the corresponding folder.