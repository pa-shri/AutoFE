# Submodules:

TsFresh has a huge collection of submodules for different purposes. You can check them [here](https://tsfresh.readthedocs.io/en/latest/api/tsfresh.convenience.html). At the top level, the three most commonly exported submodules of tsfresh are:

* **extract\_features**
* **select\_features**
* **extract\_relevant\_features**

**Extract\_features:**

This module contains the main function to interact with tsfresh. It can be used as:

```python
tsfresh.feature_extraction.extraction.extract_features(timeseries_container, 
default_fc_parameters=None, kind_to_fc_parameters=None, column_id=None, 
column_sort=None, column_kind=None, column_value=None, chunksize=None, 
n_jobs=1, show_warnings=False, disable_progressbar=False, impute_function=None, 
profile=False, profiling_filename='profile.txt', profiling_sorting='cumulative', 
distributor=None)
```

#### Example:

```python
from tsfresh.examples import load_robot_execution_failures
from tsfresh import extract_features
df, _ = load_robot_execution_failures()
X = extract_features(df, column_id='id', column_sort='time')
```



**Select\_features:**

This module contains the filtering process for the extracted features. The filtering procedure can also be used on other features that are not based on time-series.

```python
tsfresh.feature_selection.selection.select_features(X, y, test_for_binary_target_binary_feature='fisher', 
test_for_binary_target_real_feature='mann', test_for_real_target_binary_feature='mann', 
test_for_real_target_real_feature='kendall', fdr_level=0.05, hypotheses_independent=False, 
n_jobs=1,show_warnings=False, chunksize=None, ml_task='auto')
```

**Example:**

```python
>>> from tsfresh.examples import load_robot_execution_failures
>>> from tsfresh import extract_features, select_features
>>> df, y = load_robot_execution_failures()
>>> X_extracted = extract_features(df, column_id='id', column_sort='time')
>>> X_selected = select_features(X_extracted, y)
```



**Extract\_relevant\_features:**

The most important function used is the [“extract\_relavant\_features”](https://tsfresh.readthedocs.io/en/latest/api/tsfresh.convenience.html) function from TSFRESH.  This function is labelled as a “convenience” package within TSFRESH because it extracts the features, imputes/removes missing data, and filters out irrelevant features at the same time.  There are 22 parameters that can be modified, but 3 must be specified at a minimum:

– timeseries\_container \([DataFrame](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.html)\): The dataframe with the time series data.

– y \([Series](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.Series.html) or [numpy.array](https://docs.scipy.org/doc/numpy/reference/generated/numpy.array.html)\): The target vector.

– column\_id \([str](https://docs.python.org/2.7/library/functions.html#str)\): The name of the id column to group by.

The “column\_sort” parameter is technically optional, but highly recommended.  This parameter is used to specify the column that contains values which can be used to sort the time series data \(e.g. time stamps\).  If you omit this column, the dataframe is assumed to be already sorted in increasing order.

As specified above, “y” \(“failures” in our case\) must be a pandas.Series or numpy.array to be used in the function.  Since it is currently a pandas.DataFame, it needs to be converted before it can be used \(outlined above in blue\), and the converted pandas.Series is named “failures\_tmp”.  The two parameters that need to be set are “data” and “index”, and the inputs need to be “array-like”.  This can be done by using the [pandas.values](https://pandas.pydata.org/pandas-docs/stable/generated/pandas.DataFrame.values.html) function.  Set the “data” parameter to be equal to the “no\_failure” column’s values, and then set the “index” parameter to the “id” column’s values.

```python
tsfresh.convenience.relevant_extraction.extract_relevant_features(timeseries_container, 
y, X=None, default_fc_parameters=None, kind_to_fc_parameters=None, 
column_id=None, column_sort=None, column_kind=None, column_value=None, 
show_warnings=False, disable_progressbar=False, profile=False, 
profiling_filename='profile.txt', profiling_sorting='cumulative', 
test_for_binary_target_binary_feature='fisher', test_for_binary_target_real_feature='mann', 
test_for_real_target_binary_feature='mann', test_for_real_target_real_feature='kendall', 
fdr_level=0.05, hypotheses_independent=False, n_jobs=1, distributor=None, 
chunksize=None, ml_task='auto')
```

**Example:**

```python
from tsfresh.examples import load_robot_execution_failures
from tsfresh import extract_relevant_features
df, y = load_robot_execution_failures()
X = extract_relevant_features(df, y, column_id='id', column_sort='time')
```



**Additional Resources:**

For more notebooks on tsfresh: [Github](https://github.com/pa-shri/tsfresh/tree/main/notebooks/examples) 

{% embed url="https://www.youtube.com/watch?v=Fm8zcOMJ-9E" %}





  


