# Part III - Feature Selection

Feature selection aims to find a small subset of useful features by removing noisy, irrelevant and redundant features. A large number of features not only make algorithms slow, but also degenerate the performance of the learning task and lead to difficulty on interpretability of the model. Feature selection can lead to:

* dimensionality reduction, limiting storage requirements and increase algorithm speed
* performance improvement
* improved model interpretability

Feature selection process can be categorized based on label information and based on feature selection technique.

1**. Based on the label availability:**

* Supervised
* Semi-supervised
* Unsupervised

In case of supervised learning, we have a well-labeled dataset that allows effective search for discriminative and relevant features to distinguish samples from different classes. When there is only a small portion of labeled data is available, semi-supervised learning is able to take advantage of both labeled and unlabeled data. Semi-supervised algorithms mostly rely on similarity matrix and only select features that best fit this similarity matrix. Unsupervised learning is considered a much harder problem due to unavailability of guiding features.

2. Based on the feature selection technique:

* Filters
* Wrappers
* Embedded methods

Filter methods are known to select features based on their rank. They order features based on their relevance index and then select the features with the highest ranks. They do not improve the performance of the predictive model. Some of the filter-based methods are correlation coefficient\(assess the degree of dependence of input variables with the target variables\), statistics methods like T-test, F-test, Chi-Squared. Wrappers also use rank-based approach, they select the features according to their predictive power based on their score using some learning algorithm. Embedded methods select features in the process of training. Embedded methods and wrappers may yield very different feature subsets under small perturbations of the dataset. Ensemble methods are used to minimize this effect and improve feature set stability.

