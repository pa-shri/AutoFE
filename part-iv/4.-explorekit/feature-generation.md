# Feature generation:

Explorekit feature generation is based on the intuition that the most informative features are often obtained from manipulation of the elementary ones. Gilad, Shin and Song in their paper on ‘**Explorekit: Automatic Feature Generation and Selection**’ claims that they have identified a set of common operators that can be applied individually or in combination to maximize the predictive performance of the model. Unary, Binary and Higher order operators are applied to obtain the candidate feature set. 

The steps to generate features are as follows:

1. **Unary operators:** applied on all possible features in the feature set\(Fu,i\)

**Discretization:** It is used to transform continuous and datetime features into a discrete one. Explorekit implements _EqualRange_ discretization\(partition the range of values of the features into X equal segments\) for numerical features and daytime features into DayOfWeek/MonthOfYear/IsWeekend, etc.

**Normalization:** To fit the scale of continuous \(i.e. numeric\) features to specific distributions \(range\[0,1\]\)

2. **Binary and Higher-order operators**: applied on the unified set Fi ∪ Fu,i\(Fo,i\)

**Binary:** arithmetic operators\(+,−,×,÷\)

**Higher-order:** SQL based operations\(GroupByThenMax, GroupByThenMin, GroupByThenAvg, GroupByThenStdev and GroupByThenCount\)

3. Once again apply unary operators on all the final features  




