# Unsupervised Learning: K-Means Clustering and PCA

Hello everyone! 👋

This repository is part of my teaching materials on unsupervised learning. It is designed to help both students and professors understand key concepts, formulas, and practical implementation of unsupervised learning techniques like **K-Means Clustering** and **Principal Component Analysis (PCA)**. The material also includes code examples that you can use and modify for your projects. Feel free to explore, learn, and contribute! 😊

---

## 📊 K-Means Clustering

K-Means is a popular clustering algorithm used to group data points into \( k \) distinct clusters. It is an unsupervised method that minimizes the intra-cluster variance while maximizing inter-cluster variance.

### Key Steps in K-Means:
1. Initialize \( k \) cluster centroids randomly.
2. Assign each data point to the nearest cluster centroid (based on Euclidean distance).
3. Recalculate the centroids as the mean of all points in each cluster.
4. Repeat steps 2 and 3 until the centroids stabilize or a stopping criterion is met.

### Formula:
- **Distance Metric** (Euclidean Distance):  
  \[
  d(x_i, c_j) = \sqrt{\sum_{k=1}^{n} (x_{ik} - c_{jk})^2}
  \]
  where \( x_i \) is a data point and \( c_j \) is the centroid of cluster \( j \).

- **Centroid Update**:  
  \[
  c_j = \frac{1}{N_j} \sum_{i \in C_j} x_i
  \]
  where \( N_j \) is the number of points in cluster \( C_j \), and \( x_i \) are the data points.

---

## 🧠 Principal Component Analysis (PCA)

PCA is a dimensionality reduction technique used to transform high-dimensional data into a lower-dimensional space while retaining as much variance as possible.

### Key Steps in PCA:
1. **Standardize the Data**: Subtract the mean and divide by the standard deviation.
2. **Calculate the Covariance Matrix**:
   \[
   \mathbf{C} = \frac{1}{n-1} \mathbf{X}^T \mathbf{X}
   \]
3. **Compute Eigenvalues and Eigenvectors** of the covariance matrix.
4. **Select Principal Components**: Choose the top \( k \) eigenvectors corresponding to the \( k \) largest eigenvalues.
5. **Transform the Data**: Project the original data onto the new feature space:
   \[
   \mathbf{Z} = \mathbf{X} \mathbf{W}
   \]
   where \( \mathbf{W} \) is the matrix of selected eigenvectors.

### Formula:
- **Covariance Matrix**:
  \[
  \mathbf{C} = \frac{1}{n-1} \sum_{i=1}^n (x_i - \bar{x})(x_i - \bar{x})^T
  \]
  where \( \bar{x} \) is the mean vector.

- **Eigenvalue Decomposition**:
  \[
  \mathbf{C} \mathbf{v} = \lambda \mathbf{v}
  \]
  where \( \lambda \) is an eigenvalue and \( \mathbf{v} \) is its corresponding eigenvector.

---

## 🖥️ Using Pretrained Models for Feature Extraction

Pretrained models can be used as feature extractors to reduce memory and computational load in downstream tasks. By passing data through a pretrained model's convolutional or hidden layers, you can obtain feature representations that are highly informative for clustering or classification tasks.

---

## 📂 Contributions

Feel free to suggest improvements, fix errors, or add new examples by submitting a pull request. Let's make this material even more helpful for the community! 😊
