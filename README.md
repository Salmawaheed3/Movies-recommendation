# Movie Recommendation System

This repository contains a Movie Recommendation System that is built using machine learning techniques. It leverages both **content-based filtering** and **collaborative filtering** (using the `Surprise` library) to provide personalized movie recommendations.

## Project Overview

The recommendation system is designed to:
- Analyze and clean movie datasets.
- Perform **Exploratory Data Analysis (EDA)** to understand the data distribution and relationships.
- Build a **content-based recommendation system** that suggests movies similar to a given movie based on features like genres, cast, and language.
- Implement a **collaborative filtering system** using **Singular Value Decomposition (SVD)** to recommend movies to users based on their historical preferences and ratings.

## Datasets

The project uses the following datasets:
- **tmdb_5000_movies.csv**: Contains metadata about 5000 movies including title, genres, cast, crew, and keywords.
- **tmdb_5000_credits.csv**: Contains additional metadata such as the full cast and crew for the movies.

These datasets have been preprocessed and combined for effective recommendation modeling.

## Features

The project is divided into two recommendation approaches:

### 1. Content-Based Filtering
This method recommends movies based on their similarity to a given movie. It uses features such as:
- **Genres**
- **Cast**
- **Language**

These features are combined into a new column called `combined_features`, and the similarity between movies is calculated using **cosine similarity** after vectorizing the text features.

### 2. Collaborative Filtering with SVD
This method recommends movies based on user preferences. It utilizes the **Singular Value Decomposition (SVD)** algorithm from the `Surprise` library to make predictions about how a user might rate a movie they haven't watched yet.

### Model Evaluation
The collaborative filtering model is evaluated using cross-validation with the following metrics:
- **RMSE** (Root Mean Squared Error)
- **MAE** (Mean Absolute Error)

## Requirements

To run this project, you will need the following Python libraries:

```bash
pandas
numpy
scikit-learn
scikit-surprise
