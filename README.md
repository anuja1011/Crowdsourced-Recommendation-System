# Crowdsourced-Recommendation-System

****************************************************************************
I have been leaning on how to do Text Analytics and Natural Language Processing on wide platform of social media like Public Forums (Edmunds, Yelp etc.), Instagram, Twitter etc.

This is the first Project of the Series #User-Generated-Content-Analysis. Since this is a learning process, you will see a gradual improvement in the techniques used and also reduction in the number of assumption. 

As for this project: 

Things Learned:
* Lift Calculation
* Word-Frequency count
* Natural Language Processing
* Stemming & Lemitization
* Importance of word replacement
* Sentiment Analysis
* Cosine Similarity
****************************************************************************

# Project 3 of Series #User-Generated-Content-Analysis

The objective of this project is to create the building blocks of a crowdsourced recommendation system. This recommendation system should accept user inputs about desired attributes of a restaurant and come up with 3 recommendations. 

The flow of this project goes as follows:

* Extract 3k-4k reviews of restaurants from Yelp. This is done by - On Yelp.com, specify the location – e.g., Austin downtown, and type of food (e.g., Chinese or Mexican food). Scrape the text reviews and well as the ratings (the number of stars) provided by the users (there is no need to scrape pictures of food and other details). The data file should have 3 columns – the name of the restaurant, reviews, and ratings. 

* The assumption here is that a customer who will be using this recommendation system has specified 4 desirable attributes in a restaurant s/he is looking for – (i) service (e.g., speed, friendliness, etc.), (ii) food (e.g., quality, taste, etc.), (iii) price and (iv) location (e.g., parking, easy to find, drive through, etc.). 

* Pre-processing of data which includes removing of stop words, punctuations etc. Deleting redundant tweets i.r duplicate tweets followed by frequency count and word replacement. From a word frequency analysis of the reviews, do word replacements as deemed suitable – e.g., replace fast, friendly, etc. with service; variety, taste, choice, taco, etc. with food; etc.

* Also perform a cosine similarity analysis between the attribute set (service, food, price and location) and the reviews. It is like running a document query with words = service, food, price and location, and finding documents which are the best matches for the query words. Choose 200 reviews that have the highest cosine similarity scores. 

* Perform sentiment analysis on these 200 reviews and sort them (high to low) by the sentiment scores. Based on the above tasks, recommend 3 restaurants to the customer. It is possible that multiple reviews may refer to the same restaurant. Hence using the average sentiment score for each restaurant. 

* The idea is to find how would our recommendations differ if we ignored the cosine similarity and sentiment scores and simply recommended the 3 highest rated restaurants from your entire dataset? To do this, we need to calculate the average rating for each restaurant mentioned. Each restaurant in the data has many reviews, and we need to get the average rating for each restaurant; also not all reviews come with ratings. In calculating average ratings, we ignore reviews without ratings. The answers we are looking are would these three restaurants meet the requirements of the user looking for recommendations? Why or why not? 
