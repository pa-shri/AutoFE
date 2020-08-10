# Feature Selection:

After having generated thousands of features, the optimal feature subset needs to be selected. Before starting feature selection, all the features that are highly correlated with the original or simpler features are removed.

Autofeat uses a wrapper method-based approach to perform multi-variate feature selection. The Lasso LARS linear regression model and the L1-regularized logistic regression model are used to choose features based on sparse weights. It uses a ‘noise filtering approach’ by training the model using the original features and the noise features and selecting only those features that have a model coefficient greater than the largest coefficient of the noise features. This approach works perfectly well when there is a sufficient number of features.

But, if the dataset has a large number of correlated features and the total number of features is greater than the data samples, an initial set of features is obtained by training the L1-regularized model on all features and selecting features with the largest absolute coefficients. This set is then combined with the chunk of features obtained by equally splitting the remaining features from initial feature selection by an L1-regularized linear model. A model is fit on each such chunk to select additional features. All feature subsets are then combined and used to train another model based on which the final feature set is determined. Finally, the independent feature selection subsets are combined and highly correlated features are filtered out \(keeping those features that were selected in the most runs\). The remaining features are then again used to fit a model to select the ultimate feature set.

Please have a look at the below image and the description for a better and detailed understanding of feature selection in autofeat.

![Fig: The heart of this feature selection algorithm. Given the feature matrix X with all candidate features H, the aim is to select a few informative features \(G\) that explain the target variable y. The set of good features G is adapted until a stable set of features is reached. First, promising features are identified by computing the correlation between the features and the target residual, and G is extended by those features with the largest absolute correlation until G contains up to n/2 features \(to guarantee numerical stability in the following regression step\). Next, the currently selected good features are used to train a Lasso LARS regression model, based on which the target residual is updated and the good features are filtered by retaining only those with a non-zero regression weight.](../../.gitbook/assets/image%20%281%29.png)



