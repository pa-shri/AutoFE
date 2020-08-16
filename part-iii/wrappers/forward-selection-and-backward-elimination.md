# Forward Selection and Backward Elimination

#### Forward Selection

The heuristic behind forward selection is very simple. We first try out all subsets with only one attribute and keep the best solution. But instead of trying all possible subsets with two features next, we only try specific 2-subsets. We try the 2-subsets which contain the best attribute from the previous round. If we do not improve, we stop and deliver the best result from before, i.e. the single attribute. But if we have improved the accuracy, we continue trying by keeping the best attributes so far and try to add one more. We continue this until we no longer have to improve.

What does this mean for the runtime for our example with 10 attributes from above? We start with the 10 subsets of only one attribute which is 10 model evaluations. We then keep the best performing attribute and try the 9 possible combinations with the other attributes. This is another 9 model evaluations then. We stop if there is no improvement or keep the best 2-subset if we get a better accuracy. We now try the 8 possible 3-subsets and so on. So, instead of going brute force through all 1,023 possible subsets, we only go through 10 + 9 + … + 1 = 55 subsets. 

#### Backward Elimination

Things are similar with backward elimination, we just turn the direction around. We begin with the subset consisting of all attributes first. Then, we try to leave out one single attribute at a time. If we improve, we keep going. But we still leave out the attribute which led to the biggest improvement in accuracy. We then go through all possible combinations by leaving out one more attribute. This is in addition to the best ones we already left out. We continue doing this until we no longer improve. Again, for 10 attributes this means that we will have at most 1 + 10 + 9 + 8 + … + 2 = 55 combinations we need to evaluate.

