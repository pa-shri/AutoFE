# Some Important concepts

**Features:** Data is usually represented by a fixed number of features that can be binary, categorical or continuous. A Feature is synonymous to the attribute or variable or column in a dataset. Example of features:

![](../.gitbook/assets/image%20%2810%29.png)

The image above contains a snippet of data from [a public dataset](https://github.com/awesomedata/awesome-public-datasets/blob/master/Datasets/titanic.csv.zip) with information about passengers on the ill-fated Titanic maiden voyage. Each feature, or column, represents a measurable piece of data that can be used for analysis: Name, Age, Sex, Fare, and so on.

In character recognition: features may include histograms counting the number of black pixels along the horizontal and vertical directions, number of internal holes, stroke detection.

In speech recognition: features for recognizing phonemes can include noise ratios, length of sounds, relative power, filter matches.

In spam detection algorithms: features include the presence or absence of certain email headers, the email structure, the language, the frequency of specific terms, the grammatical correctness of the text.

In computer vision: features include edges and objects.

**Feature relevance:** A feature is relevant if it contains some information about the target. Kohavi and John \(1996\) give a simple and intuitive definition of relevance that is sufficient for the purpose of feature selection: a feature X is relevant in the process of distinguishing class Y = y from others if and only if for some values X = x for which P\(X = x\) &gt; 0 the conditional probability P\(Y = y\|X = x\) is different than the unconditional probability P\(Y = y\).

**Overfitting:** Poor generalization of a model accompanied by high accuracy on the train**i**ng data is called overfitting and is often caused by too large complexity of the model \(too many adaptive parameters\). The danger of “overfitting” is to find features that “explain well” the training data, but have no real relevance or no predictive power. 

![](../.gitbook/assets/image%20%286%29.png)

The green line represents an overfitted model and the black line represents a regularized model. While the green line best follows the training data, it is too dependent on that data and it is likely to have a higher error rate on new unseen data, compared to the black line.

\*\*\*\*

**Curse of dimensionality:** The _curse of dimensionality_, first introduced by Bellman \[[1](https://link.springer.com/referenceworkentry/10.1007%2F978-0-387-39940-9_133#CR1_133)\], indicates that the number of samples needed to estimate an arbitrary function with a given level of accuracy grows exponentially with respect to the number of input variables \(i.e., dimensionality\) of the function.

Let’s take an example below. Fig. 1 \(a\) shows 10 data points in one dimension i.e. there is only one feature in the data set. It can be easily represented on a line with only 10 values, x=1, 2, 3... 10.

But if we add one more feature, same data will be represented in 2 dimensions \(Fig.1 \(b\)\) causing increase in dimension space to 10\*10 =100. And again if we add 3rd feature, dimension space will increase to 10\*10\*10 = 1000. As dimensions grows, dimensions space increases exponentially.

```text
   10^1 = 10

   10^2 = 100

   10^3 = 1000 and so on...
```

![Curse of dimensionality](https://www.kdnuggets.com/wp-content/uploads/curse-dimensionality-2.png)

This exponential growth in data causes high sparsity in the data set and unnecessarily increases storage space and processing time for the particular modelling algorithm. Think of image recognition problem of high resolution images 1280 × 720 = 921,600 pixels i.e. 921600 dimensions. And that’s why it’s called [**Curse of Dimensionality**](https://www.kdnuggets.com/?s=curse+of+dimensionality). The value added by the additional dimension is much smaller compared to the overhead it adds to the algorithm.

Bottom line is, the data that can be represented using 10 space units of one true dimension, needs 1000 space units after adding 2 more dimensions just because we observed these dimensions during the experiment. The true dimension means the dimension which accurately generalize the data and observed dimensions means whatever other dimensions we consider in dataset which may or may not contribute to accurately generalize the data.

The second issue that arises is related to sorting or classifying the data.  In low dimensional spaces, data may seem very similar but the higher the dimension the further these data points may seem to be.  The two wind turbines below seem very close to each other in two dimensions but separate when viewed in a third dimension. This is the same effect the curse of dimensionality has on data.

![](https://images.deepai.org/glossary-terms/curse-of-dimensionality-5166894.jpg)

