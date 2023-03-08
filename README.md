# Recommendation-System-Assignment-2


__EDA_on_food_dataset__ 

This file contains the analysis of the data, information on the data, and how the data was distributed.</br>
--> Preprocessing of the Data</br>
Some columns like nutritional values and ingredients are read as strings by python rather than list objects.</br>
We will now convert ingredients to list objects so that we can use them as iterables while text processing.</br>
We will convert nutritional values column to columns of nutritional values so that we can use them for comparision of different recipes nutritional values.</br>
Coverting nutritional values column to columns of nutritional values</br>
--> EDA</br>
There are many outliers, so we should remove outliers</br>
checking for NAN Values</br>
removing duplicates</br>
creating sparse matrix from data frame


__Make_file_ready_to_process: (food-making-data-ready.ipynb)__

We have considered only those users who have given a rating to more than 40 items. But some rating values are 0. For them, we counted the number of positive words and a number of negative words present in the review. According to them, we replace 0 with 2 - negative rating and 4 - positive rating values.

## __Memory_based_collaborative:__

In this file, we built a memory-based collaborative system to fill the missing values with the weighted average method. For weights, we assign their similarity as their weights and compute their ratings. After that, recipes with higher ratings are recommended to the user.
In this we have 2 main types of memory-based collaborative filtering algorithms: User-Based and Item-Based. 
In User-based we have subsampled our data to 50% while in item-based method we have subsampled our data to 5%. we did these because computation of similarity matrix on full data was not possible.
we have also use some pre-processing to have only active users in our final datset for training.

## __Model_based_collaborative:__

In this, we built a model-based collaborative system with matrix factorization with an inbuilt method and from scratch. In the inbuilt method, we used the SVD method to decompose the matrix. For scratch, we randomly initialized the U and V matrix. With the gradient descent, we U*(V.T) as similar to the rating matrix and computed the rating matrix to suggest the recipes with the higher rating for a particular user to users.
