# Yelp-Analysis-and-Recommender

### Overview
For part of my coursework during my time in General Assembly’s Data Science Immersive program, I was tasked to design and develop a recommender system. First, I conducted a thorough analysis of the data, a sentiment analysis on a popular restaurant in the city of Pittsburg, then created a text classification model that is able to predict the rating a customer would give a restaurant they tried based on the language (NLP) that they used in the rating. The choice to create a restaurant recommender inspired by my love to try new things (food) and to explore my curiosity about a company whose product/service I use regularly (Yelp).

### Data
The Yelp dataset is a subset of our businesses, reviews, and user data for use in personal, educational, and academic purposes. Available as JSON files, use it to teach students about databases, to learn NLP, or for sample production data while you learn how to make mobile apps. In this dataset, there are:
- 5,200,000 user reviews
- Information on 174,000 businesses
- The data spans 11 metropolitan areas

The dataset is extremely large, I have included a link for access.
https://www.yelp.com/dataset/challenge

### Process
The dataset was converted from JSON to CSV -  The yelp data comes in JSON (JavaScript Object Notation) and to make it easier and more flexible, I converted the data into a Pandas Dataframe. Both ‘Review’ and ‘Business’ files were merged to create one file and saved to a CSV for further analysis.

#### Exploratory Data Analysis 
A second Jupyter Notebook was created to read the CSV back in and perform EDA (Exploratory Data Analysis). A second notebook was created so that the previous code was not disturbed. 
 
#### Sentiment Analysis 
After performing EDA and identifying the most popular restaurant in the Pittsburg area. Sentiment analysis was used, specifically, emotion detection which aims to t detect emotions, like happiness, frustration, anger, sadness, and so on. This analysis is a quick way for restaurants (or other businesses) to identify customer sentiment toward their products, brands or services in online conversations and feedback.

#### Feature Engineering for Classification Model 
The raw dataset (for Pittsburg only) was transformed into flat features that are able to be used in a machine learning model. This step also includes the process of creating new features from the existing data. I converted all rated reviews (reviews that included ratings on a scale from 1-5) to a 1-3 bucket. See below

1 or 2 rating - (1 or poor)
3 or 4 rating - (2 or average)
5 rating - (3 or exceptional)

#### Recommender
I used item-based collaborative filtering to create a recommender In this approach, similarities between pair of items are computed using a cosine similarity metric. Once the recommender was created, you are able to enter a restaurant and the function will recommend a similar restaurant.
