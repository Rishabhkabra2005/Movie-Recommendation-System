# Project: Movie Recommender System Using Machine Learning!

<img src="demo/6.jpeg" alt="workflow" width="70%">

Recommendation systems are becoming increasingly important in today’s extremely busy world. People are always short on time with the myriad tasks they need to accomplish in the limited 24 hours. Therefore, the recommendation systems are important as they help them make the right choices, without having to expend their cognitive resources.

The purpose of a recommendation system basically is to search for content that would be interesting to an individual. Moreover, it involves a number of factors to create personalised lists of useful and interesting content specific to each user/individual. Recommendation systems are Artificial Intelligence based algorithms that skim through all possible options and create a customized list of items that are interesting and relevant to an individual. These results are based on their profile, search/browsing history, what other people with similar traits/demographics are watching, and how likely are you to watch those movies. This is achieved through predictive modeling and heuristics with the data available.

# Types of Recommendation System :

### 1 ) Content Based :

- Content-based systems, which use characteristic information and takes item attriubutes into consideration .

- Twitter , Youtube .

- Which music you are listening , what singer are you watching . Form embeddings for the features .
	
- User specific actions or similar items reccomendation .
	
- It will create a vector of it .
	
- These systems make recommendations using a user's item and profile features. They hypothesize that if a user was interested in an item in the past, they will once again be interested in it in the future
	
- One issue that arises is making obvious recommendations because of excessive specialization (user A is only interested in categories B, C, and D, and the system is not able to recommend items outside those categories, even though they could be interesting to them).

### 2 ) Collaborative Based :
		
- Collaborative filtering systems, which are based on user-item interactions.
	
- Clusters of users with same ratings , similar users .
	
- Book recommendation , so use cluster mechanism .
	
- We take only one parameter , ratings or comments .
	
- In short, collaborative filtering systems are based on the assumption that if a user likes item A and another user likes the same item A as well as another item, item B, the first user could also be interested in the second item . 
	
- Issues are :

	- User-Item nXn matrix , so computationally expensive .

	- Only famous items will get reccomended .

	- New items might not get reccomended at all .   

### 3 ) Hybrid Based :
	
- Hybrid systems, which combine both types of information with the aim of avoiding problems that are generated when working with just one kind.

- Combination of both and used now a days .

- Uses : word2vec , embedding .           

# About this project:
This project is a content-based movie recommendation system inspired by the "Netflix Movie Recommender System Using Machine Learning" YouTube tutorial. It suggests similar movies based on user input by analyzing movie tags and genres. The system leverages cosine similarity to recommend the top five most similar movies and integrates movie posters using the TMDb API. A simple web interface is built using Streamlit for easy user interaction
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


# Demo:

<img src="demo/1.png" alt="workflow" width="70%">

<img src="demo/2.png" alt="workflow" width="70%">

<img src="demo/3.png" alt="workflow" width="70%">


# Dataset has been used:

* [Dataset link](https://www.kaggle.com/tmdb/tmdb-movie-metadata?select=tmdb_5000_movies.csv)

# Concept used to build the model.pkl file : cosine_similarity

1 . Cosine Similarity is a metric that allows you to measure the similarity of the documents.

2 . In order to demonstrate cosine similarity function we need vectors. Here vectors are numpy array.

3 . Finally, Once we have vectors, We can call cosine_similarity() by passing both vectors. It will calculate the cosine similarity between these two.

4 . It will be a value between [0,1]. If it is 0 then both vectors are complete different. But in the place of that if it is 1, It will be completely similar.

5 . For more details , check URL : https://www.learndatasci.com/glossary/cosine-similarity/

**📌 Known Issues**
1. The movie recommendation button initially faced issues with functionality but was corrected by linking the appropriate functions properly.

2. Minor syntax errors were encountered during development and resolved in later iterations.

**💡 Future Improvements**
1. Enhance UI for mobile responsiveness.

2. Add collaborative filtering to recommend movies based on user ratings.

3. Implement additional search filters (like year, rating, etc.).

4. Improve error handling and loading speed for larger datasets.
