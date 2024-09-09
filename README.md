# Movie Recommendation System

## Objective
The objective of this project is to build a movie recommendation system that suggests movies to users based on their preferences, using collaborative filtering, content-based filtering, or a hybrid approach.

## Data Source
The dataset used in this project comes from the [MovieLens dataset](https://grouplens.org/datasets/movielens/), which contains information about users, movies, ratings, and genres.

## Import Library
The following Python libraries are used in the project:
- **Pandas**: For data manipulation and analysis.
- **NumPy**: For numerical computations.
- **Scikit-learn**: For model building and evaluation.
- **Surprise**: A library specifically designed for building recommendation systems.
- **Matplotlib**/**Seaborn**: For data visualization.

## Import Data
The dataset is imported as CSV files, including:
- `movies.csv`: Contains movie titles and genres.
- `ratings.csv`: Contains user ratings for different movies.
- `users.csv`: Contains user demographic information (if used).

## Describe Data
- **movies.csv**: Contains movieId, title, and genres.
- **ratings.csv**: Contains userId, movieId, rating, and timestamp.
- **users.csv** (if applicable): Contains userId, age, gender, occupation, and zipcode.
- Descriptive statistics and missing data analysis are performed, including:
  - Distribution of ratings.
  - Top-rated movies.
  - Number of ratings per user.

## Data Visualization
Visualizations include:
- Rating distribution plot.
- Top 10 most rated movies.
- Heatmap showing the correlation between users and movies.
- Genre distribution across the dataset.

## Data Preprocessing
Data cleaning steps include:
- Handling missing values in the ratings and movie datasets.
- Encoding categorical data (like genres) for content-based filtering.
- Normalizing ratings for collaborative filtering.
- Splitting the data into train and test sets.

## Define Target Variable (y) and Feature Variables (X)
- **Target variable (y)**: User ratings for movies.
- **Feature variables (X)**: Movie features (genres, title, etc.) for content-based filtering, or user and movie interactions for collaborative filtering.

## Train Test Split
The dataset is split into training and testing sets using an 80-20 split to evaluate the recommendation models effectively:
```python
from sklearn.model_selection import train_test_split
train_data, test_data = train_test_split(ratings, test_size=0.2, random_state=42)
