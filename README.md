**🎬 Netflix Movie Recommendation System Using Machine Learning**
This project is a content-based movie recommendation system inspired by the "Netflix Movie Recommender System Using Machine Learning" YouTube tutorial. It suggests similar movies based on user input by analyzing movie tags and genres. The system leverages cosine similarity to recommend the top five most similar movies and integrates movie posters using the TMDb API. A simple web interface is built using Streamlit for easy user interaction.


**🔑 Key Features**
1. Content-Based Filtering:
Recommends movies based on their genres, tags, and overviews.

2. Cosine Similarity Calculation:
Calculates movie similarity scores using cosine distance to find the closest matches.

3. Movie Poster Integration:
Uses the TMDb API to fetch and display movie posters alongside recommendations.

4. Web Interface:
Built a user-friendly interface using Streamlit with a dropdown to select movies and view results instantly.

**🛠️ Technologies Used**
1. Programming Language: Python

2. Libraries: Pandas, NumPy, Scikit-learn, Requests, Pickle

3. Data Source: TMDb 5000 Movies Dataset (Kaggle)

4. Web Interface: Streamlit

5. API: TMDb API (for fetching movie posters)

**⚙️ Installation & Setup**

1. **Clone the Repository:**

git clone https://github.com/yourusername/movie-recommendation-system.git

cd movie-recommendation-system

2. **Create a Virtual Environment:**

python -m venv venv
source venv/bin/activate  # Linux/Mac
venv\Scripts\activate     # Windows

3. **Install the Required Libraries:**

pip install -r requirements.txt

4. **Run the Project:**

streamlit run main.py

**🚀 How It Works**
1. Load the TMDb 5000 Movies dataset using Pandas.

2. Preprocess the dataset by combining relevant text features (genres, keywords, overviews).

3. Vectorize the text using CountVectorizer from Scikit-learn.

4. Calculate cosine similarity to find similar movies.

5. Save processed data using Pickle for faster loading.

6. Build a Streamlit web application with a movie selection dropdown and recommend button.

7. Fetch movie posters from the TMDb API to enhance the user experience.

**✅ Functionalities**
1. Select a movie title from the dropdown menu.

2. Instantly receive top five similar movie recommendations.

3. View movie posters alongside recommendations.

4. Quick results using pre-computed similarity matrices.

**📌 Known Issues**
1. The movie recommendation button initially faced issues with functionality but was corrected by linking the appropriate functions properly.

2. Minor syntax errors were encountered during development and resolved in later iterations.

**💡 Future Improvements**
1. Enhance UI for mobile responsiveness.

2. Add collaborative filtering to recommend movies based on user ratings.

3. Implement additional search filters (like year, rating, etc.).

4. Improve error handling and loading speed for larger datasets.
