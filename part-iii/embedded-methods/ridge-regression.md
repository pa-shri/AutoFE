# Ridge Regression

Ridge regression is a way to create a parsimonious model when the number of predictor variables in a set exceeds the number of observations, or when a data set has multicollinearity \(correlations between predictor variables\).

### Shrinkage

Ridge regression uses a type of shrinkage estimator called a _ridge estimator_. Shrinkage estimators theoretically produce new estimators that are shrunk closer to the “true” population parameters. The ridge estimator is especially good at improving the least-squares estimate when multicollinearity is present.

### Regularization

Ridge regression belongs a class of regression tools that use L2 regularization. The other type of regularization, **L1 regularization**, limits the size of the coefficients by adding an _L1 penalty_ equal to the absolute value of the magnitude of coefficients. This sometimes results in the elimination of some coefficients altogether, which can yield sparse models. **L2 regularization** adds an L2 penalty, which equals the square of the magnitude of coefficients. All coefficients are shrunk by the same factor \(so none are eliminated\). Unlike L1 regularization, L2 will _not_ result in sparse models.

A tuning parameter \(λ\) controls the strength of the penalty term. When λ = 0, ridge regression equals least squares regression. If λ = ∞, all coefficients are shrunk to zero. The ideal penalty is therefore somewhere in between 0 and ∞.

### On Mathematics

OLS regression uses the following formula to estimate coefficients:  
![ridge regression](https://www.statisticshowto.com/wp-content/uploads/2017/07/ridge-regression-1.png)  
  
If X is a centered and scaled matrix, the crossproduct matrix \(X\`X\) is nearly singular when the X-columns are highly correlated. Ridge regression adds a _ridge parameter_ \(k\), of the identity matrix to the cross product matrix, forming a new matrix \(X\`X + kI\). It’s called _ridge_ regression because the diagonal of ones in the correlation matrix can be described as a ridge. The new formula is used to find the coefficients:  
![](https://www.statisticshowto.com/wp-content/uploads/2017/07/rr2.png)  
  
**Choosing a value for** _**k**_ **is not a simple task,** which is perhaps one major reason why ridge regression isn’t used as much as least squares or logistic regression.

