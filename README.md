# Movie Recommendation System

This project demonstrates how to build a **Movie Recommendation System** using the MovieLens dataset. The system includes both **content-based filtering** and **collaborative filtering** models.

---

## Project Overview

1. **Dataset**: The [MovieLens dataset](https://grouplens.org/datasets/movielens/) is used for this project. It contains movie ratings and metadata.
2. **Models**:
   - **Content-Based Filtering**: Recommends movies based on their genres using **TF-IDF** and **cosine similarity**.
   - **Collaborative Filtering**: Uses **Singular Value Decomposition (SVD)** to recommend movies based on user rating patterns.
3. **Evaluation**:
   - Root Mean Squared Error (RMSE) for collaborative filtering.
   - Qualitative evaluation for content-based filtering.

---

## Project Structure

```
movie_recommendation_system/
├── movies.csv               # Movie metadata
├── ratings.csv              # User ratings
├── README.md                # Project documentation
├── requirements.txt         # Python dependencies
├── recommendation_system.py # Main script
```

---

## How to Run the Project

### 1. Clone the Repository
```bash
git clone <repository_url>
cd movie_recommendation_system
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Run the Script
Run the `recommendation_system.py` script to train the models and generate recommendations:
```bash
python recommendation_system.py
```

---

## Key Features

### Content-Based Filtering
- Uses **TF-IDF vectorization** to represent movie genres.
- Calculates **cosine similarity** to find similar movies.
- Recommends movies similar to a given movie.

### Collaborative Filtering
- Implements **SVD (Singular Value Decomposition)** for matrix factorization.
- Reconstructs user-movie rating predictions.
- Recommends movies for a specific user based on predicted ratings.

---

## Example Output

### Content-Based Recommendation
```python
Input Movie: Toy Story (1995)
Recommended Movies:
- A Bug's Life (1998)
- Monsters, Inc. (2001)
- Finding Nemo (2003)
```

### Collaborative Filtering Recommendation
```python
Input User ID: 1
Recommended Movies:
- Forrest Gump (1994)
- Pulp Fiction (1994)
- The Shawshank Redemption (1994)
```

---

## Evaluation
- **RMSE** for collaborative filtering: 0.306
- Recommendations tested qualitatively for relevance.

---

## Dependencies
The project requires the following Python libraries:
- pandas
- numpy
- scikit-learn
- scipy

---

## Future Work
- Add user and item biases to collaborative filtering.
- Explore hybrid models combining both filtering techniques.
- Evaluate using metrics like Precision@K and Recall@K.

---

## Acknowledgments
- [MovieLens Dataset](https://grouplens.org/datasets/movielens/)
- [Scikit-learn Documentation](https://scikit-learn.org/)
- [SciPy Documentation](https://docs.scipy.org/doc/scipy/)
