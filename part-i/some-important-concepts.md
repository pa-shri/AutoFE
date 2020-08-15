# Few Important concepts

### 1. **Features:** 

Data is usually represented by a fixed number of features that can be binary, categorical or continuous. A Feature is synonymous to the attribute or variable or column in a dataset. Example of features:

![Table2: Titanic voyage data](../.gitbook/assets/image%20%2810%29.png)

The image above contains a snippet of data from [a public dataset](https://github.com/awesomedata/awesome-public-datasets/blob/master/Datasets/titanic.csv.zip) with information about passengers on the ill-fated Titanic maiden voyage. Each feature or column represents a measurable piece of data that can be used for analysis: Name, Age, Sex, Fare, and so on.

Example of features in different contexts:

**In character recognition:** features may include histograms counting the number of black pixels along the horizontal and vertical directions, number of internal holes, stroke detection.

**In speech recognition:** features for recognizing phonemes can include noise ratios, length of sounds, relative power, filter matches.

**In spam detection algorithms:** features include the presence or absence of certain email headers, the email structure, the language, the frequency of specific terms, the grammatical correctness of the text.

**In computer vision:** features include edges and objects.



### **2. Feature relevance:** 

A feature is relevant if it contains some information about the target. [Kohavi and John \(1996\) ](https://pdf.sciencedirectassets.com/271585/1-s2.0-S0004370200X00331/1-s2.0-S000437029700043X/main.pdf?X-Amz-Security-Token=IQoJb3JpZ2luX2VjEOv%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEaCXVzLWVhc3QtMSJIMEYCIQC%2BRfZigMieGYgS9BC%2BmnuC%2FduJghepu1g4FMNGsdcHBAIhAK3TGSYO59bYjqJH7pvxsbr6e%2BGe9secB5JymeX3IpHSKr0DCMP%2F%2F%2F%2F%2F%2F%2F%2F%2F%2FwEQAxoMMDU5MDAzNTQ2ODY1Igxr8KZAAW44zhFsGEcqkQOYwWmuP5mI7T1%2BtGUp7OJK7Tg0axRXk%2FleDTAKdqtwKyStn0tPEWfzuP332I7HoRxGw9zqjWRdNEnoDN%2B59GWKYhp3YJpV9Un4UFxZHnbG6XXpVuG5N2%2BNdpZi%2Bx%2F5tk88Ygl%2F0YIKSQ%2FDwlGTXfFv8awky3Qt6Zs0%2F1UwOtag0%2BP37zEN%2FyIx5ij4h%2F%2BvQmnGRrrX3cW0sASNv6O3AZL8NnEouwKUEZOVVmh67MoGbWK6y3jccBVlrwMk7UoCAinsSRJbB%2Fax%2FixbnguAI07YA7T1Moc4vaxLtm0z7rsDHgDvJrO5cKhJjEEegC1T3ztM878%2FyR%2Feg6H8xRrueKdYchAAZ%2Fa1XYkjVWmcwj9pu%2F%2BFxlYh%2FDMyh8FHgrdpskZhQfZFxrD49Sok9OQaylAfwMyQG9mNpmisiHtzOoNO7JiYj0itzXfba%2BWH2OFcWJlz7TioAqAFBwVMY%2BE4OmDF3ZmISN3dXr%2BQ116S00TcUfmehok%2Fex0s7P5LTCo%2FqMOx3hFbHdY7sZUFwIXHbXt78jCuyuD5BTrqAXNWrzW8G5jTYuQNcoPb15THBxyYdwyQEJ1Ke71k5FqLOP5K4GiYlVS%2B4w5FoCRwJU5gWmCf%2FlKjoYQ%2B2ySnJLjJFf0lTvj7NWNBg%2F2IxZhOeIrUzolKUMPb6V8WF0vGXF0XhD8JHeTdpAGqWZrU28h7mmX6bgor6%2BHbAYZYWLy27xi80HXcFuyvD8DBjus7mkfsGSMrM33fk6k%2BdxIbJ8AnZ2C3awZvox2Hbwjc7X1adH5zTqKct294XeMzGSplsHP331dM7lILD2gXwQaIsc2LGKRCOmnJKSuagJ60Ta%2FYxEndz0sb9sz2FA%3D%3D&X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Date=20200815T194943Z&X-Amz-SignedHeaders=host&X-Amz-Expires=300&X-Amz-Credential=ASIAQ3PHCVTYW7JB533F%2F20200815%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Signature=cf6aea595b2bcfbb513904a04bb25ae2a928212cd71a55b346479e7cb5ec0427&hash=3337486e48d12c159516530a0aeb8a07af41f9583176b086f33d751dfcca520a&host=68042c943591013ac2b2430a89b270f6af2c76d8dfd086a07176afe7c76c2c61&pii=S000437029700043X&tid=spdf-ad1a029e-efec-4181-8fc3-4def060ca17a&sid=c799262c325f984a150b51c73c4d1dbe5e9bgxrqa&type=client)give a simple and intuitive definition of relevance that is sufficient for the purpose of feature selection: '_a feature X is relevant in the process of distinguishing class Y = y from others if and only if for some values X = x for which P\(X = x\) &gt; 0 the conditional probability P\(Y = y\|X = x\) is different than the unconditional probability P\(Y = y\)._'

\*\*\*\*

### **3. Overfitting:** 

Poor generalization of a model accompanied by high accuracy on the train**i**ng data is called overfitting and is often caused by too much complexity of the model \(too many adaptive parameters\). The danger of overfitting is to find features that “explain well” the training data but have no real relevance or no predictive power. 

![Fig : Overfitiing of data](../.gitbook/assets/image%20%286%29.png)

In the above image, the green line represents an overfitted model and the black line represents a regularized model. While the green line best follows the training data, it is too dependent on that data and it is likely to have a higher error rate on new unseen data, compared to the black line.

\*\*\*\*

### 4. Curse of **D**imensionality: 

The curse of dimensionality, first introduced by Bellman \[[1](https://books.google.com/books?hl=en&lr=&id=iwbWCgAAQBAJ&oi=fnd&pg=PR9&ots=bDKcWkI84i&sig=5vw6p1z3z0fWrFgihVtnPwZeeII#v=onepage&q&f=false)\], indicates that the number of samples needed to estimate an arbitrary function with a given level of accuracy grows exponentially with respect to the number of input variables \(i.e., dimensionality\) of the function.

Let’s take an example below. Fig.\(a\) shows 10 data points in one dimension i.e. there is only one feature in the data set. It can be easily represented on a line with only 10 values, x=1, 2, 3... 10.

But if we add one more feature, same data will be represented in 2 dimensions \(Fig. \(b\)\) causing an increase in dimension space to 10\*10 =100. And again if we add 3rd feature, dimension space will increase to 10\*10\*10 = 1000. As dimensions grow, dimensions space increases exponentially.

```text
   10^1 = 10

   10^2 = 100

   10^3 = 1000 and so on...
```

![Fig: Curse of dimensionality](https://www.kdnuggets.com/wp-content/uploads/curse-dimensionality-2.png)

This exponential growth in data causes high sparsity in the data set and unnecessarily increases storage space and processing time for the particular modelling algorithm. Think of image recognition problem of high resolution images 1280 × 720 = 921,600 pixels i.e. 921600 dimensions. The value added by the additional dimension is much smaller compared to the overhead it adds to the algorithm.

Bottom line is, the data that can be represented using 10 space units of one true dimension, needs 1000 space units after adding 2 more dimensions just because we observed these dimensions during the experiment. The true dimension means the dimension which accurately generalizes the data and observed dimensions means whatever other dimensions we consider in the dataset which may or may not contribute to accurately generalize the data.

The second issue that arises is related to sorting or classifying the data.  In low dimensional spaces, data may seem very similar but the higher the dimension the further these data points may seem to be. For instance, the two wind turbines below seem very close to each other in two dimensions but separate when viewed in a third dimension. This is the same effect the curse of dimensionality has on data.

![](https://images.deepai.org/glossary-terms/curse-of-dimensionality-5166894.jpg)





