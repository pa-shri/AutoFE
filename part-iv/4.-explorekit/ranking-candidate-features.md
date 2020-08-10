# Ranking Candidate Features:

The Novel ML-based approach generates a set of meta-features for each candidate feature and then the Ranking Classifier assigns a score to each candidate feature.

Types of meta-features:

1. **Dataset based meta-features:** Every dataset has multiple characteristics that may affect the likelihood of the candidate features being effective.

**General information:** General statistics \(like the number of instances and classes, stats on size\)

**Initial evaluation:** Stats on the current performance of classifier when applied on an initial set of features\(like AUC, log loss and precision value\)

**Entropy-based measures:** Grouping initial features based on the type\(discrete, numeric, date-time\) and then calculate stats on information gain of the features

**Feature diversity:** Using Chi-squared and T-test to calculate similarity. Using test stats to create meta-features.

2. **Candidate based meta-features:** Represent interaction of candidate features w.r.t initial features

**Entropy and statistical tests for the candidate feature:** use the chi-squared and paired t-tests to derive statistics on candidate features correlation to each group\(type-based group\) also derive entropy-based measures

**General information on parent features and operators:** stats representing the type of each parent feature, the range of possible values, and the number and type of operators used.

**Ranking Candidate Features:** derive statistics on the inter-correlation of the parent features as well as their correlation with the remaining features of the initial feature set.  




