# machine-learning-challenge

Based on Gridsearch of 3 models ( SVC, Tree, KNN ), it showed over 50% accuracy on each of model.

Gridsearch parameter and features that selected from data.
(All model used same target-y as koi_disposition)

For SVC model, I used parameters as C and gamma on gridsearch.
Selected features : koi_disposition, koi_period, koi_time0bk, koi_slogg

I used SVC model with linear kennel.
Best param and score was C : 1 and 0.0001. Best C of 1 means that there are many noise when we apply SVC and it conclude that this model is not clear to apply on this data.

For Tree model, I used parameters as criterion and max_depth on gridsearch.
Selected features : koi_disposition', 'koi_period', 'koi_time0bk', 'koi_slogg', 'koi_srad', 'ra', 'dec', 'koi_kepmag'

Gini and entropy is factor to choose which feature for splitting the nodes in subsets. 
Best criterion was Entropy which mean information theory is better for measuring impurity on this data.
Max depth of tree was 8. This criteria shows best max tree on this data. 


For KNN model, I used parameters as n_neighbors / weights / metric on gridsearch
Selected feature : koi_period

Best K value was 18 and which is way higher than default value of 5. 
It means that dataset doesn't have intuitive middle point for classify data trend. 


Conclusion : Based on model results none of this model fit for this dataset. 

