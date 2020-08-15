# TsFresh Process overview

![](../../.gitbook/assets/image%20%285%29.png)





![](../../.gitbook/assets/image%20%284%29.png)



First, the “timeseries” and “failures” data files are read in. Next, the data is moved into the “Execute Python” operator where code executing a TSFRESH function is used. After that, the data is joined together, and roles are set inside of the “Data Preparation” subprocess. Finally, the data is modelled inside of the “Cross Validation” operator using the Logistic Regression Operator, the model is applied to test data using the “Apply Model” operator, and the performance of the model is checked using the “Performance \(Binomial Classification\)” operator.

