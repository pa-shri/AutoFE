# Aspects of feature selection:

There are 3 aspects of the feature selection process:

* **Feature Search strategy**
* **Feature Evaluation criterion \(like relevance index or predictive power\)**
* **Feature Evaluation or assessment method**

### 1. Feature Search Strategy:

Once an evaluation method for the variable subsets has been defined, one can start the search for the best subset. A search strategy defines the order in which the variable subsets are evaluated. There are a wide variety of search options available such as:  
**Optimal search:**

* Exhaustive search
* Branch and bound

**Sequential search:**

* Sequential backward selection
* Sequential forward selection
* Beam search
* Floating search

**Stochastic search:**

* Simulated Annealing
* Genetic algorithm

### 2. Feature Evaluation based on relevance index or predictive power:

There are two common approaches to feature selection:

**Univariate Feature selection:** This approach is based on the ranking of features according to their individual relevance. Such univariate feature ranking methods are usually fast and effective for large datasets. The univariate feature selection approach is limited in scope because:

* the individually irrelevant features may become relevant in the context of others
* individually relevant features, when combined together might have redundancies

One of the most common methods to perform univariate feature selection is **Pearson's correlation coefficient**. 

**Multivariate feature selection:** Multivariate Feature selection takes into account the underlying feature dependencies to achieve potentially better results than univariate feature selection. In multivariate feature selection, features subsets are ranked rather than individual filters. There also exist multivariate relevance criteria to rank individual features according to their relevance in the context of others. It also takes into account feature redundancy and yields more compact subsets.

The **Relief method** is the classical method for performing the multivariate filter.

### 3. Feature Assessment method:

 This part aims to provide tools to statistically assess the relevance of the features and feature selection outcome. These methods can be integrated with wrappers and can also be used for filtering or feature ranking, hyper-parameter selection or model selection.

