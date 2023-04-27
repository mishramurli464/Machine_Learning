# CURSE OF DIMENSIONALIST 
The curse of dimensionality refers to the fact that as the number of input variables or features in a machine learning model increases, the amount of data needed to   learn accurately increases exponentially. This is because the volume of the input space increases exponentially with the number of dimensions, making it difficult   for the model to identify patterns and relationships within the data.  

Suppose we have a dataset of 1,000 images, where each image is 28x28 pixels (i.e., 784 pixels in total). We want to train a neural network to classify these images   into 10 different categories (e.g., cat, dog, car, airplane, etc.).  
Now, let's imagine that we decide to add a new feature to each image: the average pixel intensity. This means we now have 785 input features instead of 784. At first   glance, adding just one additional feature might not seem like a big deal. However, the curse of dimensionality tells us that as we add more and more features, the   amount of data needed to learn accurately increases exponentially.  
To see this, let's consider what happens if we add another new feature to each image: the standard deviation of the pixel intensities. This means we now have 786 input  features instead of 785.  
If we plot the number of training examples required to achieve a certain level of accuracy as a function of the number of input features, we might see a trend   
like this:

**784 features:** 500 training examples needed to achieve 90% accuracy  
**785 features:** 1,000 training examples needed to achieve 90% accuracy  
**786 features:** 2,000 training examples needed to achieve 90% accuracy  
**787 features:** 4,000 training examples needed to achieve 90% accuracy  
...
As we can see, the amount of data needed to achieve a certain level of accuracy increases rapidly as we add more features. This is the curse of dimensionality in action.  
## FEATURE REDUCTION
Feature reduction is the process of reducing the number of input variables or features used in a machine learning model while still retaining the most important    
information. The goal of feature reduction is to improve model efficiency, reduce overfitting, and improve the interpretability of the model  
### FEATURE SELECTION
Feature selection is the process of selecting a subset of relevant features (variables or input data) from a larger set of potential features, to be used  
in a machine learning model. The goal of feature selection is to reduce the dimensionality of the data, improve model performance, and reduce overfitting. 

Suppose we have a dataset consisting of a set of features X = {x1, x2, ..., xn} and a target variable y. The goal of a machine learning model is to learn a function f(X) that maps the input features X to the target variable y, i.e., f(X) = y.  

**Filter and wrapper methods are two common approaches to feature selection in machine learning.**

**i)Filter methods:**
Filter methods are feature selection techniques that select features based on their statistical properties, such as correlation, mutual information, or statistical significance. These methods evaluate the relevance of each feature independently of the learning algorithm and select a subset of features that have the highest correlation with the target variable. Filter methods are computationally efficient and can handle high-dimensional datasets, but they may miss important feature interactions that can improve the model's performance.

**Example:** One example of a filter method is correlation-based feature selection, which measures the correlation between each feature and the target variable and selects the features with the highest correlation. For example, in a dataset of medical records, we may find that blood pressure, cholesterol levels, and age are the most correlated features with the target variable, and we can select these features for further analysis.

**Wrapper methods:**
Wrapper methods are feature selection techniques that select features by evaluating the performance of a learning algorithm on different subsets of features. These methods use a learning algorithm to search for the optimal subset of features that maximizes the model's performance, and they can capture feature interactions that may be missed by filter methods. However, wrapper methods are computationally expensive and may overfit the model to the training data.

**Example:** One example of a wrapper method is recursive feature elimination (RFE), which recursively removes the least important features and re-trains the model on the remaining features until the desired number of features is reached. For example, in a dataset of customer reviews, we may use RFE to select the most informative features for sentiment analysis, such as the presence of certain words and phrases, the length of the review, and the number of positive and negative words.

Forward and reverse selection algorithms are two popular filter-based feature selection techniques for selecting uncorrelated features.  

**Forward selection:**
Forward selection is a feature selection algorithm that starts with an empty feature set and iteratively adds features one at a time, selecting the feature that maximizes the performance of the learning algorithm. The algorithm stops when the desired number of features is reached or when further feature additions do not improve the model's performance.

**Example:** In a dataset of medical records, we may use forward selection to select the most informative features for predicting a particular disease. We would start with an empty feature set and add features one at a time, evaluating the performance of the learning algorithm after each feature addition. We may start with age as the first feature, and if this improves the model's performance, we would add the next most informative feature, such as blood pressure, and continue until the desired number of features is reached.

