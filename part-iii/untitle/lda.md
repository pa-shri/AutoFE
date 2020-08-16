# LDA

Linear Discriminant Analysis \(LDA\) is a generalization of Fisher's linear discriminant, a method used in Statistics, pattern recognition and machine learning to find a linear combination of features that characterizes or separates two or more classes of objects or events. This method projects a dataset onto a lower-dimensional space with good class-separability to avoid overfitting \(“curse of dimensionality”\), and to reduce computational costs. The resulting combination may be used as a linear classifier or, more commonly, for dimensionality reduction before subsequent classification.

The original Linear discriminant was described for a 2-class problem, and it was then later generalized as “multi-class Linear Discriminant Analysis” or “Multiple Discriminant Analysis” by [C. R. Rao in 1948](http://www.jstor.org/stable/2983775?seq=1#page_scan_tab_contents) \(The utilization of multiple measurements in problems of biological classification\)

In a nutshell, the goal of an LDA is often to project a feature space \(a dataset nn-dimensional samples\) into a smaller subspace kk \(where k≤n−1k≤n−1\), while maintaining the class-discriminatory information. In general, dimensionality reduction does not only help to reduce computational costs for a given classification task, but it can also be helpful to avoid overfitting by minimizing the error in parameter estimation.

