# Movie Recommendation System

## Introduction

Welcome to the Movie Recommendation System! This Python-based project uses the cosine similarity algorithm to recommend movies based on user input. By leveraging the power of machine learning and natural language processing, this system provides personalized movie recommendations using movie descriptions and genres.

## Features

- **Data Preprocessing:**
  - Reads a CSV file containing movie data (id, title, genre, overview).
  - Combines the "genre" and "overview" columns into a new "tags" column.
  - Creates a new DataFrame with "id", "title", and "tags" columns.

- **Feature Engineering:**
  - Converts the "tags" column into a matrix of token counts using `CountVectorizer` from scikit-learn.
  - Transforms the token count matrix into a TF-IDF representation using `TfidfTransformer`.

- **Similarity Calculation:**
  - Calculates cosine similarity between movie vectors using scikit-learn's `cosine_similarity` function.
  - Generates a similarity matrix where each element represents the similarity score between two movies.

- **Recommendation Generation:**
  - Defines a `recommendator` function that takes a movie title as input.
  - Finds the index of the input movie in the DataFrame.
  - Sorts the cosine similarity scores for that movie in descending order.
  - Prints the titles of the top 5 most similar movies.


## Example

Here’s a quick example of how to use the system:

```python
from movie_recommender import recommendator

# Get recommendations for a movie titled "Inception"
recommendator("Inception")
```

## Potential Applications

- Build a basic movie recommendation system.
- Develop more sophisticated recommendation algorithms incorporating user ratings, release dates, and popularity.
- Adapt the system to recommend other items like books, articles, or products.

## Contributing

Contributions are welcome! Please feel free to submit a pull request or open an issue.


## Contact

For any questions or suggestions, please contact [Raktim ] at [raktmxx@gmail.com].

---

Thank you for checking out this project! I hope you find it useful and exciting. Let's make movie recommendations smarter and more personalized! 🎥✨
