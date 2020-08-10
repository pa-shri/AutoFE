# Part II - Feature Extraction

Data is represented by a fixed number of features which can be binary, categorical or continuous. We can describe feature construction as,

let X is an n-dimensional pattern vector, X = \[x1,x2,...,xn\], which after transformation returns X’, a vector of transformed features of dimension n’.  
  


The commonly used operators based on the feature type are:  


Boolean features: Conjunction, disjunction and negation

Nominal feature: Cartesian product, M of N

Numerical features: Min, Max, Multiplication, Division, Addition, Subtraction, Inequality and Equivalence.  


After applying the above transformations, the space dimensionality of the dataset may change. For example, non-linear expansions, feature discretization may enlarge the feature set, whereas, space embedding methods may reduce it.  


