# Recommendation System
By Victor Mwatu

<div>
<center><img src="imageO_O (1).jpg" height="300"/></center>
</div>

### Summary

This is a project whose goal is the creation of a machine learning algorithm that gives movie recommendations based on their ratings of movies in a dataset, which in this case was the Movielense dataset. 

The dataset contains several files but the ones of interest will are the ratings file containing the user ratings and the movies file with movie names.

The dataset after importing to Pandas Dataframe format has no missing values and only the timestamp field is drop as it is not relevant. A surprise dataset object is then created which will be used with the Surprise python library for recommendation systems.

Next operation is the creation of a simple baseline modelling process. It is achieved using a loop that loops through several simple memory based models and a simple basic SVD model for validating. The best performing model turns out to be the simple SVD with an RMSE of 0.877 and the worst is the KNN-basic with RMSE of 0.977. After that an SVD model is optimised using GridsearchCV to produce an optimum parameter model which is trained on the rest of the data. The final model had a RMSE of around 0.86 which is lower than that of the baseline.

A new user's data is merged with the dataset and compiled. The model is then able to provide user ratings for other movies and by selecting the movies with the highest ratings the user can be recommended top movies.
