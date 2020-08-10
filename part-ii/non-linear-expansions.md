# Non-linear expansions:

  
****

![](https://lh4.googleusercontent.com/V1T6W4PT_gM0IK2oI_Q75F_WVlwVEFKysPrdAdrXZnvckvZ7IbQxTOt9AUOIF4V_QO-UYw4hLYi5Ptnd7ciowcbw-xUp38exGUJN0mWmR3TkvrSXwlzx51bQEHZW7CI9AcVwmrc4)

**‌**When the data is not linearly separable, it is preferable to increase the dimensionality of the data.

For instance, SVM is quite intuitive when the data is linearly separable. However, when it is not, SVM is extended to perform well. The first step to non-linear generalization of SVM is, transformation of original training data into higher dimensional data using non-linear mapping. The next step involves finding a linear separating hyperplane in the new space.

So, if X1 and X2 are 2 original features, the polynomial transformation is expanded to \(X1, X2, X1^2,X2^2,X1X2\) and the hyperplane would be of the form

θ0+θ1X1+θ2X2+θ3X12+θ4X22+θ5X1X2=0  
****

