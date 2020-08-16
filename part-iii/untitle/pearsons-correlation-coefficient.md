# Pearson's correlation coefficient

This test can be applied for feature selection in classification as well as regression problems. The Pearson correlation coefficient is a classical relevance index used for individual feature ranking. We denote $$xj$$ the 'm' dimensional vector containing all the values of the jth feature for all the training examples, and by 'y' the 'm' dimensional vector containing all the target values. The Pearson correlation coefficient is defined as:

![](https://lh6.googleusercontent.com/28PLsvh9xfJ0PEKdHonnWrLAJwSIbwSL6q1HPPO2vImZFCPZpP1RBovAgm3N45PvnZw5jDA3wRh9pS2UbBPYLiKxpiZqhFPCVC3bzqnz6_9wAjNal7Xa8Pr-gMQpvoFuVxDOfRS0)

where the bar notation stands for an average over the index i. This coefficient is also the absolute value of the cosine between vectors xi and y, after they have been centered \(their mean subtracted\). For multiclass problems, Fisher coefficient methods can be used.

