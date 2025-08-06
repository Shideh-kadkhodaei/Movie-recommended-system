# 🎬 Drama Movie Recommender System

This project is a simple content-based movie recommender system that focuses on recommending similar *Drama* movies based on genre and IMDB rating. It uses cosine similarity to find movies most similar to a given input movie.

## 📌 Features

- Filters only *Drama* genre movies.
- Uses genre tags and IMDB rating for similarity.
- Visualizes top similar movies using horizontal bar plots.
- Reads data from an Excel file with 1000 movie entries.

## 🧠 How It Works

1. The dataset is loaded from an Excel file Data.xlsx.
2. Only movies that include the genre "Drama" are selected.
3. Genres are one-hot encoded, and IMDB ratings are standardized.
4. Cosine similarity is calculated between all drama movies.
5. Given a movie title, it returns the top N similar movies based on features.

## 🛠️ Technologies Used

- Python 3
- Pandas
- NumPy
- scikit-learn
- Matplotlib

## 📂 Dataset

Make sure you have a file named Data.xlsx in the root of the project. It should contain at least the following columns:

- Series_Title  
- Genre (comma-separated string, e.g., "Drama, Crime")
- IMDB_Rating  
- Released_Year  
- Gross *(optional, not used in this version)*

## ▶️ How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/drama-movie-recommender.git
   cd drama-movie-recommender

2. Install dependencies (preferably in a virtual environment):

pip install -r requirements.txt


3. Make sure Data.xlsx is placed in the same directory as your script.


4. Run the script:

python your_script_name.py


5. Try some examples:

recommend_movies("The Shawshank Redemption")
recommend_movies("The Godfather")



📊 Example Output

Recommendations similar to 'The Godfather':
----------------------------------------
1. Goodfellas (1990)
   Genre: Crime, Drama
   IMDB Rating: 8.7
   Similarity: 0.94
----------------------------------------
...

📈 Visualization

A horizontal bar chart will be displayed showing the similarity scores and release years of the recommended movies.
