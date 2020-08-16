# Normalization \(or Min-Max Scaling\)

In normalization, the data is scaled to a fixed range - \[0,1\] or \[-1,1\]. The selection of target range depends on the nature of data.  


For instance, let _x_ is an image and _xi’_s are the number of pixels with color _i_, it makes sense to normalize _x_ by dividing it by the total number of counts in order to encode the distribution and remove the dependence on the size of the image.

![Fig2.2: Normalization](../.gitbook/assets/image%20%2813%29.png)

‌This can be done using the formula:

![](https://wikimedia.org/api/rest_v1/media/math/render/svg/358923abc154221bb5022fc329061f6fc4dcc69f)

The downside is of this method is, smaller standard deviation resulting in the suppressed effect of outliers.  


