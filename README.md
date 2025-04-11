# 🎬 Movie Recommendation System

[![Recommendation Systems](https://img.shields.io/badge/Type-Recommendation_Systems-blue)](https://en.wikipedia.org/wiki/Recommender_system)
[![Python](https://img.shields.io/badge/Language-Python-green)](https://www.python.org/)
[![Machine Learning](https://img.shields.io/badge/Focus-Machine_Learning-orange)](https://en.wikipedia.org/wiki/Machine_learning)

A comprehensive movie recommendation system implementing four distinct recommendation approaches with detailed visual analytics.

## 📌 Table of Contents

- [Project Overview](#-project-overview)
- [Approaches](#-approaches)
  - [Popularity-Based Filtering](#1-popularity-based-filtering)
  - [Content-Based Filtering](#2-content-based-filtering)
  - [Collaborative Filtering (SVD)](#3-collaborative-filtering-svd)
  - [Neural Collaborative Filtering](#4-neural-collaborative-filtering)
- [Comparative Analysis](#-comparative-analysis)
- [Best Recommendation System](#-best-recommendation-system)
- [Installation](#-installation)
- [Dataset](#-dataset)
- [Future Work](#-future-work)
- [License](#-license)

## 🎥 Project Overview

This system provides movie recommendations using four different algorithmic approaches, each with specialized visualizations to demonstrate their characteristics and performance.

![System Architecture](https://via.placeholder.com/800x400?text=System+Architecture+Diagram)

## 🔍 Approaches

### 1. Popularity-Based Filtering

**Concept**: Recommends generally popular movies based on aggregate ratings.

**Key Visualizations**:

```python
import matplotlib.pyplot as plt
import seaborn as sns

plt.figure(figsize=(12, 8))
sns.barplot(x='weighted_rating', y='title', data=top_movies)
plt.title('Top 10 Movies by Weighted Rating')
plt.show()

Insight: The weighted rating formula balances between rating quality (R) and vote count (v).

$$WR = \frac{v}{v+m} \times R + \frac{m}{v+m} \times C$$

### 2. Content-Based Filtering
**Concept**: Recommends similar movies based on content features.

**Key Visualizations**:

```Python

import matplotlib.pyplot as plt

plt.barh(top_words, top_scores)
plt.title(f'Top {n_words} Important Words in "{movie_title}"')
plt.show()
Insight: Uses TF-IDF vectorization of movie overviews to calculate content similarity.

### 3. Collaborative Filtering (SVD)
**Concept**: Finds patterns in user-movie ratings using matrix factorization.

**Key Visualizations**:

```Python

import matplotlib.pyplot as plt

plt.subplot(1, 2, 1)
plt.plot(history.history['loss'])
plt.title('Model Loss')
plt.show()
Performance:

Average RMSE: 0.85
Average MAE: 0.65
4. Neural Collaborative Filtering
Concept: Deep learning model for complex user-item interactions.

### Model Architecture:

Embedding Layers → Concatenation → Dense Layers (128, 64, 32) → Output
📊 Comparative Analysis
Approach	Personalization	Cold Start	Complexity	Best For
Popularity-Based	None	Excellent	Low	New users
Content-Based	Medium	Good	Medium	Similar item discovery
Collaborative (SVD)	High	Poor	Medium	Existing users
Neural CF	Very High	Poor	High	Large-scale systems

Export to Google Sheets
🏆 Best Recommendation System
Optimal Choices:

General Purpose: Collaborative Filtering (SVD)
Cold Start: Content-Based
Maximum Performance: Neural CF
Simple Baseline: Popularity-Based
💻 Installation
Bash

git clone [[https://github.com/yourusername/movie-recommendation-system.git](https://github.com/yourusername/movie-recommendation-system.git)
cd movie-recommendation-system](https://github.com/mihirpatil37/app_17_movie_recommendation_system.git)
pip install -r requirements.txt
Requirements:

Python 3.7+
pandas, numpy, matplotlib, seaborn
scikit-learn, surprise
TensorFlow ≥ 2.0
📂 Dataset
Required files:

movies.csv
ratings.csv
credits.csv
Dataset structure:

├── data/
│   ├── movies.csv
│   ├── ratings.csv
│   └── credits.csv
🚀 Future Work
Hybrid recommendation system
Real-time API endpoint
Streamlit web interface
Docker deployment
📜 License
MIT License - See LICENSE for details.
