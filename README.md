# Principal Component Analysis in scikit-learn - Lab

This project demonstrates how to apply Principal Component Analysis (PCA) using scikit-learn on the classic Iris dataset. The goal is to reduce dimensionality while preserving variance and evaluate how this affects classification performance.

Objectives
Implement PCA using scikit-learn
Standardize features before applying PCA
Reduce 4D Iris data → 2D principal components
Visualize the transformed data
Measure explained variance
Compare classification performance using:
Original dataset
PCA-reduced dataset
Visualize decision boundaries using KNN

1. Load Dataset
from sklearn import datasets

2. Standardize Data
from sklearn.preprocessing import StandardScaler


3. Apply PCA
from sklearn.decomposition import PCA
pca = PCA(n_components=2)
X_pca = pca.fit_transform(X_scaled)

4. Visualize Principal Components
plt.scatter(X_pca[:,0], X_pca[:,1], c=y)

5. Explained Variance
Shows how much information is retained after reduction.

6. Classification (KNN)
We compare performance on:
Original 4D dataset
PCA-reduced 2D dataset
from sklearn.neighbors import KNeighborsClassifier

7. Decision Boundary Visualization
We visualize how KNN separates classes in 2D PCA space.

Key Results
PCA reduces features from 4 → 2 dimensions
Retains ~95%+ variance
Classification accuracy remains high
Training becomes faster and simpler
Visualization becomes possible in 2D

Key Takeaways
PCA is useful for dimensionality reduction
It helps with:
Visualization
Speed improvement
Reducing overfitting
Sometimes performance remains similar even with fewer features
