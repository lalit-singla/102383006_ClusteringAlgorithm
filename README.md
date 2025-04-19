# Iris Clustering Analysis with Spectral Clustering, GMM, and Fuzzy C-Means

## Project Overview

This project performs clustering analysis on the Iris dataset using three different clustering algorithms:
- **Spectral Clustering**
- **Gaussian Mixture Models (GMM)**
- **Fuzzy C-Means (FCM)**

The script applies various preprocessing techniques such as standard scaling, min-max scaling, and normalization to explore the effect of different data transformations on clustering performance. The results are evaluated using **Silhouette Score** to assess the quality of clustering.

## Requirements

To run the project, you'll need Python 3.x and the following dependencies:

- `numpy`
- `pandas`
- `matplotlib`
- `seaborn`
- `sklearn`
- `scikit-fuzzy`

You can install the required packages using `pip`:

```bash
pip install numpy pandas matplotlib seaborn scikit-learn scikit-fuzzy
```

## Files

- `clustering_analysis.py`: The main Python script to perform the clustering and visualization.
- `README.md`: This file.

## Dataset

The **Iris dataset** is a well-known dataset in machine learning that consists of 150 observations of iris flowers, with 4 features (sepal length, sepal width, petal length, and petal width) and 3 classes (species).

## How to Run the Code

1. Clone or download the repository.

2. Run the Python script:

```bash
python clustering_analysis.py
```

3. The script will:
   - Preprocess the data using different techniques (`standard`, `minmax`, and `normalized`).
   - Perform clustering with each algorithm for a range of clusters (3, 5, 7).
   - Evaluate the clustering results using the Silhouette Score.
   - Plot the clustered data in 2D using PCA for each combination of algorithm and preprocessing method.

4. The script will print the best clustering result based on the highest **Silhouette Score**.

## Best Clustering Result

After running the analysis, the best clustering result based on the highest **Silhouette Score** is as follows:

```
Best Clustering Result:
Algorithm: GMM
Preprocessing: normalized
Clusters: 3
Silhouette Score: 0.6447
```

## Detailed Explanation of Functions

### `preprocess_data(method, data)`
This function preprocesses the input data based on the selected method. It supports the following preprocessing techniques:
- **Standard Scaling** (`standard`)
- **Min-Max Scaling** with outlier removal (`minmax`)
- **Normalization** using log transformation (`normalized`)

### `run_spectral(X, k)`
Applies **Spectral Clustering** to the data `X` for `k` clusters and returns the cluster labels and silhouette score.

### `run_gmm(X, k)`
Applies **Gaussian Mixture Model** clustering to the data `X` for `k` clusters and returns the cluster labels and silhouette score.

### `run_fcm(X, k)`
Applies **Fuzzy C-Means** clustering to the data `X` for `k` clusters and returns the cluster centers, membership matrix, cluster labels, and silhouette score.

### `visualize_clusters(method, algo_name, clustering_func, data_pca, original_data)`
Visualizes the clustering results using PCA for dimensionality reduction, displaying the clustering results for each preprocessing method, algorithm, and cluster size.

## Output

The script will:
- Print the best clustering algorithm, preprocessing method, number of clusters, and silhouette score.
- Display 3 plots for each preprocessing method and clustering algorithm, showing the results of clustering for 3, 5, and 7 clusters.

## License

This project is licensed under the MIT License.
```

This version includes the best clustering result at the appropriate section. Let me know if you need any further adjustments!
