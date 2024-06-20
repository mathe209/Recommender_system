# Recommender_system
This repository holds my solution to the 2024 FNB Data quest.
The challenge is to create a 'personalized' recommendation system that will recommend a certain item to a user based on another user's behavior.

## Collaborative Filtering
In this solution, I utilize the user-to-user collaborative filtering method. This is where the assumption that similar users have similar likes holds.
The original data has multiple columns but I have decided to use only the column that holds the targets for simplicity.
There are 7 item types to recommend and several ways to interact with these items. The interaction column is used in only trimming the data in this solution.

### Data Normalization
The initial solution uses a mean-centering approach where we simply subtract the mean of each row from each entry in that row.
Subsequent solutions will look at other methods of normalization such as min-max-centering for example to see how the result may change.

#### User-item Matrix and Similarity scores
The original dataset is in long form and it has to be changed to a wide format.
From the user-item matrix, I can compute the user-user similarity matrix using Pearson's correlation.
The first approach calculates the scores of each item by multiplying the similarity score for each item by the item rating/count and then computes the average score for that item.
##### Recommendations
The first method uses the average score for each item and recommends the topK items to the user, 2 in this case.
