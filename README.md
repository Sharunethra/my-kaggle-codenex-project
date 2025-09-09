# my-kaggle-codenex-project
A content-based movie recommendation system using the TMDB 5000 dataset. It combines movie overview, genres, keywords, top cast, and director, applies TF-IDF vectorization and cosine similarity, and recommends similar movies with optional explainability.
# Content-Based Movie Recommendation System

This project is a **content-based movie recommendation system** built using the TMDB 5000 Movies dataset. It recommends movies similar to a given movie based on text features such as overview, genres, keywords, cast, and director.

---

## 📂 Project Structure


---

## 🛠 Technologies Used

- **Python 3**
- **Pandas** – Data loading and manipulation
- **NumPy** – Numerical operations
- **Scikit-learn** – TF-IDF vectorization and cosine similarity
- **Ast** – Parsing JSON-like text fields in datasets

---

## ⚙️ How It Works

1. **Data Loading**  
   Load `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv` from Kaggle dataset.

2. **Data Preprocessing**  
   - Merge movies and credits on the `title` column.  
   - Extract useful features: genres, keywords, top 3 cast members, and director.  
   - Combine all features into a single `tags` column (text).

3. **Vectorization**  
   - Apply **TF-IDF vectorization** on the `tags` column.  
   - Convert text into numerical vectors for similarity computation.

4. **Recommendation Function**  
   - Given a movie title, compute cosine similarity between its vector and all other movies.  
   - Return **top N similar movies** with similarity scores.  
   - **Explainability:** Optionally, show the reason for recommendation (common words in tags).

5. **On-Demand Recommendations**  
   Users can query the system for any movie in the dataset:

```python
recommend("Avatar")
recommend("Inception")
recommend("Titanic")
