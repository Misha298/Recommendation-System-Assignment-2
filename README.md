# Recommendation-System-Assignment-2


EDA: 

This file contains the analysis of the data, information on the data, and how the data was distributed.

Make_file_ready_to_process: (food-making-data-ready.ipynb)

We have considered only those users who have given a rating to more than 40 items. But some rating values are 0. For them, we counted the number of positive words and a number of negative words present in the review. According to them, we replace 0 with 2 - negative rating and 4 - positive rating values.

Memory_based_collaborative:  

In this file, we built a memory-based collaborative system to fill the missing values with the weighted average method. For weights, we assign their similarity as their weights and compute their ratings. After that, recipes with higher ratings are recommended to the user.

Model_based_collaborative: 

In this, we built a model-based collaborative system with matrix factorization with an inbuilt method and from scratch. In the inbuilt method, we used the SVD method to decompose the matrix. For scratch, we randomly initialized the U and V matrix. With the gradient descent, we U*(V.T) as similar to the rating matrix and computed the rating matrix to suggest the recipes with the higher rating for a particular user to users.
