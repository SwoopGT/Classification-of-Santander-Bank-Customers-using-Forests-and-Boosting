# Classification-of-Santander-Bank-Customers-using-Forests-and-Boosting

## 1. Introduction

Santander Bank is a North American bank owned by the Spanish Santander Group which employs around 10 thousand employees and has about 57 Billion dollars in deposits. It has its principal market focused around the north-eastern states of America [2].
For any consumer focused business there broadly exist two types of consumer mindsets: satisfied and dissatisfied. It also happens in very few cases that the dissatisfied consumers openly voice their opinion before leaving. This brings further to the question- How can the company improve upon the areas where the customers are dissatisfied? Such a question was put forth by Santander Bank in order to gain insights regarding the satisfaction level of customers. 

The bank provided a large dataset consisting of about 76 thousand rows and 371 features. The expected outcome was a model capable of predicting dissatisfied customers early in the process so that necessary steps can be taken before it was pretty late.
</br>

## 2. Business Problem 

The main question is- If the organization was to reduce the means by which customers are affected or left dissatisfied – What can be done for such a situation? Can early prediction of such a customer be possible? What measures can be taken to retain the customer?

This report aims to put forward an analysis of prediction of customer satisfaction using machine learning algorithms such as Random Forest and Gradient Boosting.
</br>

## 3. People interested in the Project – Target Audience

The target audience in this scenario are the management of Santander Group who are responsible to make the necessary decisions once the factors contributing to the dissatisfaction are identified. The factors can be identified by paying extra attention to the customers identified by the algorithm and tending to their needs.
</br>

## 4. Data required

The data required to build a model to predict the customer satisfaction is as follows:
Customer Data: Data pertaining to the customers is provided by the bank for analysis.
</br>

## 5. Methodology

The following steps were employed to obtain the required results:
</br>

### 5.1 Importing Necessary Libraries

The first step is to import the necessary libraries and packages. 
Numpy – For numerical calculations
Matplotlib – plotting and visualization
Pandas – Data manipulation
Sklearn – Machine Learning
XGBoost – Gradient Boosting
</br>

### 5.2 Google Drive Pre- requisites

This step involves the authentication steps taken in order to use the dataset stored in Google Drive which can be directly loaded into Google Colab.
</br>

### 5.3 Pre-Processing

The following preprocessing steps were employed:
1. Checking the columns (features) present in the dataset
2. Getting statistical information of the dataset
3. Checking for presence of null values
4. Correcting outliers present in one feature (var3)
5. Checking is the dataset is balanced or unbalanced
6. Performing the train- test split
7. Scaling the training splits
</br>

### 5.4 Machine Learning

The following 2 machine learning algorithms were used:
1. Random Forest Classifier
2. Gradient Boosting Classifier
</br>

### 5.5 Analysis
The analysis involved checking the precision and recall score of above machine learning algorithms in two sections which are as follows:

##### 1. Section A – Unbalanced dataset

This section involved using the dataset after preprocessing without performing any sampling operation. The two machine learning models were trained and were evaluated and the metrics were calculated.

##### 2. Section B – Balanced dataset
In this section undersampling procedure was performed to balance the dataset (3008 rows). Further, using this balanced dataset the two machine learning models were trained and metrics for evaluation were obtained.

** The models were trained on the balanced dataset and then tested on the unbalanced dataset to gauge the working power of the trained model.
The models were subjected to Randomized Search Cross Validation and the best hyper parameters were obtained.
These parameters were used to train the models again and the results were fed into a dataframe.

</br>

### 5.6 Metrics for Evaluation
The following metrics were used for evaluation:
1. ROC- AUC
2. Precision
3. Recall
4. Log-loss
5. Confusion Matrix
</br>

## 6.Results

Random Forest

1. Using Random Forest Classifier model on the entire dataset with 25 features, the accuracy obtained was 95.34 % owing to the fact that the dataset was highly unbalanced (97- 3).
2. After balancing the dataset (Undersampling) with 3008 records and 25 features the accuracy decreases to 72.17 % (24.3% decrease) and log loss decreases to 0.621 (15% decrease) also AUC increases by a bit (18.2 % increase).
3. Using Randomized Search CV for hyperparameter optimization the score decreases by a bit (6% decrease) with a little decrease in log loss (8% decrease). AUC increases insignificantly (3% increase).The selected parameters were n_estimators = 400 and max_features =sqrt.
4. Using the trained model on balanced dataset, to predict the results on imbalanced dataset, the accuracy increases (10% increase) and loss further reduces (5% decrease). The AUC is lower in this step as compared to the previous ones (13 % decrease).
5. Optimizing the imbalanced dataset similar to the balanced dataset provides an accuracy of around 87 % (9% increase) with a loss of about 0.561(3% decrease) with further little decrease in AUC (4 % decrease)

Gradient Boosting

1. Using Gradient Boosting Classifier model on the entire dataset with 25 features, the accuracy obtained was 96.00 % owing to the fact that the dataset was highly unbalanced (97- 3).
2. After balancing the dataset (Undersampling) with 3008 records and 25 features the accuracy decreases to 74 % (23% decrease) and log loss increases to 0.5139 (255% increase) also AUC decreases by a bit (1 % decrease).
3. Using Randomized Search CV for hyperparameter optimization the score increases by a bit (1% increase) with little change in log loss (0.4% increase) and AUC (0.3% decrease). The selected parameters were max_child_wt = 7, learning_rate = 0.05, max_depth = 8, gamma = 0, col_sample_bytree = 0.4
4. Using the trained model on balanced dataset, to predict the results on imbalanced dataset, the accuracy decreases to about 63.752 % (14% decrease) and loss further increases to 0.639 (23% increase). The AUC is lower in this step as compared to the previous ones (20% decrease).
5. Optimizing the imbalanced dataset similar to the balanced dataset provides best accuracy of around 90.706 % (42% increase) with a decrease in loss (31% decrease) with further decrease in AUC (1% decrease).
</br>

## 7. Limitations

The following inferences can be more refined if the names of the features were available. This would help in removal of unnecessary features and would further provide more idea into feature importance.
</br>

## 8. Conclusion

Using Google Collab, the dataset stored in google drive was loaded. Pre-processing steps were carried out and machine learning algorithms were applied. Hyper parameter tuning was carried out to obtain optimum results. The metrics for models were evaluated and compared.
</br>

## 9. References

Pymnts, “Santander Digital Investment Unit Global Banking Spanish Banks,” [Online]. Available:  https://www.pymnts.com/news/international/2018/santander-digital-investment-unit-global-banking-spanish-banks
Wikipedia, “Santander Bank,” [Online]. Available: https://en.wikipedia.org/wiki/Santander_Bank
</br>

