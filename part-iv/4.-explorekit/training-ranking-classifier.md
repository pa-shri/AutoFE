# Training Ranking Classifier:

To train the classifier we need a large labeled training set.

The steps to train the Ranking Classifier are as follows:

1. For training dataset, generate a set of candidate features

2. Generate meta-features for each candidate feature

3. assigning labels \(“good” or “bad”\) to each candidate feature generated for the training dataset.

A more computationally-expensive \(wrapper\) feature evaluation method is used to determine the error reduction obtained by applying the classifier on the joint set of initial features and the candidate features.

If the error declines by more than the threshold, the candidate features are labeled as “good” and “bad” otherwise.

These labels are assigned to the meta-features and the labeled meta-feature set is used to train the Ranking Classifier.  




