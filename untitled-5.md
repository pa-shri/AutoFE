# Untitled

**2. AutoFeat:** \[7\]

AutoFeat is a scikit-learn style linear regression and classification model with automated Feature Engineering or selection capabilities. Unlike featuretools, autofeat is not meant for relational data. It is a general purpose library created for scientific use cases where all the data is stored in one single table. Autofeat also enables one to specify the units of measurement so as to avoid any creation of nonsensical features.

The autofeat library provides the ‘AutoFeatRegressor’ and ‘AutoFeatClassifier’ models, which automatically generate and select additional non-linear input features given the orig- inal data and then train a linear prediction model with these features

**Feature Construction:**

Non-linear features are generated in an alternating multi-step process by applying user selectable non-linear transformations to the features \(e.g. log\(x\), √x, 1/x, x2, x3, \|x\|, exp\(x\), 2x, sin\(x\), cos\(x\)\) and combining pairs of features with different operators \(+, −, ·\).

The new features are computed using the SymPy Python library \[8\], which automatically simplifies the generated mathematical expressions and thereby makes it possible to exclude redundant features. If the original features are provided with physical units, only ‘legal’ new features are retained, e.g., a feature representing a temperature would not be subtracted from a feature representing a volume of something. This is implemented using the Pint Python library,2 which is additionally used to compute several dimensionless quan- tities from the original features using the Buckingham π-theorem \[9\]. If categorical features are included in the original features, these are first transformed into one-hot encoded vec- tors using the corresponding scikit-learn model before using them in the main feature engineering procedure.

**Feature Selection:**

We first remove those engineered features that are highly correlated with the original or other simpler features and then employ a multi-step feature selection approach relying heavily on L1-regularized linear models. In addition to the AutoFeatRegressor and AutoFeatClassifier models, the library also provides only this feature selection part alone in the FeatureSelector class, which again provides a scikit-learn style interface.

Individual features can provide redundant information or they might seem uninformative by themselves yet proof useful in combination with others. Therefore, instead of ranking the features independently by some criterion, it is advantageous to use a wrapper method that considers multiple features at once to select a promising subset \[16\]. For this we use the Lasso LARS regression model \[3, 14, 15\] and an L1-regularized logistic regression model \[5, 11\] provided in the scikit-learn library, which yield sparse weights based on which the features can be chosen \[33\]. To select the features, we mainly rely on a noise filtering approach, where the model is trained on the original features, as well as several additional ‘noise’ features \(either created by shuffling the original data or randomly drawn from a normal distribution\), and only those of the original features are kept that have a model coefficient larger than the largest coefficient associated with any of the noise features \[22\].

Selecting relevant features with an L1-regularized model amongst a feature pool that contains more features than data samples works quite well when the features are independent \[12, 33\]. However, when trained with a large set of interrelated features, such as those generated in our feature engineering process, the models often fail to identify all of the truly relevant features. Therefore, we first identify an initial set of promising features by training an L1-regularized linear model on all features and selecting those with the largest absolute coefficients. Then, the remaining features are split into equal chunks and combined with the initial set \(such that each of the chunks contains less than n/2 features\) and a model is then fit on each chunk to select additional features. The feature subsets are then combined and used to train another model based on which a final feature set is determined. To get a more robust set of features, this selection process is performed multiple times on subsamples of the data. The feature subsets of the independent feature selection runs are then combined and highly correlated features are filtered out \(keeping those features that were selected in the most runs\). The remaining features are then again used to fit a model to select the ultimate feature set.

After this multi-step selection process, typically only a few dozen of the several thou- sand engineered features are retained and used to train the actual prediction model. For new test data points, the AutoFeatRegressor and AutoFeatClassifier models can then either generate predictions directly, or a DataFrame with the new features can be computed for all data points and used to train other models. By examining the coefficients of the linear prediction model \(possibly normalized by the standard deviation of the corresponding features, in case these are not of comparable magnitudes\), the most prominent influencing factors related to higher or lower values of the target variable can be identified.

**Implementation of autofeat:**

\# instantiate the model

model = AutoFeatRegressor\(\)

\# fit the model and get a pandas DataFrame with the original, \# as well as the additional non-linear features

df = model.fit\_transform\(X, y\)

\# predict the target for new test data points

y\_pred = model.predict\(X\_test\)

\# compute the additional features for new test data points \# \(e.g. as input for a different model\)

df\_test = model.transform\(X\_test\)

