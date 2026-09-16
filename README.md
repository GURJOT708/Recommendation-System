# Movie Recommendation System

This repository contains a Movie Recommendation System built using Python, Pandas, Seaborn, Scipy, and Scikit-Learn. The system utilizes the **MovieLens (small) Dataset** to analyze user preferences and generate personalized movie suggestions using Collaborative Filtering.

## 🚀 Project Overview

- **Exploratory Data Analysis (EDA):** Identifies top-rated movies and visualizes the overall distribution of movie ratings.
- **Collaborative Filtering:** Implements an item-based K-Nearest Neighbors (KNN) model using **Cosine Similarity** to recommend movies based on user rating patterns.
- **Visualizations:** Visualizes movie similarity distances to show how closely recommended movies align with the query title.

## 🛠️ Tech Stack & Libraries

- **Python 3**
- **Pandas** (Data loading and manipulation)
- **Matplotlib & Seaborn** (Data visualization)
- **Scipy** (Sparse matrix representation for memory efficiency)
- **Scikit-Learn** (Nearest Neighbors model building)

## 📁 Dataset

This project uses the `ml-latest-small` dataset from MovieLens, which contains:
- `movies.csv`: Movie IDs, titles, and genres.
- `ratings.csv`: User ratings (0.5 to 5.0) and timestamps.

## 💻 How to Use the Recommender

Once the cells are executed, you can search for a movie and find similar items using:

```python
get_recommendations('Fight Club')
To view a visual plot of recommendations and their matching cosine distances:

plot_recommendation_distances('Fight Club')
📊 Sample Outputs
For 'Toy Story (1995)', the top recommendations include:

Toy Story 2 (1999)
Jurassic Park (1993)
Independence Day (1996)
Star Wars: Episode IV - A New Hope (1977)
Forrest Gump (1994)
