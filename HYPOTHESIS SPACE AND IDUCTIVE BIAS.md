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

## hypothesis space  
Hypothesis space is a key concept in inductive learning, which refers to the set of all possible hypotheses or models that can be used to explain a given dataset.  
In other words, the hypothesis space defines the range of functions or relationships that can be learned by a machine learning algorithm. 
 
In inductive learning, the representation of functions refers to how the machine learning algorithm represents the mapping between input features and output variables. The choice of function representation can have a significant impact on the performance of the algorithm and its ability to generalize to new, unseen data.

The function representation can be thought of as a hypothesis about the underlying relationship between the input and output variables. The goal of the machine learning algorithm is to find the best hypothesis or function that fits the training data while also generalizing well to new, unseen data.

a)Linear functions: Linear functions are commonly used to represent the relationship between continuous input features and a continuous output variable. A linear function takes the form y = w1x1 + w2x2 + ... + wn xn + b, where w1, w2, ..., wn are the weights associated with each input feature, and b is a bias term.  
![lin_func](https://miro.medium.com/max/970/1*PxrWV2vIZulpE6ID9JPzrQ.png)

b)Decision trees: Decision trees are a type of function representation that can be used to model both continuous and categorical input features. A decision tree consists of a tree-like structure where each node represents a decision based on one or more input features, and the branches represent the possible outcomes of that decision. The leaves of the tree represent the final output values.
c)Neural networks: Neural networks are a type of function representation that are used for a wide range of machine learning tasks. A neural network consists of layers of interconnected nodes or neurons, where each neuron applies a non-linear transformation to its input and passes the result to the next layer. The output of the final layer represents the predicted output value.
