## Credit risk classification
## Overview
The purpose of this activity is to train and evaluate machine learning models based on loan risk. The activity use a dataset of historical lending activity from a peer-to-peer lending services company to build a model that can identify the creditworthiness of borrowers and classify the credit risk predictions. The dataset (77,536 data points) was split into training and testing sets. The training set was used to build an initial logistic regression model (Logistic Regression Model ) using the LogisticRegression module from scikit-learn. Logistic Regression Model  was then applied to the testing dataset. The purpose of the model was to determine whether a loan to the borrower in the testing set would be low- or high-risk and results are summarized below.
This intial model was drawing from a dataset that had 75,036 low-risk loan data points and 2,500 high-risk data points. To resample the training data and ensure that the logistic regression model had an equal number of data points to draw from, the training set data was resampled with the RandomOverSampler module from imbalanced-learn. This generated 56,277 data points for both low-risk (0) and high-risk (1) loans, based on the original dataset.


## Results
- For the "healthy loan" class, the precision is 1.00, indicating that the model predicts this label with perfect precision. For the "high-risk loan" class, the precision is 0.85, meaning that 85% of the predicted high-risk loans are correct.
- The recall for the "healthy loan" class is 0.99, indicating that the model captures all the actual healthy loans. The recall for the "high-risk loan" class is 0.91, meaning that the model identifies 91% of the high-risk loans correctly.
- For the "healthy loan" class, the F1-score is 1.00, indicating perfect performance. The F1-score for the "high-risk loan" class is 0.88, representing a good balance between precision and recall for this label.



## Summary
- Machine Learning - Logistic Regression does a good job in predicting both the healthy and the high-risk loans as can be inferred from the high accuracy score of 99% and balanced accuracy score of 95%. 
- This model has a precision score of 100% for the healthy loans and 85% for the high-risk loans. This again can be attributed to the imbalance in the data. The precision scores imply that the healthy loans were classified correctly as positive 100% of the times. However, for the high-risk loans, the classification was correct only 85% of the times.
- This model has a recall score of 99% for the healthy loans and 91% for the high-risk loans. The scores imply that for all the instances where the loans were actually healthy, 99% of the times they were classified correctly. However, for all the instances where the loans were actually high-risk, they were classified correctly 91% of the times.
