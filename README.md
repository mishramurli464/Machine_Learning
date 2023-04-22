# Machine_Learning
There are three broad types of machine learning:

Supervised Learning: In supervised learning, the algorithm is trained on labeled data, where the input features and the corresponding output labels are provided. The   goal is to learn a mapping between the input features and the output labels. Examples of supervised learning include image classification, sentiment analysis, and   regression analysis.  

Unsupervised Learning: In unsupervised learning, the algorithm is trained on unlabeled data, where the input features are provided, but the corresponding output labels   are not. The goal is to find hidden patterns or structures in the data. Examples of unsupervised learning include clustering, dimensionality reduction, and anomaly   detection.  

Reinforcement Learning: In reinforcement learning, the algorithm learns by interacting with an environment, where it receives feedback in the form of rewards or   penalties based on its actions. The goal is to learn a policy that maximizes the cumulative reward over time. Examples of reinforcement learning include game playing,   robotics, and recommendation systems.  

## Types of Supervised Learning:  
**1)Classification**  
Classification is a type of supervised learning in which an algorithm is trained to predict a categorical output variable (also known as a label or class) based on    input  variables (also known as features). The goal of classification is to build a model that can accurately classify new instances into one of the predefined categories.  

**For example**, let's say we have a dataset of customer information for a bank, including features such as age, income, credit score, and whether they have a mortgage   or not. The goal is to predict whether each customer is likely to default on their loan payments or not. In this case, defaulting or not defaulting is the categorical    output variable, and the features are the input variables.  

To train a classification model, we would start by dividing the dataset into a training set and a test set. The training set would be used to train the model by   presenting it with labeled examples of customer data, with each example consisting of the features and the corresponding label (i.e., whether the customer defaulted or   not). The model would then learn to recognize patterns in the data that are associated with each label.  

Examples of classification problems include:  

**a)Spam filtering:** Given an email message, classify it as either spam or not spam.  
**b)Sentiment analysis:** Given a text document or social media post, classify it as either positive, negative, or neutral in sentiment.  
**c)Image recognition:** Given an image, classify it as one of several predefined categories, such as "cat," "dog," "car," or "tree."  

**2)Regression**  
Regression is a type of supervised learning in which an algorithm is trained to predict a continuous output variable based on input variables (also known as features). The goal of regression is to build a model that can accurately predict the value of the output variable for new instances based on their input features.

**For example**, let's say we have a dataset of housing prices, including features such as the number of bedrooms, square footage, location, and age of the house. The goal is to predict the price of a new house based on its features. In this case, the price is the continuous output variable, and the features are the input variables.

To train a regression model, we would start by dividing the dataset into a training set and a test set. The training set would be used to train the model by presenting it with labeled examples of housing data, with each example consisting of the features and the corresponding price. The model would then learn to recognize patterns in the data that are associated with housing prices.

Once the model is trained, we can evaluate its performance on the test set by measuring how accurately it predicts the prices of the test examples. We can also use the model to make predictions for new, unlabeled instances of housing data.

**Examples of regression problems include:**

**a)Stock price prediction:** Given historical data on a stock's price and other market indicators, predict the future price of the stock.
**b)Sales forecasting:** Given historical data on a company's sales and marketing efforts, predict the future sales of the company.
**c)Weather forecasting:** Given historical data on weather patterns and other meteorological factors, predict the future temperature or precipitation levels.
