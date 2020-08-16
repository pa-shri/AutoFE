# Implementation of AutoFeat for FE

```text
# instantiate the model
model = AutoFeatRegressor()

# fits the model and returns a pandas DataFrame with the original and new transformed features. These new features can then be used to generate predictions or can directly be used to train other models.
df = model.fit_transform(X, y)

# predict the target for new test data points
y_pred = model.predict(X_test)

# compute the additional features for new test data points # (e.g. as input for a different model)
df_test = model.transform(X_test)
```



**Additional Resources:**

{% embed url="https://www.youtube.com/watch?v=4-4pKPv9lJ4&feature=emb\_title" %}

\*\*\*\*

