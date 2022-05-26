# ML-driven-Personalized-Gourmet

This project is aimed at easing out the user experience of a customer who seems to be indecisive about what they want and also help business owners ameliorate their businesses.

<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/Restaurants-in-Brewster-MA.png" width = 700><p>
  
  ## Table of Contents

- [Problem Statement](#problemstatement)
- [Understanding the  Data](#understandingthedata)
- [Solution Architecture](#architecture)
- [Data Exploration](#EDA)
- [Features that constitute the solution](#features)
- [Algorithms Used](#algo)
- [Results](#results)
- [Evaluation metrics](#evaluation)
- [Challenges Faced](#challenges)
- [Future Scope](#futurescope)
- [References](#references)
- [Contact Me](#contact)  
  

***
<a id='problemstatement'></a>
## Problem Statement
In a world where food delivery is done within minutes, finding the right restaurant based on a user’s taste takes a lot more time with the plethora of options. In addition, every restaurant is judged by the customer reviews and ratings. The intention of this project is to build a recommendation system for restaurants in Philadelphia, based on the past experiences and reviews of a particular user. **The hybrid recommendation engine which is a combination of matrix factorization and cosine similarity will be used to solve this problem. This project also aims at providing the restaurant owners, the insights into what is working well and what can be improved which could help the restaurant retain the good services and improvise on the flawed ones**. Also a technique called sentiment analysis is used to provide insights about the social sentiment pertaining to the restaurant.

<a id='understandingthedata'></a>  
## Understanding the data
I have pulled the datasets using the Yelp API endpoint https://api.yelp.com/v3/businesses/search. 
The datasets that I designed for this project are:
  
1) Restaurant information dataset
  
2) Restaurant reviews dataset
  
3) Users dataset

Below are the Schemas of the JSON structure of each of the dataset that I have prepared:
  
**Restaurant Information Dataset**
  
<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/restaurant_new.png" width = 700><p>  
  
**Restaurant Reviews Dataset**
  
<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/reviews_new.png" width = 700><p>
  
**Users Dataset**
  
<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/users.png" width = 700><p>
  
<a id='architecture'></a>
## Solution Architecture
  
<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/architecture.png" width = 700><p>  

1) Data Retrieval - Python API programming from the Yelp API endpoint.
2) Business logic - Pyspark SQL, Pyspark MLlib, Pandas,Pymongo.
3) Storage mechanisms - MongoDB Atlas Cloud, HDFS.
4) Data visualization - Matplotlib, Seaborn, Recmetrics, Folium, Wordcloud.
5) Hyper Parameter Tuning - Pyspark Grid Search feature.
  
<a id='EDA'></a>
## Data Exploration
  
Let’s start with some basic yet useful data exploration and see what business value they can add. We will start of with,
1) The distribution of ratings in a particular city
2) The long tail plot
3) Most active users of the system
4) The restaurants with most customer traffic
5) The most valuable patrons of a particular restaurant
6) Categories of dishes to avoid in the city
  
**Distribution of Ratings in a particular city**

<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/Ratings%20distribution'.png" width = 700><p>
  
Ratings are a good calibration of the quality of a restaurant. The ratings distribution for each city can improve the confidence of people who are looking to move to the city and tourists as well. 
  
**Long Tail Plot**
  
<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/longtailplot.png" width = 700><p>
  
The long tail plot is often underestimated and can be very useful for recommender systems.
It indicates that most of the customer traffic is centralized to the most popular restaurants in the city. 

**Business value:**

While recommending we should be wary of the fact that users already know these restaurants and are expecting to try something new. Recommendations that avoid these restaurants can be more personalized and clever. 
It can also improve the business of “New to the Market” restaurants.
  
**Most Active Users of the System**
  
<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/top_10_reviewers_byreviews.png" width = 700><p>
  
**Business Value:**

Encouraging users who review and contribute to the system using special offers and freebies can really contribute to better performance of the recommendation engine. 
The user-business interaction matrix used in the recommendation algorithm is extremely sparse. In our case 99.4% sparse. Which means there are several million restaurants and several million orders happening everyday. But only a very small percentage of users rate their experience. So there is basically a lot of fill in the blanks. As reviews start pouring in, the model can learn better and achieve better performance and personalization.
  
**The Restaurants with the Most Customer Traffic**
  
<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/top10restaurantsbyrating.png" width = 700><p>
  
This is usually not very useful during modeling. But can be very useful during hypothesis and A/B testing.

**Most Valuable Patrons of a Particular Restaurant**
  
<p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/mvp.png" width = 700><p>
  
**Business Value:**
Insights like these can help  business owners reinvent the aspect of customer relationship.
  
<a id='features'></a>
## Features that constitute the solution
  
**Features for Patrons:**
1) Every user in the system will be provided with the recommendations from the hybrid engine.
2) The users will also be able to locate these recommendations on the map to filter further based on the location.
3) The users will also be provided with insights such as best rated restaurants, dishes to avoid etc.
4) A new user who has currently logged into the system will be provided the top 10 trending restaurants nearby based on their coordinates.

 **Features for the business owners:**
1) The business owners will also be provided with insights such as most valuable patrons, their current rating and reviews.
2) What is doing well and what people are not satisfied about, using the sentiment analysis technique.
  
<a id='algo'></a>

## Algorithms Used
%%%%%%%%%Under Construction%%%%%%%%%%
  
 <a id='results'></a> 
 ## Results

 **Set of 10 recommendations for the user_id "mNCd6ctHcY0ueistbprTwg" using the ALS model**
  
 <p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/recusingALS.png" width = 700><p>
   
 **The Table containing the predictions of ratings made for all users, business combination in the test set**
 
 <p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/table.png" width = 700><p>
     
 **Table containing the Top 10 Restaurant recommendations for the same User but using Cosine Similarity**
   
 <p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/cosinerec.png" width = 700><p>
   
 **Sentiment Analysis - Table showing trigrams of the text**
   
 <p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/trigrams.png" width = 700><p>
   
 **Sentiment Analysis - trigrams with svm coefficients (weights)**
   
 <p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/svmcoeff.png" width = 700><p>
   
 **Sentiment Analysis - Positive and Negative word clouds**
   
 <p align="center"><img src = "https://github.com/Rahul-Vasan/ML-driven-Personalized-Gourmet/blob/main/img/wordcloud.png" width = 700><p>  
   
   
   
   
   
   
  
  
  
  
  

  
  
  
  
  
  
  
  
  

  
  
  
 
