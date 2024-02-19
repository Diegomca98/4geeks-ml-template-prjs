# Time Series Forecasting - Project Tutorial

- Understanding a new dataset.
- Analyze the time series and study its characteristics.
- Train a model to predict future memory expenditure.

## Sales forecasting system

> We want to set up our company's warehouse in another location and we need to estimate the rate of sales, which has been increasing since the company's creation, for the next few months in order to provide the space we will need.

### Step 1: Loading the dataset

The dataset can be found in this project folder under the name `sales.csv`. You can load it into the code directly from the link (`https://raw.githubusercontent.com/4GeeksAcademy/alternative-time-series-project/main/sales.csv`) or download it and add it by hand in your repository.

### Step 2: Construct and analyze the time serie

Construct the valid data structure for the time serie, graph it, and then analyze it and answer the following questions:

- Which is the tensor of the time serie?
- Which is the trend?
- Is it stationary?
- Is there variability or noise?

> NOTE: A `tensor` in a time serie is the minimum unit of time for which there is data. It can be every second, minute, hour, day, week, month...

### Step 3: Train an ARIMA

Use the training data to find the best parameterization of your ARIMA model.

### Step 4: Predict with the test set

Now use the trained model with the test set and compare the points with the real ones. Measure the performance of the time serie.

### Step 5: Save the model

Store the model in the corresponding folder.