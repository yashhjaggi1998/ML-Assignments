# README

### Overview
This homework focuses on time series classification using data from a Wireless Sensor Network to classify human activities. It involves feature extraction, binary classification using logistic regression, and multiclass classification using various methods.

### Data Set
- **Name:** AReM (Activity Recognition system based on Multisensor data fusion)
- **Source:** [AReM Data](https://archive.ics.uci.edu/ml/datasets/Activity+Recognition+system+based+on+Multisensor+data+fusion+(AReM))
- **Attributes:** 6 time series per instance (avg rss12, var rss12, avg rss13, var rss13, avg rss23, var rss23)
- **Instances:** 88 instances, each with 480 consecutive values per time series

### Tasks

#### 1. Time Series Classification Part 1: Feature Creation/Extraction
- **Data Preparation:**
  - Download the AReM data set.
  - Use datasets 1 and 2 in folders bending1 and bending2, and datasets 1, 2, and 3 in other folders as test data. Use remaining datasets as train data.
- **Feature Extraction:**
  - Research and list common time-domain features for time series classification.
  - Extract features: minimum, maximum, mean, median, standard deviation, first quartile, and third quartile for all 6 time series in each instance.
  - Estimate the standard deviation of each feature and build a 90% bootstrap confidence interval for these standard deviations.
  - Select the three most important time-domain features using your judgment.

#### 4. Binary Classification Using Logistic Regression
- **Scatter Plots:**
  - Depict scatter plots of selected features for time series 1, 2, and 6 to distinguish between bending and other activities.
  - Repeat with time series split into equal parts.
- **Logistic Regression:**
  - Break each time series into \( l \) parts (from 1 to 20) and fit logistic regression models.
  - Calculate p-values and refit models using significant features.
  - Use 5-fold cross-validation to find optimal \( l \) and number of features.
  - Report confusion matrix, ROC, and AUC for classifier on train data.
  - Test classifier on test set and compare accuracy with cross-validation results.
  - Address class imbalance if observed.

#### 5. Binary Classification Using L1-penalized Logistic Regression
- **L1 Regularization:**
  - Repeat logistic regression using L1-penalized logistic regression.
  - Cross-validate for both \( l \) and L1 penalty weight \( \lambda \).
  - Compare results with variable selection using p-values.

#### 6. Multi-class Classification
- **Multinomial Regression:**
  - Find the best \( l \) and build an L1-penalized multinomial regression model.
  - Report test error and visualize confusion matrices and ROC curves for multiclass classification.
- **Naive Bayes:**
  - Compare multinomial regression with Naive Bayes classifier using Gaussian and Multinomial priors.
  - Evaluate which method performs better for multiclass classification.

### Notes
- **Data Cleaning:** Minor cleaning required for some data files.
- **Feature Engineering:** Experiment with normalizing/standardizing features.
- **Cross-Validation:** Use stratified cross-validation if class imbalance is an issue.
- **Tools:** Use Python’s `bootstrapped`, `scikit-learn`, and other relevant libraries for implementation.
