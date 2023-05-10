# Evaluation and Cross-validation  
Experimental evaluation of learning models is the process of testing and measuring the effectiveness and accuracy of different machine learning models on a specific 
dataset. The main goal of experimental evaluation is to determine which model performs the best for a particular task or problem.
Typical choices for performance evaluation:
-->Error   
-->Accuracy  
-->precision/recall  

## Explain confusion matrix for performance evaluation 
A confusion matrix is a performance evaluation technique for machine learning models that provides a summary of the classification results. It is often used to evaluate the performance of classification models, where the goal is to predict the class label of each data point in a dataset.

A confusion matrix is a matrix with four entries, which are:

True Positive (TP): The number of data points that are correctly predicted as positive (belonging to the positive class).   
False Positive (FP): The number of data points that are incorrectly predicted as positive (belonging to the negative class).  
True Negative (TN): The number of data points that are correctly predicted as negative (belonging to the negative class).   
False Negative (FN): The number of data points that are incorrectly predicted as negative (belonging to the positive class).   

The entries in the confusion matrix can be used to calculate several performance metrics, such as:  

Accuracy: The proportion of correctly classified data points, which is calculated as (TP + TN) / (TP + TN + FP + FN).  
Precision: The proportion of true positives among all predicted positives, which is calculated as TP / (TP + FP).  
Recall (or sensitivity): The proportion of true positives among all actual positives, which is calculated as TP / (TP + FN).    
F1 score: The harmonic mean of precision and recall, which is calculated as 2 * (precision * recall) / (precision + recall).  
The confusion matrix provides a useful way to visualize the performance of a classification model and identify areas where the model is making errors. By examining  
the entries in the confusion matrix, it is possible to determine whether the model is overfitting or underfitting, and adjust  
the model parameters accordingly.  
![con_mat](https://i1.wp.com/dataaspirant.com/wp-content/uploads/2020/08/3_confusion_matrix.png?ssl=1)   
Let's consider a binary classification problem where we are trying to predict whether an email is spam (positive class) or not spam (negative class). Here's an example confusion matrix:
                
                |Spam (Positive)| Not Spam (Negative)|
                |-----------|-----------|
Actual Spam     |   90      |       10  |
Actual Not Spam |   5       |     895   |


## Sample error & True error  

Sample error refers to the error that occurs when a machine learning model is trained on a limited dataset, also known as the training set. This error is calculated by comparing the performance of the model on the training set to its actual output. Sample error occurs when the model is overfitting to the training data and is not able to generalize well to new, unseen data.  

True error, on the other hand, refers to the error that occurs when a machine learning model is tested on new, unseen data that was not used in the training phase.  
This error is calculated by comparing the performance of the model on the testing set to its actual output. True error is a more accurate measure of the model's   
performance since it measures how well the model is able to generalize to new data.  

## Training & Testing Set 
In performance evaluation, a **training set** is a subset of data used to train a machine learning model. The goal is to find patterns and relationships within the data that the model can learn from, so that it can make accurate predictions on new, unseen data.

Once the model has been trained on the training set, it is evaluated on a testing set, which is another subset of data that the model has not seen before. The **testing set** is used to assess the model's performance and to estimate how well it will generalize to new data. The testing set should be representative of the data that the model is likely to encounter in the real world.  

![Training_&_Testing_Set](https://algotrading101.com/learn/wp-content/uploads/2020/06/training-validation-test-data-set.png)

