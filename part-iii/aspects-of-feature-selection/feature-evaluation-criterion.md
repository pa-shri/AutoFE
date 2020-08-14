# Feature Evaluation criterion

There are two common approaches to feature selection:

**Univariate Feature selection:** This approach is based on the ranking of features according to their individual relevance. Such univariate feature ranking methods are usually fast and effective for large dataset. Univariate feature selection approach is limited in scope because:

* the individually irrelevant features may become relevant in the context of others
* individually relevant features when combined together might have redundancies

One of the most common method to perform univariate feature selection is **Pearson correlation coefficient**. 

**Multivariate feature selection:** Multivariate Feature selection takes into account the underlying feature dependencies to achieve potentially better results than univariate feature selection. In multivariate feature selection, features subsets are ranked rather than individual filters. There also exist multivariate relevance criteria to rank individual features according to their relevance in the context of others. It also takes into account feature redundancy and yield more compact subsets.

The **Relief method** is the classical method for performing multivariate filter.

