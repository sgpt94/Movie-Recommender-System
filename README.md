# Movie-Recommender-System
### Implementing the collaborative filtering learning algorithm to recommend movies to a user.
#### Platform: MATLAB

Please refer to the "**main.m**" file

The dataset consists of ratings on a scale of 1 to 5.
The dataset has nu = users, and nm = 1682 movies

I have implemented the function **cofiCostFunc.m** that computes the collaborative filtering objective function and gradient. 
After implementing the cost function and gradient, I have used **fmincg.m** to learn the parameters for collaborative filtering.

The **matrix Y** (a num_movies * num_users matrix) stores the ratings y(i,j) (from 1 to 5). The **matrix R** is an binary-valued indicator 
matrix, where R(i, j) = 1 if user j gave a rating to movie i, and R(i, j) = 0 otherwise. The objective of collaborative filtering 
is to predict movie ratings for the movies that users have not yet rated, that is, the entries with R(i, j) = 0. This will
allow us to recommend the movies with the highest predicted ratings to the user.


After we have finished implementing the collaborative filtering cost function and gradient, we can now start training our 
algorithm to make movie recommendations for ourself.
You can enter your own movie preferences, so that later when the algorithm runs, you can get your own movie recommendations! 
I have filled out some values according to my own preferences, but you can change this according to your own tastes. 
The list of all movies and their number in the dataset can be found listed in the file **movie_idx.txt**.

After the additional ratings have been added to the dataset, the script will proceed to train the collaborative filtering model. 
This will learn the parameters **X** and **Theta**. The next part of the script computes the ratings for all the movies and 
users and displays the movies that it recommends, according to ratings that were entered earlier in the script.
