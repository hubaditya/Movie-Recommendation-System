# Movie-Recommendation-System
 A movie recommendation system based on user-userm item-item collaborative filtering and matrix factorization of user-movie rating matrix
 
 ### Motivation
 Businesses often rely on personalization and customization of their products and services for the end users that they are more likely to engage in. If built in the right way, they can leverage this information to recommend the user betters which puts the users as well as the business in the win-win scenario.
This project tries to breakdown the mechanism that some of the companies like Netflix potentially use to recommend movies to users.

### Problem Statement
Given a user-movie rating matrix, create a recommendation tool for users that they are more likely to rate the recommended movie higher

### Data Dictionary

| Column            | Description         | Data Type |
|:---               |:---                 |:----------|
| user_id     | user represented as a unique identifier      | Integer   |
| movie_id      | movie represented as a unique identifier   | Integer   |
| rating     | rating given by the user for the movie        | Integer   | 
| unix_timestamp     | timestamp when the user rated the movie   | Integer   |

### Technical Details

#### Libraries
* pandas and numpy - for data wrangling and mathematical operations
* matplotlib and seaborn - for rich data visualizations
* sklearn - for calculating pairwise distances

#### Modeling
* User-user collaborative filtering
  * created a pearson similarity score between each user with movie ratings given as features and did a dot product with the rating given by each user for that movie 
  * sorted the dot product score in descending order for each user that that particular user should watch
* Item-item collaborative filtering
  * created a pearson similarity score between each movie with users as features and did a dot product with the rating given to each movie by that user
  * sorted the dot product score in descending order for each movie that that particular movie should be recommended to
* Matrix-Factorization

#### Evaluation
The model from matrix-factorization got a mean squared error of 225


#### Result
The user-movie rating matrix with each cell value filled with historical rating and predicted rating
