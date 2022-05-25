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
  
  

  
  
  
 
