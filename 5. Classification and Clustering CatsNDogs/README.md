# CATs vs DOGs Image Classification and Clustering

## Project Focus
Evaluation of supervised and unsupervised learning methods on 64x64 grayscale images of cats and dogs, including simulations on sample size and class imbalance.

## Key Components

### 1. Supervised Learning
- **Deep Learning:** CNN achieved up to 95% validation accuracy, some overfitting observed.
- **Classical ML:** SVM, KNN, Logistic Regression, Naive Bayes on flattened images; SVM best (~80-85% accuracy).
- **Misclassification Analysis:** Visualized errors; pixel importance heatmaps showed key regions.

### 2. Unsupervised Learning / Clustering
- PCA for dimensionality reduction and visualization.
- **K-Means & K-Medoids:** Low accuracy and silhouette scores, limited separability.
- **Hierarchical Clustering:** Ward linkage confirmed poor clustering performance.
- Visualization of clusters and centroids in PCA space.

### 3. Simulation Studies
- Explored effect of increasing training sample size (10–190) on KNN, SVM, QDA, Logistic Regression, Gradient Boosting, RF, and Neural Networks.
- Patch-wise classification (16x16 patches) revealed upper head patches most informative.
- SVM and KNN performed best; QDA struggled; neural networks showed inconsistent accuracy.

### 4. Imbalanced Data Analysis
- Simulated increasing dog class proportion.
- All models overclassified dogs as imbalance grew, highlighting sensitivity to class imbalance.

## Key Insights
- CNNs excel with large data but can overfit small datasets.
- SVM and KNN robust across sample sizes and patch-wise analysis.
- Clustering poorly separates cats vs dogs due to high similarity in feature space.
- Class imbalance significantly affects predictive performance, emphasizing need for proper sampling or weighting.
