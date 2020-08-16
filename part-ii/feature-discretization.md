# Feature discretization

Some algorithms do not handle continuous data well. At such times it is better to discretize continuous data into finite discrete sets. 

![Fig2.4: Discretization](../.gitbook/assets/image%20%2814%29.png)

Approaches to discretization:

**Supervised Approach**

* Discretization with decision trees

#### Unsupervised Approaches

* Equal-width discretization
* Equal-frequency discretization
* K-means discretization



**1.Discretization with decision trees:**

Discretization with decision trees consists of using a decision tree to identify the optimal **bins**.

Technically, when a decision tree makes a decision, it assigns an observation to one of **N** end leaves. Accordingly, any decision tree will generate a **discrete output**, which its values are the predictions at each of its **N** leaves.

Steps for discretization with decision trees

1. First, we train a decision tree of limited depth \(2, 3, or 4\) using only the variable we want to discretize and the target.
2. Second, we replace the variable’s value with the output returned by the tree.

\*\*\*\*

**2. Equal-width discretization:**

This is the most simple form of discretization—it divides the range of possible values into **N** bins of the **same width**.

The width of intervals is determined by the following formula:![Image for post](https://miro.medium.com/max/60/0*57RHdF-Nm4JhNl0U?q=20)![Image for post](https://miro.medium.com/max/1150/0*57RHdF-Nm4JhNl0U)

where **N** is the number of bins or intervals, this parameter is something to determine experimentally—there’s no rule of thumb here.

![Fig2.5: Equal width discretization](../.gitbook/assets/image%20%2815%29.png)

**3. Equal-frequency discretization:**

Equal-frequency discretization divides the scope of possible values of the variable into **N** bins, where each bin holds the **same number** \(or approximately the same number\) of observations.

![Fig2.6: Equal frequency discretization](../.gitbook/assets/image%20%2812%29.png)

**4. K-means discretization:**

This discretization method consists of applying k-means clustering to the continuous variable ****then each cluster is considered as a **bin**.



Reference: [https://heartbeat.fritz.ai/hands-on-with-feature-engineering-techniques-variable-discretization-7deb6a5c6e27](https://heartbeat.fritz.ai/hands-on-with-feature-engineering-techniques-variable-discretization-7deb6a5c6e27)

