# LOGISTIC REGRESSION
Logistic regression is a statistical learning model that is commonly used in machine learning for binary classification problems. In logistic regression, the goal is to predict the probability of an event occurring (such as a customer purchasing a product or a patient developing a certain disease) based on one or more input variables or features (such as age, gender, income, etc.).

The output of logistic regression is a probability value between 0 and 1, which can then be thresholded to make a binary prediction (e.g., if the probability is above 0.5, predict class 1, otherwise predict class 0).

The logistic regression model is trained using a set of labeled data, where the labels indicate whether each example belongs to class 0 or class 1. The model learns a set of coefficients (weights) for each input feature, which are used to compute the probability of belonging to class 1.

Let Y be the binary outcome (0 or 1) that we want to predict, and let X be a vector of input features. We assume that the probability of Y given X follows a logistic (or sigmoid) function:

p(Y=1 | X) = f(X)

where f is the logistic function, defined as:

f(X) = 1 / (1 + exp(-z))

where z is a linear function of the input features:

z = b0 + b1X1 + b2X2 + ... + bn*Xn

Here, b0 is the intercept (or bias) term, and b1 to bn are the coefficients (or weights) associated with each input feature X1 to Xn.

The logistic function f(X) maps the linear combination of input features to a probability value between 0 and 1. Specifically, when z is large and positive, the logistic function approaches 1, indicating a high probability of the positive outcome (Y=1); when z is large and negative, the logistic function approaches 0, indicating a low probability of the positive outcome; and when z is close to 0, the logistic function is close to 0.5, indicating a neutral or uncertain probability.

To estimate the model parameters (i.e., the intercept and coefficients), we typically use maximum likelihood estimation (MLE), which involves finding the values of b0 to bn that maximize the likelihood of observing the training data. This can be done using iterative optimization algorithms such as gradient descent or Newton-Raphson.

During training, the **logistic regression** model is optimized to minimize a loss function (such as binary cross-entropy) that measures the difference between the predicted probabilities and the true labels. This is typically done using an optimization algorithm such as gradient descent.

Once the model is trained, it can be used to make predictions on new, unseen data by computing the output probability using the learned coefficients and the input features, and then thresholding the probability to make a binary prediction.
