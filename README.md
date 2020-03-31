# Project 3 : SubReddit Classifier



## Problem statement

A Book publisher has come up with an new and interesting idea for cook book and is looking forward to publish it.With so much of materials (like cooking and baking recipes) available online, they want to check if people are still interested in  reading a cook book i.e., will it be profitable to publish a cookbook.

This Project compares top 1000 posts from two **subreddit** - Bookclub and Cooking from **Reddit** which is an American social news aggregation, web content rating, and discussion website.
**Bookclub** is a discussion forum about all things related to books, authors, genres and recommendation of books. 
**Cooking** , as the name suggests is a discussion forum related to recipes, preparation and various cuisines  and all things related to cooking.

In this Project, these two subreddits are explored to see if people in Bookclub and Cooking are discussing about cookbook, despite so many cooking/baking recipes available online.

## Executive Summary


### Contents

- [Data Collection and Cleaning](#Data-Collection-&-Cleaning)
- [Exploratory Data Analysis](#Exploratory-Data-Analysis)
- [Pre Processing](#Pre-Processing)
- [Modeling](#Modelling)
- [Inferential Visualizations](#Inferential-Visualizations)
- [Conclusions and Recommendation](#Conclusions-and-Recommendation)


### Data Collection & Cleaning


Data is extracted from reddit website by webscrapping (-a technique to automatically access and extract large amounts of information from a website ) the subreddit **Cooking** and **Bookclub** and cleaned. The link to those jupter notebooks is as follows:
<br><br>
[Click here to open notebook Cooking](project3_cooking.ipynb)<br>
[Click here to open notebook Bookclub](project3_book.ipynb)<br><br>

### Exploratory Data Analysis
This step involves the following:

>1. Import and Read data - Reading the csv file <br>
>2. Data Dictionary - is specified below <br>
>3. Data Visualization - Creating histogram and word cloud <br>
>4. Baseline Accuracy - Calculation <br>

Data Dictionary :

|Feature|Type|Description|
|---|---|---|
|subreddit|int64|specifies the type of subreddit|
|selftext|object|post of the subreddit| 
|length|int64|length of the post|



### Pre Processing
This step involves the following methods :

>1. Tokenizing - splitting data into distinct chunks<br>
>2. Removing Stopwords- Removing commonly used words/stop words as they take up space and processing time <br>
>3. Lemmatizing - return the base/dictionary form of a word<br>

### Modeling
 This step creates three models and compares them.

>1. Logistic Regression Model<br>
>2. Naive Bayes Model<br>
>3. Decision Tree Model<br>
>4. Comapring Models

Train and Test Scores:

|Model|Train Score|Test Score|
|---|---|---|
|Logistic Regression Model|0.9980769230769231|0.9942418426103646|
|Naive Bayes Model|0.9871794871794872|0.9846449136276392
|Decision Tree Model|0.9993589743589744|0.9328214971209213|

Confusion Matrix Result:

|Model|False Positives|False Negatives|
|---|---|---|
|Logistic Regression Model|0|3|
|Naive Bayes Model|8|0|
|Decision Tree Model|20|15|

### Inferential Visualizations

>1. Creating a desicion tree with Labels <br> 
>2. Creating word clouds for subreddit - Bookclub and Cooking<br>


## Conclusions and Recommendations

 By interpreting the nodes of Decision Tree structure, it is evident that approximately 330 posts in **Cooking** contains the word **"book"** and most of the post includes words related to books like chapter, read etc. 
On the other hand very minimal post in **Bookclub** have words related to cooking like recipe,meat,ingredient, oil etc. Based on this data it can be assumed that post in cooking forum might have referred to any recipe from a book and posts in Bookclub might be referring to any recipe in a cookbook but cannot be confirmed.
Since reddit is a popular forum, top 1000 posts from subreddit 'Cooking and 'Bookclub' were explored. This analysis can be extended to more posts in the same subreddit, other related subreddit and other popular online discussion forum to get a better insight about cookbook, which will help to conclude about profitability of publishing an cook book worldwide.
