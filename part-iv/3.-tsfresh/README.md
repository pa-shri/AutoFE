---
description: Automated FE for time-series data
---

# 3. TsFresh \(Time Series Feature Extraction on the basis of Scalable Hypothesis tests\)

![Fig4.4: TsFresh](../../.gitbook/assets/screen-shot-2020-08-15-at-7.32.42-pm.png)



Time Series data exists throughout multiple facets of society such as the stock price of a company over a duration of time or the meteorological conditions of a city. The availability of cheap sensors and advancing connectivity has led to an increase in availability of temporal data.

Time Series Feature Engineering is a time-consuming process as the Data Scientist or engineers have to consider the multifarious algorithms of signal processing and time series analysis for identifying and extracting meaningful features from time series.

**TsFresh \(Time Series Feature Extraction on the basis of Scalable Hypothesis tests\)** is an open-source python package for automatically extracting a large number of meaningful features for time series data. TsFresh provides a highly parallel feature selection algorithm based on statistical hypothesis tests, which by default are configured automatically depending on the type of supervised machine learning problem\(classification/ regression\) and feature type\(categorical/ continuous\). This package implements standard APIs of time series and machine learning libraries \(like pandas and scikit learn\) and is designed for exploratory analysis as well as straightforward integration into operational data science applications.

TsFresh is based on the **FRESH** algorithm.

It is the only python library available for this type of data. There is a Matlab package called '[hctsa\(highly comparative time-series analysis\)](https://github.com/benfulcher/hctsa)' which can be used to automatically extract features from time series. It is also possible to use hctsa from within python by means of the [pyopy](https://github.com/strawlab/pyopy) package.  


![Fig4.5: highlevel overview of steps in tsfresh](https://lh5.googleusercontent.com/K53sYYLxo2p0fWd8f3R6_Xe5tz_HfSeSf-Kjuql961Qjaa8P1fRqkNTS7CwDFIeswMiI918ycoWic4J-5h3iO64QBBQX_QBmbkdgRcorB8TOyeWZr65H-QLHH8JLu7rAp-_cfqWw)

As shown in above figure TsFresh involves 3 steps:

1. Feature Extraction
2. P-value calculation
3. Multiple test procedure

