# Movie Recommendation System

This project is a Movie Recommendation System that suggests movies similar to the user's favorite movie based on features such as genres, keywords, tagline, cast, and director. The model uses TF-IDF (Term Frequency-Inverse Document Frequency) for text vectorization and cosine similarity to measure the similarity between movies.

# Table of Contents

1.Dataset

2.Dependencies

3.Project Structure

4.Data Preprocessing

5.Recommendation Process

6.Usage

# Dataset

The dataset used in this project is a CSV file that contains information about movies, including:

index: Unique index for each movie.

title: The title of the movie.

genres: The genres of the movie.

keywords: Keywords associated with the movie.

tagline: The tagline of the movie.

cast: The main cast of the movie.

director: The director of the movie.

# Dependencies

To run the project, you need the following libraries:

Python 3.x

NumPy

Pandas

scikit-learn

You can install the required libraries using the following command:

pip install numpy pandas scikit-learn

# Project Structure

movies.csv: The dataset file containing the movie information.

movie_recommendation_system.py: The main Python script for data preprocessing, building the recommendation system, and generating movie recommendations.

# Data Preprocessing

Handling Missing Values: Any missing values in the selected features (genres, keywords, tagline, cast, director) are replaced with an empty string.

Combining Features: The selected features are combined into a single string for each movie, which will be used for text vectorization.

TF-IDF Vectorization: The combined features are converted into numerical vectors using TF-IDF Vectorizer.

Cosine Similarity: Cosine similarity is calculated between all movie vectors to measure how similar they are to each other.

# Recommendation Process

Input: The user provides the name of their favorite movie.

Finding a Close Match: The system finds the closest match to the input movie name in the dataset using difflib.

Similarity Calculation: The similarity score between the selected movie and all other movies in the dataset is calculated.

Sorting and Displaying Recommendations: Movies are sorted based on their similarity score in descending order, and the top 30 similar movies are displayed to the user.

# Usage

Run the movie_recommendation_system.py script.

Enter the name of your favorite movie when prompted.

The system will suggest a list of similar movies based on the input.

Example output:

Enter your favourite movie name : Inception

Movies suggested for you :
1. Inception
2. The Dark Knight
3. Interstellar
  ...
