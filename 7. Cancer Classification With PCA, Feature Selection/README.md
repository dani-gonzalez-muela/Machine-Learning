# Cancer Subtype Classification with PCA, Feature Selection, and Noise Robustness

## Project Focus
Classification of cancer subtypes from gene expression data using dimensionality reduction, feature selection, and robustness analysis under label noise.

## Key Components

### 1. Dimensionality Reduction & Feature Selection
- Scaled gene expression data and applied PCA (10–20 components) to reduce dimensionality.
- Tested classifiers: Logistic Regression, KNN, and QDA.
- Feature selection via variance thresholding and ANOVA F-score improved model simplicity and maintained high accuracy.
- Logistic Regression with F-score feature selection achieved best overall results.

### 2. Robustness to Label Noise
- Simulated label noise at 5%, 30%, and 70% across six cancer classes.
- Evaluated classifiers with and without PCA and feature selection.
- Logistic Regression with feature selection retained higher recall and stability under mislabeling.
- PCA reduced robustness to noise; larger training sets improved resilience.

### 3. Key Insights
- Feature selection is crucial for both performance and robustness.
- PCA aids dimensionality reduction but may decrease noise tolerance.
- Classifiers vary in sensitivity to mislabeled data; F-score-based selection enhances stability.
- Visualizations (recall vs mislabeling, heatmaps) provide insight into model behavior across classes.

## Conclusion
The project demonstrates effective cancer classification using dimensionality reduction and feature selection, while highlighting the importance of robustness strategies to handle label noise in high-dimensional biological datasets.
