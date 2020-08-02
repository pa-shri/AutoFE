# Untitled

**Part II: Feature Construction/Transformation:**

Data is represented by a fixed number of features which can be binary, categorical or continuous. To describe feature construction let x is an n dimensional pattern vector,

x = \[x1,x2,...,xn\]. Which after transformation returns x’, a vector of transformed features of dimension n’.

Feature transformations may include following operations:

**Standardization :**

For features having different scales but refer to same comparable objects. For instance, a pattern x = \[x1,x2\] where x1 is a width in meters and x2 is height in centimeters. Both can be compared, added or subtracted but not before appropriate normalization. The following classical centering and scaling of the data is often used

X’ = \(xi - ui\)/sigmai where ui and sigmai are mean and standard deviation of feature xi over training examples respectively.

**Normalization:**

_\(Add explanation and other example_\) Let x is an image and xi’s are the number of pixels with color i, it makes sense to normalize x by dividing it by total number of counts in order to encode the distribution and remove the dependence on the size of the image.

This can be done using formula : x’ = x/\|\|x\|\|

**Extraction of local features:**

For sequential, spatial or other unstructured data, specific techniques like convolution methods using hand crafted kernels or syntactical and structural methods are used. These techniques encode problem specific knowledge into the features . They can bring significant improvement\(can be discussed in detail in appendix\)

**Linear and non-linear space embedding methods:**

When the dimensionality of the data is already pretty high, techniques like PCA\(Principal Component Analysis\), LDA\(Linear Discriminant Analysis\) and MDS\(Multidimensional scaling\) are used to project or embedded the data into lower dimensional space while retaining as much information as possible.

**Non-linear expansions:**

When the problem is very complex and first hand interaction is not enough to derive good results, it is better to increase the dimensionality. \(Find different example\).

This consists of instance in computing products of the original features xi to create monomials xk1, xk2,.... Xkp

**Feature discretization:**

Sometimes to simplify data description and improve data understanding, It makes sense to discretize continuous data into finite discrete set. \(add example\)

**Signal enhancement:**

This involves improving signal-to-noise ratio by applying signal or image-processing filters. These operations include baseline background removal, de-noising , smoothing, or sharpening. The Fourier transform and wavelet transforms are popular methods.

After applying above transformations, the space dimensionality of the dataset may change. For example, non-linear expansions, feature discretization may enlarge the feature set, whereas, space embedding methods may reduce it.

\#Example of feature construction, also FC for Boolean,Nominal,Numerical

