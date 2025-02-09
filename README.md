# Berkeley Haas - Professional Certificate in Machine Learning and Artificial Intelligence - Cap

## Background
This project aims to train a classification model to predict if a user will accept a coupon given his/her answers to some survey questions.

The data used in here comes from a survey on Amazon Mechanical Turk. 
[In-Vehicle Coupon Recommendation](https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation)

In this project the work I have done is split into 3 parts.

### Part 1 - Preprocessing of the data
During this data processing, I have worked to:

* Handle Missing Values
* Handle Duplicated Data
* Handle Outliers
* Feature Transformation
* Feature Encoding
* Handle Class Imbalance
* Feature Selection & Feature Extraction

### Part 2 Modeling training

Here in Part 2, I have transformed the features  we tested our data train to machine learning model and evaluated it. 

#### Data Tranformation and Encoding
Here I am performing data preprocessing for machine learning pipeline using ColumnTransformer from sklearn. 

Standardized numerical features by scaling them to have zero mean and unit variance using StandardScaler().

Encoded categorical variables using OneHotEncoding, converting each category into a binary vector.

Fit the transformations to X_train (learns scaling parameters for numerical data and identifies unique categories for OneHotEncoding).

Used the same transformations learned from X_train and applies them to X_test (without refitting).

All numerical features are standardized.
All categorical features are one-hot encoded.
With this the data is now ready for machine learning models that require numerical input.

#### Creation and running performance of different models

 I created and tested the model performance for the following models:
 
 * Logistic Regression
 * Lasso Regression
 * Decision Trees
 * Gaussian Naive Bayes
 * Bernoulli Naive Bayes
 * K-nearest Neighbor
 * Linear SVM - Support Vector Machines

### Part 3 Summary and Evaluation of Model performance

The following table summarizes the results of Validation Accuracy,  Testing Accuracy  and AUC - Area Under the Curve

From the table it clear that KNN Classifier performs better than the rest of the models.

| Model | Validation Accuracy|Testing Accuracy|AUC|
|-------|---------|-------|-----------|
|Logistic Regression with No Penalty|0.683|0.673|0.73|
|Lasso Logistic Regression|0.685|0.674|0.73|
|Ridge Logistic Regression|0.685|0.674|0.73|
|Decision Tree|0.684|0.686|0.73|
|Gaussian Naive Bayes|0.636|0.637|0.67|
|Bernoulli Naive Bayes|0.657|0.655|0.70|
|KNN Classifier|**0.722**|**0.732**|**0.79**|
|Linear SVM|0.685|0.672|0.73|

## Link to Notebook:
[Explore Coupon Acceptance Factors by Customers](https://github.com/nbajam/BH-PCAIML-project/blob/main/bh_pcaiml_project_final.ipynb)

## Data Used:
[In-Vehicle Coupon Recommendation](https://archive.ics.uci.edu/dataset/603/in+vehicle+coupon+recommendation)

