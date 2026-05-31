# Advanced MNIST Digit Classification and Clustering

## Project Focus
Analysis and classification of a modified MNIST dataset with 50,000 handwritten digit images (0-9), using dimensionality reduction, classification pipelines, and clustering to explore structure and label quality.

## Key Components

### 1. Dimensionality Reduction
- Subsampling: random (5,000 samples) and diversified sampling for representative subsets.
- Methods: PCA, Truncated SVD, Sparse PCA, NMF, KPCA, t-SNE, UMAP.
- Findings: KPCA (~60 components) achieved best variance preservation and cluster separation; UMAP provided superior visualization for overlapping digits.

### 2. Classification Performance
- Classifiers: KNN, QDA, SVM (linear & kernel), Logistic Regression, Random Forest, Neural Networks.
- Dimensionality reduction embedded in pipelines; KPCA selected for final models.
- Results: KPCA + SVM/RF/NN yielded best validation accuracy (~0.83). Smaller training sets decreased performance, with QDA most sensitive.

### 3. Clustering Analysis
- Methods: K-means, DBSCAN, Agglomerative hierarchical clustering.
- Findings: K-means identified ~8 clusters corresponding to some digits, but merged others (e.g., 4&7, 6&9). DBSCAN failed; Ward linkage agglomerative clustering partially recovered structure.

## Key Insights
- Diversified sampling improves subset representativeness.
- KPCA provides effective embeddings for classification; UMAP excels in visualization.
- Nonlinear embeddings + robust classifiers (SVM, RF, NN) deliver best accuracy/stability.
- Clustering partially recovers digit structure; overlapping digits and label noise limit perfect separation.
- Future work: ensemble methods, refined embeddings, and active sample cleaning for mislabeled data.
