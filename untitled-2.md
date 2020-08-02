# Untitled

**Univariate vs Multivariate feature selection:**

**Univariate FS:**

Univariate Feature Selection ranks features according to their individual relevance. These methods are fast and effective when the number of training data is less and the number of features is comparatively large\(100:10000\).

Univariate feature ranking works well in situations where one feature is relevant individually and the other is not providing any help for better class separation. In such a case, the feature that provides good class separation will rank high and will be chosen.

Following Feature Selection criterias can be used:

Pearson correlation coefficient

T-test Statistics

Naive Bayes

But there are limitations to the univariate feature ranking because the features that are not individually relevant may become relevant when combined with others or the features that are individually relevant may not be useful because of possible redundancies. That is why we have, ‘multivariate’ feature selection methods.

**Multivariate FS:**

Multivariate Feature selection takes into account the underlying feature dependencies to achieve potentially better results than univariate FS.

Feature Selection criteria/Method:

Relief method

Greedy Methods\(forward selection and backward elimination\)

**1. Assessment Methods:**

This topic aims to provide an overview of the tools required to statistically assess the relevance of the features and use in feature selection. These methods can be integrated in feature selection wrappers and can also be used for filtering or feature ranking.

In such frameworks, feature selection consists of setting a threshold r0 and making the decision that all the candidates with relevance index less than r0 should be discarded.

**1.1 Univariate statistical tests:**

**1. Tests for binary classification problems:**

**T-test:**

For classification problem with classes A and B. Let us assume that the distribution of examples of both classes is Gaussian. As a univariate ranking index, we will use a test statistic to compare the means μA and μB of the two Gaussian distributions in projection on a given variable. The paired T-statistic performs that task; a realization t of the statistic T is given by:

![](.gitbook/assets/2.png)

where mA and mB are the number of examples of each distribution, and sA and sB the estimation of the standard deviations of the distributions obtained from the available examples. Under the null hypothesis that the means are equal, T has a Student distribution with mA + mB − 2 degrees of freedom. Clearly, a variable for which the means of the two Gaussians are further apart is more informative. Since the polarity of the classes is interchangeable, it does not matter which mean is larger than the other. The absolute value of the T-statistic may be used directly as a ranking index: the larger its value, the more informative the feature. But the two-tailed p-value of t, which varies monotonically with abs\(t\), may be also used as a ranking index. The smaller the p-value of the feature, the larger the discrepancy between the means, hence the more informative the feature. One can then set a threshold on the p-value above which features are considered statistically significant.

**Wilcoxon test and AUC criterion:**

If the assumption that the distribution of features is Gaussian does not hold, then a non-parametric test, the Wilcoxon-Mann-Whitney rank sum test can be conducted.

\#explanation remaining

**2. Other tests:**

**Pearson correlation coefficient:**

This test can be applied for feature selection in both classification as well as regression problems. The Pearson correlation coefficient is a classical relevance index used for individual feature ranking. We denote by xj the m dimensional vector containing all the values of the jth feature for all the training examples, and by y the m dimensional vector containing all the target values. The Pearson correlation coefficient is defined as:

![](.gitbook/assets/3.png)

where the bar notation stands for an average over the index i. This coefficient is also the absolute value of the cosine between vectors xi and y, after they have been centered \(their mean subtracted\). For multiclass problems, Fisher coefficient methods can be used.  


**ANOVA:**

For the problems in which the input is categorical and the output is continuous or vice-versa, ANOVA test is used.

**1.2 Multivariate test for feature subset selection:**

**Fisher’s test for backward elimination**

**Random probe test for orthogonal forward regression ranking**

**Filter Methods:**

Feature ranking and feature selection algorithms may roughly be divided into three types.

The first type encompasses algorithms that are built into adaptive systems for data analysis \(predictors\), for example feature selection that is a part of embedded methods \(such as neural training algorithms\).

Algorithms of the second type are wrapped around predictors providing them subsets of features and receiving their feedback \(usually accuracy\). These wrapper approaches are aimed at improving results of the specific predictors they work with.

The third type includes feature selection algorithms that are independent of any predictors, filtering out features that have little chance to be useful in analysis of data. These filter methods are based on a performance evaluation metric calculated directly from the data, without direct feedback from pre- dictors that will finally be used on data with reduced number of features.

What is the relevance of a feature?

Kohavi and John \(1996\) give a simple and intuitive definition of relevance that is sufficient for the purpose of feature se- lection: a feature X is relevant in the process of distinguishing class Y = y from others if and only if for some values X = x for which P\(X = x\) &gt; 0 the conditional probability P\(Y = y\|X = x\) is different than the unconditional probability P\(Y = y\). Moreover, a good feature should not be redundant, i.e. it should not be correlated with other features already selected.

**Correlation based filtering:**

**Based on distance between distributions:**

**Based on information theory:**

**Decision tree for filtering:**

\*\*\*\*

