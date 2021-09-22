### Abstract

The goal of this project was to generate a music genre classifier. My goal with this project was to use audio features provided by Spotify to create a classifer that can accuratly classify the music genre. I will be taking a look at the performance of several different algorithms to see which I can get to perform best in terms of accuracy. 

### Design
 For new artists it's important to know your own genre to help ensure your music is reaching your target audience. However, in today's music industry genres are dynamic and are often classified based off of feelings instead of logic and reason.
 
### Data

The dataset consisted of over 50,000 songs pulled from spotify using the spotify API. The data was scrubbed to ensure the songs we had were classified into a "normal" genre (not one of Spotify's many niche genres such as "in the car." In addition to the songs, all the audio features of the songs were pulled from Spotify as well. This included 13 features such as "energy", "danceability", and "loudness." 

### Algorithms

Feature Engineering:
1. Using for loop to find best k value for KNN 
2.Using for loop to find best n_estimator value for Random Forest

Models

The three models I attempted to use were KNN, Logistic Regression and Random Forest. In the end I decided to go with Random Forest since it performed best and accuracy is what I was aiming for with my problem. Additionally KNN proved to be difficult to work with given the size of my dataset. Since logistic regression does not optimize accuracy, it did not seem like the ideal option. 

When it came to Random Forest, I performed an 80/20 train, test split on my data. I then performed bootstraping with Random Forest with n_estimator equal to 100. Different numbers of estimators made very little difference in performance. I left the class weight as the default for my final model. I did attempt to run it with a balanced weight, but the balanced model actually performed worse than the default. 


The accuracy on the training data was high (as expected) of .99 while the test accuracy was significantly less with a .437 accuracy. 

### Tools 
Numpy,Pandas, 
Scikit-learn,
Matplotlib and Seaborn
