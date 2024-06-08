# README

### Overview
This homework focuses on analyzing and predicting the net hourly electrical energy output of a Combined Cycle Power Plant using various regression techniques and KNN.

### Data Set
- **Name:** Combined Cycle Power Plant Data Set
- **Source:** Data points collected over 6 years (2006-2011) from a power plant operating at full load.
- **Attributes:** Temperature (T), Ambient Pressure (AP), Relative Humidity (RH), Exhaust Vacuum (V), Electrical Energy Output (EP).

### Tasks

#### 1. Download and Explore the Data
- **Download:** Obtain the data set from [Combined Cycle Power Plant](https://archive.ics.uci.edu/ml/datasets/Combined+Cycle+Power+Plant).
- **Exploration:**
  - Determine the number of rows and columns in the dataset.
  - Create pairwise scatterplots for all variables.
  - Compute and summarize the mean, median, range, quartiles, and interquartile ranges of each variable.

#### 2. Simple Linear Regression
- **Fit Models:**
  - For each predictor, fit a simple linear regression model to predict the response.
  - Identify statistically significant associations between predictors and response.
  - Create plots to support your findings.
  - Identify and consider removing outliers.

#### 3. Multiple Regression Model
- **Fit Model:**
  - Predict the response using all predictors.
  - Identify which predictors reject the null hypothesis \( H_0 : \beta_j = 0 \).

#### 4. Comparison of Regression Models
- **Compare Results:**
  - Compare univariate and multiple regression results.
  - Create a plot with univariate regression coefficients on the x-axis and multiple regression coefficients on the y-axis.

#### 5. Nonlinear Associations
- **Fit Models:**
  - For each predictor, fit a polynomial regression model of the form \( Y = \beta_0 + \beta_1X + \beta_2X^2 + \beta_3X^3 + \epsilon \).
  - Check for evidence of nonlinear associations.

#### 6. Interaction Terms
- **Fit Models:**
  - Run a full linear regression model with all pairwise interaction terms.
  - Identify statistically significant interaction terms.

#### 7. Model Improvement
- **Improve Models:**
  - Train a regression model on a randomly selected 70% subset with all predictors.
  - Run a regression model with all interaction terms and quadratic nonlinearities, removing insignificant variables.
  - Report train and test Mean Squared Errors (MSEs).

#### 8. KNN Regression
- **Perform KNN:**
  - Use k-nearest neighbor regression with both normalized and raw features.
  - Find the optimal k ∈ {1, 2, ..., 100} for the best fit.
  - Plot train and test errors in terms of 1/k.

#### 9. Comparison of KNN and Linear Regression
- **Compare Models:**
  - Compare the results of KNN regression with the best linear regression model.
  - Provide an analysis of the comparison.