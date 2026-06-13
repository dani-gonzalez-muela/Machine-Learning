# Fish Species Classification Using Machine Learning

## Project Focus
Classifying fish species from a dataset of 1492 observations using six physical features (weight, lengths L1–L3, height, width) and 7-class species labels. Explored multiple classifiers, feature importance, noise effects, and classification confidence.

## Key Components

### 1. Classifier Training
- Models: KNN, Random Forest, SVM (linear & RBF), QDA, Kernel Logistic Regression.
- Preprocessing: scaling, PCA, non-linear dimension reduction (t-SNE, Kernel PCA).
- Hyperparameters optimized with GridSearchCV.
- Top performers: KNN (~0.93 Kappa), Random Forest (~0.88), SVM-RBF (~0.87).
- Common misclassifications: Bream over-prediction, Silver Bream vs Perch confusion.

### 2. Feature Importance & Selection
- Most influential features: Height, Width, L3.
- Feature selection (Variance Thresholding, F-score, Best Subset) showed all features contribute meaningfully.
- Random Forest preferred all features; SVM and KNN mostly comprehensive.

### 3. Effects of Noise
- **Uncorrelated noise:** RF robust, SVM moderately affected, KNN highly sensitive.
- **Correlated noise:** similar trends; KNN accuracy drops faster.
- Highlights RF’s ensemble robustness and KNN’s distance metric sensitivity.

### 4. Classification Confidence & Label Noise
- Confidence metrics identified ambiguous or potentially mislabeled samples.
- Overlaps between classes (e.g., Perch and Silver Bream) indicate areas for dataset improvement.

## Key Insights
- Stratified splits and Kappa metric handle class imbalance effectively.
- Non-linear dimension reduction captures richer class structures than PCA.
- Height, Width, and L3 drive species distinction.
- Random Forest is robust to noise; KNN is highly sensitive.
- Ambiguous samples point to potential mislabeling and invite dataset refinement.
