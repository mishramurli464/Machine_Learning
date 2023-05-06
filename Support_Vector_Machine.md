# SUPPORT VECTOR MACHINE  
A Support Vector Machine (SVM) is a type of supervised learning algorithm used for classification and regression analysis. SVMs are effective in solving problems 
where the data is separable by a hyperplane.  
In classification problems, SVM tries to find a hyperplane that separates the data into classes with the maximum margin possible, which means that the distance between 
the hyperplane and the nearest data point from each class is maximized. This is called the maximum margin hyperplane. The SVM algorithm can also handle non-linearly 
separable data by mapping the data into a higher-dimensional space, where it can be linearly separated.  
In regression analysis, SVMs can be used to predict a continuous variable by finding a hyperplane that is closest to as many data points as possible, while still having
a maximum margin between the hyperplane and the data points.  
In SVM, there are two types of margins: the functional margin and the geometric margin. Let's discuss each of them in detail:

## Functional margin:

![functional_margin](https://user-images.githubusercontent.com/128781536/235594121-1b47f7b0-e9b9-4131-b8e3-191a51643a44.png)
 
The classifier with the maximum margin width is robust to outliners and thus has strong generalization ability

The functional margin of a data point (x_i, y_i) is the product of the distance of the data point from the decision boundary (i.e., hyperplane) and its true label y_i. 
Mathematically, the functional margin is given by:  

**margin_i = y_i * (w*x_i + b)**  
Here, w and b are the parameters of the hyperplane that we are trying to learn.
To find the optimal hyperplane, we want to maximize the minimum functional margin of all the data points. Mathematically, this can be represented as:  

**maximize min_i(y_i * (w*x_i + b))**   

**subject to ||w|| = 1**  
where ||w|| is the Euclidean norm of the weight vector w.

The functional margin is sensitive to outliers, as it takes into account the distance of each data point from the decision boundary. However, the outliers may 
not be representative of the underlying data distribution, so they should not have too much influence on the model.  

## Geometric margin:

The geometric margin is the distance between the decision boundary (i.e., hyperplane) and the closest data point, normalized by the length of the weight vector w. 
Mathematically, the geometric margin is given by:  

**margin_i = y_i * (w*x_i + b) / ||w||**

Note that the geometric margin is always positive, regardless of the true label y_i. Therefore, the geometric margin is a better measure of the model's generalization
ability than the functional margin.  

To find the optimal hyperplane based on the geometric margin, we want to maximize the minimum geometric margin of all the data points. Mathematically, this can be 
represented as:  

**maximize min_i(y_i * (w*x_i + b) / ||w||)**

**subject to ||w|| = 1**
where ||w|| is the Euclidean norm of the weight vector w.

## LINEAR AND NON-LINEAR SVM

Linear SVM is used when the data is linearly separable, which means that there exists a straight line or a hyperplane that can completely separate the data points into their respective classes. In linear SVM, the decision boundary is a straight line or a hyperplane, and the classification is based on which side of the decision boundary the data point falls on.

Non-linear SVM is used when the data is not linearly separable, which means that there is no straight line or hyperplane that can completely separate the data points into their respective classes. In non-linear SVM, the decision boundary is a non-linear function of the input features, and the classification is based on which side of the decision boundary the data point falls on.  

## The primal and dual problem in SVM  

SVMs work by finding the hyperplane that maximizes the margin between the support vectors of different classes. The optimization problem that SVMs solve can be formulated as both a primal problem and a dual problem.

The primal problem in SVM is to minimize the following optimization problem:

**minimize ½||w||² + CΣξ**

**subject to yi(w · xi + b) ≥ 1 - ξi, and ξi ≥ 0**

where w is the weight vector, b is the bias term, ξ is the slack variable, C is the regularization parameter, and (xi, yi) are the training examples.

This problem seeks to find the weight vector w, bias term b, and slack variable ξ that minimize the margin between the support vectors of different classes while minimizing the classification error on the training set. The regularization parameter C controls the trade-off between maximizing the margin and minimizing the classification error. The solution to the primal problem gives us the optimal hyperplane that separates the data points into their respective classes.

The dual problem in SVM involves finding the Lagrange multipliers that define the support vectors and the hyperplane. The Lagrange multipliers are used to transform the primal problem into a dual problem, which is formulated as a maximization problem subject to the constraints that the Lagrange multipliers are non-negative and sum to zero. The Lagrange multipliers are used to compute the weight vector and bias term that define the optimal hyperplane.
The Lagrange multipliers are denoted by αi for each training example (xi, yi) and are used to maximize the Lagrangian function with respect to the weight vector w and bias term b. The Lagrangian function for the primal problem is:

**L(w, b, ξ, α, μ) = ½||w||² + CΣξ - Σαi(yi(w · xi + b) - 1 + ξi) - Σμiξi**

where ||w||² is the squared Euclidean norm of the weight vector w, C is the regularization parameter, ξi is the slack variable, and μi is the Lagrange multiplier associated with the ith slack variable.

The Lagrangian function is subject to the following constraints:

 **αi ≥ 0**  
 **Σαiyi = 0**

These constraints ensure that the Lagrange multipliers are non-negative and sum to zero, respectively.

The optimal solution for the primal problem can be obtained from the dual problem by using the Lagrange multipliers. The dual problem is computationally more efficient than the primal problem when the number of training examples is larger than the number of features. The dual problem also allows for non-linear SVMs through the use of kernel functions, which map the input features into a higher-dimensional space where the data is more likely to be linearly separable.  

##   NON-Linear SVM and Kernel Function  
 Non-linear SVM uses a **kernel function** to transform the data into a higher-dimensional space where a linear decision boundary can be found. The kernel function maps the data points into the new feature space without actually computing their coordinates. The most commonly used kernel functions are polynomial kernel, RBF kernel, and sigmoid kernel. The optimization problem for non-linear SVM is the same as that of linear SVM, but with the kernel function replacing the dot product in the decision function.
 ![m](https://user-images.githubusercontent.com/128781536/236613985-364b79f7-4632-4b3e-8992-3c4aef269cfc.JPG)   
 
 **Commonly-used kernel functions**  
 **Linear kernel:** K(xi, xj) = Xi.Xj

 **Polynomial of power p**: K(xi, xj) = (1 + xi.xj)^P

 **Sigmoid: K(xi,Xj)** = tanh(Bo(xi.xj) + Bi)

In general, functions that satisfy Mercer's condition can be kernel functions.


