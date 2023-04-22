## Inductive learning  
Inductive learning is a type of machine learning that involves the process of learning patterns or regularities in data and making predictions based on those patterns.
In inductive learning, the machine learning algorithm works by analyzing a set of training data, which contains examples of input-output pairs, and then inferring a 
general rule or pattern that can be used to make predictions on new, unseen data.
**examples**
1)Spam filtering  
2)Handwriting recognition  
3)Predictive modeling  

## TERMINOLOGY
Features: The number of features or distinct traits that can be used to describe each item in a quantitative manner.  
Feature vector: n-dimensional vector of numerical features that represent some object  
Instance Space X: Set of all possible objects describable by features.each instance is the point in the features space    
Example (x,y): Instance x with label y=f(x).  
Concept c: Subset of objects from X (c is unknown).  
Target Function f: Maps each instance x EX to target label y EY  
Example (x,y): Instance x with label y=f(x).  
Training Data S: Collection of examples observed by learning algorithm.  
![termilogy](https://ds055uzetaobb.cloudfront.net/image_optimizer/6aaeb27b0fd954d9232de5a9142eb1dc658ea8a1.jpg)

## Representation
In inductive learning, the representation of functions refers to how the machine learning algorithm represents the mapping between input features and output variables. The choice of function representation can have a significant impact on the performance of the algorithm and its ability to generalize to new, unseen data.  
The function representation can be thought of as a hypothesis about the underlying relationship between the input and output variables. The goal of the machine learning algorithm is to find the best hypothesis or function that fits the training data while also generalizing well to new, unseen data.

a)Linear functions: Linear functions are commonly used to represent the relationship between continuous input features and a continuous output variable. A linear function takes the form y = w1x1 + w2x2 + ... + wn xn + b, where w1, w2, ..., wn are the weights associated with each input feature, and b is a bias term.  
![lin_func](https://miro.medium.com/max/970/1*PxrWV2vIZulpE6ID9JPzrQ.png)  

b)Decision trees: Decision trees are a type of function representation that can be used to model both continuous and categorical input features. A decision tree consists of a tree-like structure where each node represents a decision based on one or more input features, and the branches represent the possible outcomes of that decision. The leaves of the tree represent the final output values.  
![dec_tree](https://assignmentpoint.com/wp-content/uploads/2016/05/Decision-Tree-Learning.jpg)   

c)Neural networks: Neural networks are a type of function representation that are used for a wide range of machine learning tasks. A neural network consists of layers of interconnected nodes or neurons, where each neuron applies a non-linear transformation to its input and passes the result to the next layer. The output of the final layer represents the predicted output value.  
![neu_net](https://mlatcl.github.io/deepnn/slides/diagrams/convnets/fc_s.png)
## Hypothesis space  
Hypothesis space is a key concept in inductive learning, which refers to the set of all possible hypotheses or models that can be used to explain a given dataset.  
In other words, the hypothesis space defines the range of functions or relationships that can be learned by a machine learning algorithm.   
Hypothesis space is represented by **H** and **h** represents any single hypothesis.  

## Size of Hypothesis Space  
In inductive learning, the size of the hypothesis space refers to the number of possible functions or models that can be used to explain a given dataset. A larger   hypothesis space means that there are more possible functions or models that can fit the data, while a smaller hypothesis space means that there are fewer possible   functions or models that can fit the data.  
If there are 4(N) input features, there are 2^16 (2^2^N) possible Boolean functions.  
We cannot figure out which one is correct unless we see every possible input-output pair 2^4(2^N)  

## inductive bias  
In inductive learning, bias in the hypothesis space refers to the tendency of the machine learning algorithm to prefer certain functions or models over others, even when both functions or models fit the training data equally well. The bias in the hypothesis space is typically introduced by the choice of function representation and the specific learning algorithm used to optimize the model parameters.
**Inductive bias** is a key concept in inductive learning that refers to the set of assumptions or biases that a machine learning algorithm makes about the underlying data and the function that maps the input features to the output variable. Inductive bias is necessary because it helps the algorithm to generalize from the training data to new, unseen data.
**Two types of bias:**
**Restriction:** Restriction bias refers to the limitations or assumptions imposed on the hypothesis space by the machine learning algorithm. For example, if a linear function is used to represent the mapping between input features and output variables, the hypothesis space will be restricted to linear models, and non-linear models will be less likely to be selected as the optimal function. Similarly, if a decision tree is used to represent the mapping, the hypothesis space will be restricted to decision trees.(Limit the hypothesis space)
**Preference:** Preference bias, on the other hand, refers to the tendency of the machine learning algorithm to prefer certain functions or models over others, even when both functions or models fit the training data equally well.For example, if the algorithm uses a L1 regularization term, the model will be biased towards sparse solutions, where many of the model parameters are set to zero. Similarly, if the algorithm uses a squared loss function, the model will be biased towards minimizing the mean squared error, even if other loss functions might be more appropriate for the specific problem.



