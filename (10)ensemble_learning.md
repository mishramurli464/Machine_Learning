# Ensemble Learning

Ensemble learning is a machine learning technique that involves combining multiple models to improve the overall performance of a predictive model. It is based on the concept that combining multiple models can result in a better predictive accuracy than any individual model.

The ensemble learning approach is based on the idea that multiple weak learners can be combined to form a strong learner. A weak learner is a model that performs slightly better than random guessing. Examples of weak learners include decision trees, k-nearest neighbors, and logistic regression models. By combining multiple weak learners, the resulting model can have better accuracy and robustness than any of the individual models.

**EXAMPLE**  
Suppose you want to build a model that can predict whether a person is likely to buy a new smartphone or not. You have collected a dataset that contains features such as age, income, education, and previous smartphone ownership, along with the target variable (whether the person bought a new smartphone or not).

Now, you can use ensemble learning to improve the accuracy of your predictive model. Here's how:

Divide the dataset into multiple subsets: Divide the dataset into multiple subsets, using a technique such as cross-validation.

Train multiple models on each subset: Train multiple models on each subset of the dataset using different algorithms or hyperparameters. For example, you could train a decision tree, a logistic regression model, and a neural network on each subset.

Combine the predictions of the models: Once all the models are trained, you can combine their predictions to make the final prediction. You can use a simple technique such as majority voting, where you predict the class that receives the most votes from the models.

For example, suppose you have trained three models: a decision tree, a logistic regression model, and a neural network. The decision tree predicts "Yes", the logistic regression model predicts "No", and the neural network predicts "Yes". In this case, the majority prediction is "Yes", so you would predict that the person is likely to buy a new smartphone.

Evaluate the performance of the ensemble model: Once you have combined the predictions of the models, you can evaluate the performance of the ensemble model on a validation set or test set. You can use metrics such as accuracy, precision, recall, and F1-score to evaluate the performance of the model.
Ensemble learning can help improve the accuracy and robustness of predictive models, especially when dealing with complex datasets and models.

## There are two main types of ensemble learning: bagging and boosting.  
### Bagging 
![1_JksRZ1E72Rsx2s8lQbNR1w](https://user-images.githubusercontent.com/128781536/236659007-ff186de5-669e-4462-8334-294c43675000.jpg)  

Bagging (Bootstrap Aggregating) is a popular ensemble learning algorithm that involves training multiple models on different subsets of the training dataset using bootstrap sampling. The Bagging algorithm aims to reduce the variance of a single model and improve its accuracy by combining the predictions of multiple models.

Here's an example of how the Bagging algorithm works:

Suppose you have a dataset of 1000 records and you want to predict whether a customer will buy a new product or not based on their age, income, and purchase history. You want to use the Bagging algorithm to improve the accuracy of your predictive model.

1)Divide the dataset into multiple subsets: Divide the dataset into multiple subsets of equal size, using a technique such as random sampling with replacement (i.e., bootstrap sampling). For example, you could create 10 subsets of 100 records each.

2)Train a model on each subset: Train a model on each subset of the dataset using the same algorithm (e.g., decision tree) and hyperparameters. For example, you could train 10 decision trees on each subset.

3)Combine the predictions of the models: Once all the models are trained, you can combine their predictions to make the final prediction. You can use a simple technique such as majority voting, where you predict the class that receives the most votes from the models.

For example, suppose you have trained 10 decision trees using the Bagging algorithm. Each decision tree has predicted whether a customer will buy a new product or not. You can then combine the predictions of the decision trees using majority voting. If 7 out of 10 decision trees predict "Yes", then you would predict that the customer is likely to buy a new product.

4)Evaluate the performance of the ensemble model: Once you have combined the predictions of the models, you can evaluate the performance of the ensemble model on a validation set or test set. You can use metrics such as accuracy, precision, recall, and F1-score to evaluate the performance of the model.  
This Algorithm might tend to fall in overfitting

### Boosting  

![a9a5ff4e-b617-4afe-b27b-d96793defa87_6](https://user-images.githubusercontent.com/128781536/236659152-777a8194-6167-4993-a9e4-f178f6b6a53c.jpg)

Boosting is another popular ensemble learning algorithm that involves training multiple models sequentially on different subsets of the training dataset. Unlike Bagging, Boosting focuses on reducing the bias of a single model and improving its accuracy by giving more weight to misclassified samples in each subsequent iteration.

Here's an example of how the Boosting algorithm works:

Suppose you have a dataset of 1000 records and you want to predict whether a customer will buy a new product or not based on their age, income, and purchase history. You want to use the Boosting algorithm to improve the accuracy of your predictive model.

1)Initialize the weight of each sample: In the first iteration, you assign an equal weight to each sample in the training dataset. For example, you could assign a weight of 1/1000 to each sample.

2)Train a weak model on the weighted dataset: In each subsequent iteration, you train a weak model on a subset of the training dataset that is selected based on the weighted distribution of the samples. For example, you could train a decision tree on a subset of the training dataset where the weights of misclassified samples are increased.

3)Update the weight of each sample: After each iteration, you update the weight of each sample in the training dataset based on the misclassification rate of the weak model. For example, you could increase the weight of misclassified samples and decrease the weight of correctly classified samples.

4)Combine the predictions of the models: Once all the models are trained, you can combine their predictions to make the final prediction. You can use a weighted voting technique, where you predict the class that receives the most weighted votes from the models.

For example, suppose you have trained 10 decision trees using the Boosting algorithm. Each decision tree has predicted whether a customer will buy a new product or not. You can then combine the predictions of the decision trees using weighted voting. The weight of each decision tree's prediction is determined by its accuracy and importance in the Boosting algorithm.

5)Evaluate the performance of the ensemble model: Once you have combined the predictions of the models, you can evaluate the performance of the ensemble model on a validation set or test set. You can use metrics such as accuracy, precision, recall, and F1-score to evaluate the performance of the model.  
Boosting algorithms can potentially fall into overfitting
