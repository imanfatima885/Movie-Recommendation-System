#  Movie Recommendation System

A content-based movie recommendation system built with Python and Streamlit that suggests similar movies using cosine similarity on the TMDB 5000 dataset.

---

##  Overview

This project recommends movies based on content similarity. Given a movie title, it finds the top 10 most similar movies using cosine similarity computed on movie metadata. Movie posters are fetched live from the TMDB API.

---

##  Features

-  Search from thousands of movies
-  Content-based filtering using cosine similarity
-  Displays movie posters in a clean 2×5 grid layout
-  Built with Streamlit for a fast, interactive UI

---

##  Tech Stack

| Layer | Technology |
|---|---|
| Language | Python |
| UI Framework | Streamlit |
| Data Processing | Pandas |
| ML / Similarity | Scikit-learn (cosine similarity) |
| Movie Data | TMDB 5000 Movie Dataset |
| Poster Fetching | TMDB API |

---

##  Project Structure

```
movie-recommendation-system/
│
├── app.py                  # Streamlit app
├── main.ipynb              # Data preprocessing notebook
├── movie_data.pkl          # Preprocessed movies + similarity matrix
├── requirements.txt        # Python dependencies
└── README.md
```

---

##  Setup & Installation

### 1. Clone the repository

```bash
git clone https://github.com/imanfatima885/Movie-Recommendation-System.git
cd movie-recommendation-system
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Get your TMDB API Key

- Sign up at [https://www.themoviedb.org/](https://www.themoviedb.org/)
- Go to **Settings → API** and copy your API key
- Replace the `api_key` value in `app.py`:

```python
api_key = 'YOUR_TMDB_API_KEY'
```

### 4. Prepare the data

Run the `main.ipynb` notebook to preprocess the TMDB 5000 dataset and generate `movie_data.pkl`.

> Dataset: [TMDB 5000 Movie Dataset on Kaggle](https://www.kaggle.com/datasets/tmdb/tmdb-movie-metadata)

### 5. Run the app

```bash
streamlit run app.py
```

---

##  How It Works

1. The TMDB 5000 dataset is preprocessed in the notebook (tags, genres, cast, etc.)
2. A TF-IDF or count vectorizer builds feature vectors for each movie
3. Cosine similarity is computed between all movies and saved to `movie_data.pkl`
4. When you select a movie, the app finds the top 10 most similar movies by cosine score
5. Posters are fetched in real-time from the TMDB API

---

##  Screenshot

<img width="1919" height="954" alt="image" src="https://github.com/user-attachments/assets/15ef5a94-5a6d-46ae-86f7-f1b6a84f76bc" />



---

