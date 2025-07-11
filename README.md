# 🎬 Movie Recommender System Using Machine Learning!

<img src="demo/Screenshot%202025-07-11%20183836.png" alt="Recommendation Systems Concept" width="80%"/>

Recommendation systems are becoming increasingly important in today’s fast-paced world. People are often short on time, and recommender systems help them make better choices quickly, without expending much cognitive effort.

These systems use AI-based algorithms to suggest relevant content based on user profiles, history, and behavior—leveraging predictive modeling and heuristics to generate personalized lists.

---

## 📌 Types of Recommendation Systems

### 1️⃣ Content-Based Filtering:
- Uses item features (e.g., genres, tags) to recommend similar items.
- Personalized: Suggestions based on a user’s past preferences.
- Example platforms: **YouTube**, **Twitter**.
- Pros: Tailored to user.
- Cons: May lead to over-specialization (recommend only similar items).

### 2️⃣ Collaborative Filtering:
- Based on user-item interactions.
- Relies on user clusters with similar preferences.
- Example: Book/music/movie recommendations using user ratings/comments.
- Pros: Doesn’t need item metadata.
- Cons:
  - Cold-start problem (new items/users not recommended).
  - Scalability issues due to sparse user-item matrices.

### 3️⃣ Hybrid Filtering:
- Combines content-based and collaborative approaches.
- Example: **Netflix**.
- Uses advanced models like **Word2Vec**, embeddings.
- Pros: Mitigates limitations of individual systems.

---

## 🧠 About This Project

This is a **content-based movie recommendation system** inspired by the Netflix-style approach. It analyzes tags and genres to suggest movies similar to a selected title using **cosine similarity**. It also displays movie posters using the **TMDb API**, and offers an interactive web app built with **Streamlit**.

---

## 🔑 Key Features

- 🎯 **Content-Based Filtering**: Uses genres, keywords, and overviews.
- 🧮 **Cosine Similarity**: Computes similarity scores between movies.
- 🖼️ **Movie Posters**: Fetched using **TMDb API**.
- 🌐 **Web Interface**: Built with **Streamlit** for easy interaction.

---

## 🛠️ Technologies Used

- **Language**: Python  
- **Libraries**: Pandas, NumPy, Scikit-learn, Requests, Pickle  
- **Dataset**: [TMDb 5000 Movies Dataset (Kaggle)](https://www.kaggle.com/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv)  
- **Web Framework**: Streamlit  
- **API**: [TMDb API](https://www.themoviedb.org/documentation/api)

---
## ⚙️ Installation & Setup

### 🧪 Create a Virtual Environment

```bash
python -m venv venv
# Activate:
source venv/bin/activate       # On Linux/Mac
venv\Scripts\activate          # On Windows
```

### 📦 Install Dependencies

```bash
pip install -r requirements.txt
```

### ▶️ Run the Application

```bash
streamlit run main.py
```

---

## 🚀 How It Works

1. Load the **TMDb 5000 Movies** dataset using **Pandas**.  
2. Preprocess by combining **genres**, **tags**, and **descriptions**.  
3. Convert text into numerical vectors using `CountVectorizer`.  
4. Compute pairwise **cosine similarity** between movies.  
5. Save/load preprocessed data using **Pickle** for faster startup.  
6. Build the UI with **Streamlit** (dropdown to select a movie).  
7. Display **top 5 similar movies** with poster previews using **TMDb API**.

---

## ✅ Functionalities

- 🎬 Select a movie from the dropdown.
- 🧠 Instantly receive top 5 similar movie suggestions.
- 🖼️ View movie posters next to recommendations.
- ⚡ Fast performance via precomputed similarity matrix.

---

## 📊 Dataset Used

- **Source**: [Kaggle - TMDb Movie Metadata](https://www.kaggle.com/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv)

---

## 📚 Cosine Similarity (Used in `model.pkl`)

- Measures how similar two vectors are based on their angle.
- Output ranges from `0` (completely different) to `1` (identical).
- Applied to vectorized movie tags and genres to find similar items.

🔗 [Learn More](https://www.learndatasci.com/glossary/cosine-similarity/)

---

## 📷 Demo

<img src="demo/Screenshot%202025-07-11%20183726.png" alt="Spider-Man 3 demo" width="80%"/>
<img src="demo/Screenshot%202025-07-11%20183755.png" alt="Avatar demo" width="80%"/>
<img src="demo/Screenshot%202025-07-11%20183820.png" alt="Avengers demo" width="80%"/>
---

## 🐞 Known Issues

- Initial bug in the movie recommendation button (✅ fixed).
- Minor syntax errors during early development (✅ resolved).

---

## 💡 Future Improvements

- 📱 Improve UI responsiveness for mobile/tablet users.
- 🔄 Add collaborative filtering based on user ratings.
- 🎚️ Add filtering options (e.g., year, genre, rating).
- ⚡ Optimize performance for large datasets.
- 🛡️ Add better error handling and fallback logic for API issues.
