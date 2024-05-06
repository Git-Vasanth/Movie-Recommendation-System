# Movie Recommendation System

1. Data Collection:
•	You start by importing two datasets, `tmdb_5000_movies.csv` and `tmdb_5000_credits.csv`, which contain information about movies, including their titles, overviews, genres, keywords, cast, and crew.

2. Data Preprocessing:
•	You merge the two datasets based on the movie titles to consolidate the relevant information into a single dataframe.
•	Data cleaning is performed by dropping any rows with missing values.

3. Feature Engineering:
•	You extract and preprocess textual data such as movie overviews, genres, keywords, cast, and crew to prepare them for analysis.
•	The `convert` function is used to extract names from JSON-like string representations of lists of dictionaries.
•	The `fetch_director` function is used to extract director names from the crew list.

4. Text Data Processing:
•	The textual data is tokenized and converted into bag-of-words representations using the `CountVectorizer` from scikit-learn.
•	Stop words (commonly occurring words like "the," "is," etc.) are removed to focus on meaningful content.

5. Similarity Calculation:
•	Cosine similarity is calculated between the bag-of-words vectors of movie descriptions.
•	Cosine similarity measures the cosine of the angle between two vectors and indicates how similar they are irrespective of their magnitude.

6. Recommendation Function:
•	The `recommend` function takes a movie title as input.
•	It finds the index of the input movie in the dataframe.
•	Then, it computes the cosine similarity between the input movie and all other movies.
•	Finally, it sorts the movies based on similarity scores and recommends the top 5 most similar movies.

7. Recommendation Demonstration:
•	You demonstrate the recommendation system by recommending movies similar to "Gandhi."

Overall Process:
1. Data Acquisition: Collect movie data from two CSV files.
2. Data Preprocessing: Merge datasets, clean data, and handle missing values.
3. Feature Engineering: Extract relevant features like genres, keywords, cast, and crew.
4. Text Data Processing: Tokenize and vectorize textual data using CountVectorizer.
5. Similarity Calculation: Compute cosine similarity between movie descriptions.
6. Recommendation: Create a function to recommend similar movies based on user input.

Concepts Used:
Natural Language Processing (NLP): Techniques used to process and analyze textual data.
CountVectorizer: Converts text data into numerical feature vectors.
Cosine Similarity: Measures similarity between vectors irrespective of their magnitude.
Data Cleaning and Preprocessing: Handling missing values and preparing data for analysis.
Feature Engineering: Extracting relevant features from raw data.


