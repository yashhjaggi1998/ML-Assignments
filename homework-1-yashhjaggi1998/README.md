# README

### Overview

This project focuses on the Vertebral Column Data Set for a binary classification task (Normal vs. Abnormal) using k-Nearest Neighbors (KNN) with various distance metrics.

### Data Set
- **Name:** Vertebral Column Data Set
- **Source:** Built by Dr. Henrique da Mota during a medical residency in Lyon, France.
- **Attributes:** Pelvic incidence, pelvic tilt, lumbar lordosis angle, sacral slope, pelvic radius, grade of spondylolisthesis.
- **Classes:** Normal (NO=0) and Abnormal (AB=1).

### Tasks

#### 1. Download and Pre-Processing/Exploratory Analysis
- **Download:** Obtain the data set from [Vertebral Column Data Set](https://archive.ics.uci.edu/ml/datasets/Vertebral+Column).
- **Pre-Processing:**
  - Scatterplots of independent variables colored by Classes 0 and 1.
  - Boxplots for each independent variable colored by Classes 0 and 1.
  - Split data: First 70 rows of Class 0 and first 140 rows of Class 1 as training set; remaining data as test set.

#### 2. Classification Using KNN
- **Implementation:**
  - Write KNN code with Euclidean metric or use a software package.
  - Test all data in the test set with KNN. Use majority polling for decisions.
  - Plot train and test errors for k ∈ {208, 205, ..., 7, 4, 1}.
  - Identify the most suitable k (k*).
  - Calculate confusion matrix, true positive rate, true negative rate, precision, and F1-score for k = k*.
- **Learning Curve:**
  - Plot best test error rate against the size of training set (N ∈ {10, 20, 30, ..., 210}).
  - For each N, select training set with first ⌊N/3⌋ rows of Class 0 and N - ⌊N/3⌋ rows of Class 1.
  - Select optimal k from {1, 6, 11, ..., 196} for each N.

#### 3. Alternative Distance Metrics
- **Minkowski Distance:**
  - Manhattan Distance (p = 1).
  - Log10(p) ∈ {0.1, 0.2, 0.3, ..., 1} using k* found for Manhattan distance.
  - Chebyshev Distance (p → ∞).
- **Mahalanobis Distance:**
  - Requires inverting the covariance matrix of the data.
- **Summary:** Report test errors (k = k*) in a table for all metrics.

#### 4. Weighted Voting
- Replace majority polling with weighted decision.
- Use weights inversely proportional to the distance from the test point.
- Report best test errors for k ∈ {1, 6, 11, ..., 196} using Euclidean, Manhattan, and Chebyshev distances.

#### 5. Training Error
- Report the lowest training error rate achieved in this homework.

### Notes
- Ensure labels are converted to 0 and 1.
- Research how to compute the confusion matrix, true positive rate, true negative rate, precision, and F1-score.

### Additional Information
- **Distance Metrics:** Use sklearn.neighbors.DistanceMetric.
- **Mahalanobis Distance:** May require pseudoinverse if covariance matrix is singular or ill-conditioned.

For further details, refer to the assignment guidelines provided in the homework document.