# Approaches to Feature Engineering

From a broader perspective, there are 2 common approaches to perform Feature Engineering:

1. **Generate an exhaustively large feature pool and then perform feature selection.**
2. **Iteratively expand the original feature set by evaluating whether the inclusion of new features improves the prediction accuracy of the model.** 

Both these approaches have their own drawbacks: 

The first approach is very memory-intensive, especially when starting off with a large initial feature set from which the additional features are constructed via various transformations. 

With the second approach, important features might get missed if some variables are eliminated too early in the feature engineering process and can therefore not serve to construct more complex, possibly helpful features. Furthermore, depending on the strategy for including additional features, the whole process might either be very time-intensive, if at each step a model is trained and evaluated on the feature subset, or can fail to include the relevant features if a simple heuristic is used for the feature evaluation and selection.   


![](https://lh6.googleusercontent.com/Rcdv_-y0ucbrUWOoXpoT56GkUaAaOkZPonT5DjMehqSIH1YupQsMGQ-S6rC5n5BUoZQRW3d4bgtYXJ1B6Oj1XXrqjfwA_MAX6HegMK7BJ09AV4S0XWiREezo-_gVSh0zmwjjbyZf)

 Fig1: Feature engineering approaches  


Even though, most of the feature construction frameworks follow one of the two approaches discussed above. Some frameworks might also use more complex approaches \(like Cognito which is discussed later \). The recent trend is to use meta-learning i.e, algorithms trained on other datasets to decide whether to apply a specific transformation to a feature or not.

\#Add LFE approach by IBM team  


