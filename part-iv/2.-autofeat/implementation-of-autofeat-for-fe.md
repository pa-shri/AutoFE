# Implementation of AutoFeat for FE

\# instantiate the model

model = AutoFeatRegressor\(\)

\# fits the model and returns a pandas DataFrame with the original and new transformed features. These new features can then be used to generate predictions or can directly be used to train other models.

df = model.fit\_transform\(X, y\)

\# predict the target for new test data points

y\_pred = model.predict\(X\_test\)

\# compute the additional features for new test data points \# \(e.g. as input for a different model\)

df\_test = model.transform\(X\_test\)  