**Reverse selection:**
Reverse selection is a feature selection algorithm that starts with the full feature set and iteratively removes features one at a time, selecting the feature that has the least impact on the performance of the learning algorithm. The algorithm stops when the desired number of features is reached or when further feature removals do not improve the model's performance.

**Example:** In the same dataset of medical records, we may use reverse selection to select the most informative features for predicting a particular disease. We would start with the full feature set and remove features one at a time, evaluating the performance of the learning algorithm after each feature removal. We may start by removing the least informative feature, such as weight, and continue until the desired number of features is reached.
###  Pearson correlation coefficient
In the context of feature selection, Pearson correlation coefficient is used to measure the correlation between each feature and the target variable. Features with a high correlation with the target variable are more likely to be informative and should be retained, while features with a low correlation can be discarded.
The Pearson correlation coefficient, denoted by the symbol r, ranges from -1 to +1, where -1 indicates a perfect negative correlation, +1 indicates a perfect positive correlation, and 0 indicates no correlation. A value of 1 indicates that the two variables move in the same direction, while a value of -1 indicates that the two variables move in opposite directions.

In the context of feature selection, Pearson correlation coefficient is used to measure the correlation between each feature and the target variable. Features with a high correlation with the target variable are more likely to be informative and should be retained, while features with a low correlation can be discarded.

Example: In a dataset of student grades, we may use Pearson correlation coefficient to identify the most informative features for predicting the final grade. We would calculate the correlation between each feature, such as the student's attendance, homework scores, and exam scores, and the final grade. If we find that the attendance and homework scores have a high positive correlation with the final grade, while the exam scores have a low correlation, we can select the attendance and homework scores as the most informative features and discard the exam scores.   

## FEATURE EXTRACTION
In machine learning, feature extraction is the process of selecting and transforming raw input data into a set of features that can be used as input for learning algorithms. Feature extraction is a crucial step in machine learning because it can greatly impact the performance and accuracy of the resulting model.  

![feat_selection](http://byclb.com/TR/Tutorials/neural_networks/ch5_1_dosyalar/image005.jpg)  

**Principal Component Analysis (PCA)**  
Principal Component Analysis (PCA) is a widely used technique in machine learning for feature extraction. It is a statistical technique that is used to reduce the dimensionality of a dataset while retaining most of the information present in the original data. PCA works by finding a set of new variables, called principal components, that are linear combinations of the original features.

The first principal component is the linear combination of the original features that accounts for the most variance in the data. The second principal component is the linear combination of the original features that accounts for the most variance after accounting for the first principal component, and so on.

PCA is a mathematical technique for feature extraction that finds a set of linearly uncorrelated and orthogonal principal components that account for most of the variance in the data. PCA can be used to reduce the dimensionality of a dataset and improve the performance of learning algorithms.  

![pca](https://vitalflux.com/wp-content/uploads/2020/08/Screenshot-2020-08-08-at-7.07.26-PM-768x255.png)  
The above fig shows. that the first pc is chosen based on the largest variance and the second pc if it is uncorrelated with the first feature  so its orthigonal to the first   

PCA can also be used for image reduction, which is a common application of dimensionality reduction in image processing. In this context, the goal is to reduce the dimensionality of an image while preserving its essential features.

Let's say you have a grayscale image with 1000 pixels, each pixel represented by a value ranging from 0 to 255. This image can be represented as a 1000-dimensional vector, which is high-dimensional and difficult to analyze.

To reduce the dimensionality of the image using PCA, we compute the principal components of the image matrix. The first principal component represents the direction in which the pixel values vary the most across all images. The second principal component represents the direction orthogonal to the first principal component that captures the most variation, and so on.

By retaining only the top k principal components, we can reduce the dimensionality of the image matrix from 1000 to k while retaining most of the variability in the image. This is equivalent to compressing the image while preserving its essential features.

To reconstruct the compressed image, we multiply the compressed image matrix by the transpose of the principal component matrix and add back the mean value of each pixel. This produces an approximation of the original image with reduced dimensionality.

The quality of the compressed image depends on the number of principal components retained. Retaining more principal components results in a higher quality approximation of the original image, while retaining fewer principal components results in a lower quality approximation.  





