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

python
recommend("Avatar")
recommend("Inception")
recommend("Titanic")

sample ouput
{
  "title": "Apollo 18",
  "similarity": 0.236,
  "reasons": ["Common words: ['space', 'mission', 'moon']"]
}
How to Run
Clone this repository:

git clone https://github.com/username/movie-recommendation.git
cd movie-recommendation
Open the Jupyter Notebook:

jupyter notebook movie_recommender.ipynb
Run each cell step-by-step:

Step 1: Import libraries

Step 2: Load datasets

Step 3: Merge and preprocess

Step 4: Create tags column

Step 5: TF-IDF vectorization

Step 6: Run recommendation function

Step 7: Test recommendations

Optionally, modify the recommend() function to show explainability.

🔍 Project Highlights
Uses both movies and credits datasets from Kaggle.

Combines multiple textual features for richer recommendations.

TF-IDF + Cosine Similarity ensures fast and accurate results.

Supports explainable recommendations for better understanding.

Fully reproducible with Kaggle datasets.

📈 Possible Extensions
Add a simple Streamlit or Flask interface for live recommendations.

Create a hybrid recommendation system by combining content-based with collaborative filtering.

Improve explainability by weighting different features (overview, cast, genres) differently.

Allow user ratings or feedback to refine recommendations.

📝 References
Kaggle TMDB 5000 Movies Dataset: https://www.kaggle.com/tmdb/tmdb-movie-metadata

Scikit-learn TF-IDF documentation: https://scikit-learn.org/stable/modules/feature_extraction.html#text-feature-extraction


---

If you want, I can also **write a short paragraph at the top that “sells” your project** for selection purposes, highlighting novelty and explainability to impress reviewers.  

Do you want me to do that?
