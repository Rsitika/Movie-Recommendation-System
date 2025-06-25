# 🎬 Movie Recommendation System

This project is a **Content-Based Movie Recommender System** that suggests movies based on similarity of genres, cast, keywords, and description. It uses **Natural Language Processing (NLP)** and **Cosine Similarity** to find the most similar movies.

---

## 📂 Dataset

The dataset used is the [TMDB 5000 Movie Dataset](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata), which includes:
- Movie overviews
- Genre tags
- Cast and crew info
- Keywords

---

## 🧠 Features Used for Recommendation

- **Overview** (description of the movie)
- **Genres**
- **Keywords**
- **Top 3 Cast Members**
- **Director**

These features are combined into a single text-based field (`tags`) and then vectorized for similarity comparison.

---

## 🧪 Tech Stack & Libraries

- Python 🐍
- Pandas
- Scikit-learn
- CountVectorizer
- Cosine Similarity

---

## 💡 How It Works

1. Preprocessing:
   - Extract relevant info from `genres`, `keywords`, `cast`, and `crew`.
   - Merge them into a new feature column `tags`.

2. Vectorization:
   - Apply `CountVectorizer` with max 5000 features and English stopwords removed.

3. Similarity Calculation:
   - Use `cosine_similarity` to compare every movie with others.

4. Recommendation:
   - Enter a movie name → it returns top 5 most similar movies.

---

## 🚀 How to Use

1. Clone this repo or open in Google Colab.
2. Upload the two CSV files:
   - `tmdb_5000_movies.csv`
   - `tmdb_5000_credits.csv`
3. Run all notebook cells.
4. Use the function:
   ```python
   recommend("Avatar")
