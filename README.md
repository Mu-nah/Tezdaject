# Movie Data Analysis & Recommendation

# Project Overview
This project involves analyzing a dataset of ~4,800 movies and building a recommendation system based on content similarity. The tasks include:
Exploratory Data Analysis (EDA)
Data Cleaning & Feature Engineering
Building a Movie Recommendation System
Creating Visualizations in Power BI
Documentation and Summary

# Dataset Description
The dataset contains the following key columns:
budget, revenue, popularity, vote_average, runtime (Numeric features)
genres, keywords, cast, crew, production_companies (Textual features, some in JSON-like format)
title, original_language, release_date, overview (General movie information)

# Steps Taken
1. Exploratory Data Analysis (EDA)
Loaded the dataset and checked for missing values and duplicates.
Analyzed descriptive statistics: average budget, revenue, distribution of ratings.
Identified the top 10 highest-grossing and highest-budget movies.
Explored correlations between numeric columns (e.g., budget vs. revenue).
Analyzed the most common genres and languages in the dataset.
Created visualizations such as a bar chart of top genres and a scatter plot of budget vs. revenue.

2. Data Cleaning & Feature Engineering
Handled missing values by dropping rows with critical missing data.
Extracted meaningful values from JSON-like columns (genres, keywords, cast, crew).
Converted crew column from a string representation to extract the director’s name.
Created a combined_features column by merging title, genres, keywords, and cast for recommendation purposes.
Normalized numeric columns like budget and popularity for better comparison.

3. Recommendation System
Implemented a content-based filtering approach:
Used TF-IDF vectorization on overview, genres, and keywords.
Calculated cosine similarity between movies.
Built a recommend_movies(movie_title) function to find the most similar movies based on content.

Alternative: Used popularity-based filtering to recommend top-rated movies within the same genre.

4. Visualizations
Top 10 movies by revenue and rating.
Genre distribution visualization.
Budget vs. revenue comparison.


Exported the cleaned dataset for Power BI visualization.


# Prerequisites
Python 3.8+

# How to Run the Code
Install required libraries:
pip install pandas numpy scikit-learn matplotlib seaborn ast
Running the Jupyter Notebook
Open the Jupyter Notebook (main.ipynb).
Run all cells to clean data, perform EDA, and generate recommendations.
Use recommend_movies("Movie Title") to get recommendations.

# Power BI Dashboard
Open the Power BI file (TezdaViz.pbix).
Explore the dashboards with filters and insights.
