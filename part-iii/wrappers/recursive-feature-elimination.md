# Recursive Feature Elimination

It is a greedy optimization algorithm which aims to find the best performing feature subset. It repeatedly creates models and keeps aside the best or the worst performing feature at each iteration. It constructs the next model with the left features until all the features are exhausted. It then ranks the features based on the order of their elimination.

The method, given that one wishes to employ only σ0 &lt; n input dimensions in the final decision rule, attempts to find the best subset of size σ0 by a kind of greedy backward selection. It operates by trying to choose the σ0 features which lead to the largest margin of class separation, using an SVM classifier. This combinatorial problem is solved in a greedy fashion at each iteration of training by removing the input dimension that decreases the margin the least until only σ0 input dimensions remain.



