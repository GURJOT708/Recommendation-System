# Movie Recommendation System

This project implements and compares two popular recommendation approaches using the MovieLens dataset (small version).

## 📋 Project Overview

Recommendation engines are critical for content-driven platforms. In this notebook, we explore two core modeling paradigms:
1. **K-Nearest Neighbors (KNN)**: An instance-based Collaborative Filtering approach that calculates similarities between movies directly based on user ratings.
2. **Matrix Factorization (SVD)**: A model-based Collaborative Filtering approach that decomposes the user-movie rating matrix into lower-dimensional latent factors representing hidden traits (e.g., quality, style, pacing).

---

## 📊 Models & Methodology

### 1. K-Nearest Neighbors (KNN)
* **Logic**: Measures direct overlap in rating behaviors. For a target movie, we retrieve its closest neighbors using **Cosine Similarity**.
* **Best for**: Intuitive, direct similarity recommendations (e.g., recommending sequels, spin-offs, or movies in the exact same franchise).

### 2. Matrix Factorization (Singular Value Decomposition - SVD)
* **Logic**: Compresses the sparse user-item matrix into dense $k$-dimensional vectors capturing abstract themes and user taste profiles.
* **Best for**: Discovered patterns, serendipitous discovery, and handling highly sparse data.

---

## 📈 Performance Comparison

We evaluated both models on a random sample of 500 records from the test split (80/20 train-test split):

| Metric | KNN Model (Item-based) | SVD (Matrix Factorization) |
| :--- | :---: | :---: |
| **MAE** (Mean Absolute Error) | 0.7558 | **0.7416** |
| **RMSE** (Root Mean Squared Error) | 0.9935 | **0.9369** |

### Key Findings
- **SVD achieves lower error values**: The SVD model outperforms KNN across both metrics, indicating that generalizing ratings through latent feature vectors provides cleaner predictions than direct local comparisons.
- **Recommendation Diversity**: SVD introduces broader discovery (recommending *WALL·E* or *Lost in Translation* alongside *The Dark Knight* based on abstract high-quality traits), while KNN focuses strictly on genre-adjacent titles (*Batman Begins*, *Iron Man*).
