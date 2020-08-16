---
description: Automated FE for general-purpose data
---

# 2. AutoFeat

[  
AutoFeat](https://arxiv.org/abs/1901.07329) is a python library that provides **scikit-learn** **style** linear regression and classification models with automated feature generation and selection capabilities. Unlike FeatureTools, autofeat is a general-purpose library created with scientific use cases in mind where all the experimental data is stored in a single table. Autofeat also allows specifying the units of measurement to avoid any creation of nonsensical features. For instance, specifying weight in$$pounds(lb)$$and distance in$$miles(m)$$can prevent the creation of any new feature combining weight and distance.

The autofeat library provides the **‘AutoFeatRegressor’** and the **‘AutoFeatClassifier’** models, which automatically generate and select non-linear input features given the original data and then train a linear prediction model with these features. This framework is inspired by the **SISSO** algorithm.

Along with AutoFeatRegressor and AutoFeatClassifier, the autofeat library also provides a [**FeatureSelector**](https://pypi.org/project/feature-selector/) class, which can directly be used to perform feature selection.



