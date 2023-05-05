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

