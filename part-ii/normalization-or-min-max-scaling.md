# Normalization \(or Min-Max Scaling\):

In normalization, the data is scaled to a fixed range - \[0,1\] or \[-1,1\]. The selection of target range depends on the nature of data.  


For instance, let x is an image and xi’s are the number of pixels with color i, it makes sense to normalize x by dividing it by total number of counts in order to encode the distribution and remove the dependence on the size of the image.

‌

This can be done using formula:



![](https://lh3.googleusercontent.com/A_SCMUynyIJHrNjxjd4k4zEK_UIOcqKobe9blXumH1RSp6kEpxy5SZpLmft0Fhzu441UERNKmX5AXDvDjZ2v02m8cTarJhtQoIsdwGAtLXsT7nyhTTLWIwc2rOFXs4GR3HlFoaCw)

The downside is of this method is smaller standard deviation resulting in the suppressed effect of outliers.  


