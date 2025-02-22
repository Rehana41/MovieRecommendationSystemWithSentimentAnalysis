# Movie Recommendation System with Sentiment Analysis

## 📌 Project Overview
This project is a **Content-Based Movie Recommendation System** that suggests movies based on user preferences and performs **Sentiment Analysis** on user reviews. Content Based Recommender System recommends movies similar to the movie user likes and analyses the sentiments on the reviews given by the user for that movie.

The details of the movies(title, genre, runtime, rating, poster, etc) are fetched using an API by TMDB, https://www.themoviedb.org/documentation/api, and using the IMDB id of the movie in the API, I did web scraping to get the reviews given by the user in the IMDB site using beautifulsoup4 and performed sentiment analysis on those reviews.

## 🔥 Features
- 🎬 **Movie Recommendations**: Recommends movies based on content similarity.
- 🤖 **Sentiment Analysis**: Analyzes user reviews using **Naive Bayes**.
- 📊 **Data Preprocessing**: Cleans and processes movie datasets.
- 🔍 **Search Functionality**: Allows users to find movies by name.
- 📜 **Cast & Details**: Fetches top cast and movie details from **TMDB API**.
- 🎭 **Genre-Based Filtering**: Users can explore movies based on genres.

## 🛠️ Technology Stack
- **Programming Language**: Python
- **Libraries & Frameworks**:
  - **Pandas, NumPy**: Data handling
  - **NLTK, Scikit-learn**: NLP & Machine Learning
  - **Flask**: Web-based UI
  - **Requests**: Fetching data from TMDB API
  - **Pickle**: Model persistence
  - **BeautifulSoup**: Web scraping 

## 📂 Dataset & Preprocessing
- The dataset includes movie metadata, descriptions, genres, and user reviews.
- **Preprocessing Steps**:
  1. **Cleaning Movie Data**: Handling missing values, text normalization.
  2. **TF-IDF Vectorization**: Converting text data into numerical form.
  3. **Sentiment Labeling**: Classifying reviews as positive or negative.
  4. **Feature Extraction**: Generating similarity scores for recommendations.

## 🚀 Model & Algorithm
### 🎥 Movie Recommendation
- **Count Vectorization**: Converts movie descriptions into feature vectors.
- **Cosine Similarity**: Measures the similarity between movies.
- **Content-Based Filtering**: Suggests movies similar to a given movie.

### 💬 Sentiment Analysis
- **Naive Bayes Classifier**: Used for analyzing user review sentiments.
- **Text Preprocessing**: Stopword removal, tokenization, and lemmatization.
- **Model Accuracy**: Achieved **97% accuracy** on the sentiment analysis task.

## 🎨 User Interface
The app is built using **Flask** with an interactive UI:
1. Upload a movie name to get recommendations.
2. View the **top cast & details** from TMDB API.
3. Analyze user **sentiments** from reviews.
4. Search for movies by title.

## How to get the API key?
Create an account in https://www.themoviedb.org/, click on the API link from the left hand sidebar in your account settings and fill all the details to apply for API key. If you are asked for the website URL, just give "NA" if you don't have one. You will see the API key in your API sidebar once your request is approved.

## 📦 Installation & Setup
1. Clone or download this repository to your local machine.
2. Install all the libraries mentioned in the requirements.txt file with the command pip install -r requirements.txt
3. Get your API key from https://www.themoviedb.org/. (Refer the above section on how to get the API key)
4. Replace YOUR_API_KEY in both the places (line no. 15 and 29) of static/recommend.js file and hit save.
5. Open your terminal/command prompt from your project directory and run the file main.py by executing the command python main.py.
6. Go to your browser and type http://127.0.0.1:5000/ in the address bar.
Hurray! That's it.

## Architecture
![Image](https://github.com/user-attachments/assets/9751c5b2-641e-44d6-9f95-cdff725f9e4b)

## Similarity Score
How does it decide which item is most similar to the item user likes? Here come the similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.

## How Cosine Similarity works?
Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.


![Image](https://github.com/user-attachments/assets/41c18c07-e4ba-4557-a44c-3c7a3ab5c7f0)


More about Cosine Similarity : [Understanding the Math behind Cosine Similarity](https://www.machinelearningplus.com/nlp/cosine-similarity/)

## Sources of the datasets
1. IMDB 5000 Movie Dataset(https://www.kaggle.com/carolzhangdc/imdb-5000-movie-dataset)
2. The Movies Dataset(https://www.kaggle.com/datasets/rounakbanik/the-movies-dataset)
3. List of movies in 2018(https://en.wikipedia.org/wiki/List_of_American_films_of_2018)
4. List of movies in 2019(https://en.wikipedia.org/wiki/List_of_American_films_of_2019)
5. List of movies in 2020(https://en.wikipedia.org/wiki/List_of_American_films_of_2020)








