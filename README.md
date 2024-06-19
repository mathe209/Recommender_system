# Recommender_system
This repository holds my solution to the 2024 FNB Data quest
## Collaborative Filtering
In this solution, I utilize the user-to-user collaborative filtering method. This is where the assumption that similar users have similar likes holds.
The original data has multiple columns but I have decided to use only the column that holds the targets for simplicity
### Data Normalization
The initial solution uses a mean-centering approach where we simply subtract the mean of each row from each entry in that row
Subsequent solutions will look at other methods of normalization such as min-max-centering for example to see how the result may change
#### User-item Matrix
The original dataset is in long form and it has to be changed to a wide format
From the user-item matrix, I can compute the user-user similarity matrix using Pearson's correlation
