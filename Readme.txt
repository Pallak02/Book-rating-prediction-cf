Author: Palak Wadhwa
Data606
Project-2

# 📚 Book Rating Prediction using Item-Item Collaborative Filtering

This project implements an item-item collaborative filtering (CF) algorithm to predict how users would rate books they haven't rated, using their previous ratings and the preferences of similar items.

---

##  Description of the Algorithm

- **Collaborative Filtering Type**: Item-Item CF
- **Similarity Measure**: Cosine similarity between book rating vectors
- **Prediction**: Weighted average of the ratings given by the user to `k` most similar books
- **Evaluation Metric**: Mean Absolute Difference (MAD)

---

##  Implementation Choices

- The ratings matrix was filtered to remove users and books with fewer than 10 ratings to reduce sparsity and improve performance.
- Ratings with value `0` were removed as they indicate "not rated".
- Experiments were conducted to observe performance variation with:
  - Neighborhood size `k = 5, 10, 15, 20, 50, 100`
  - Train-test splits from 60% to 90% (in 5% increments)
- Code was written and tested in Google Colab.

---

##  How to Run

1. Upload the dataset files (`Users.csv`, `Books.csv`, `Ratings.csv`) to a folder in your Google Drive.
2. Open the notebook: `Book_Rating_CF.ipynb`.
3. Mount your Google Drive inside the notebook.
4. Set your `data_path` to match the location of your uploaded files.
5. Run all cells in order.

---

##  Dependencies

The following libraries are required:

pandas
numpy
scikit-learn
matplotlib
