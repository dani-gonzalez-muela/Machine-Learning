# Machine Learning Projects

## Overview
This collection showcases a range of machine learning applications, spanning image classification, regression, classification, clustering, and robustness analysis. Projects use classical ML models, ensemble methods, and deep learning techniques to tackle tasks such as fish species recognition, digit classification, image analysis, genomic feature classification, house price prediction, and cancer subtype detection.

## Projects

### 1. Fish Species Classification
- **Objective:** Classify 7 fish species from 1492 observations using six physical features.
- **Models:** KNN, Random Forest, SVM (linear & RBF), QDA, Kernel Logistic Regression.
- **Results:** KNN (~0.93 Kappa), Random Forest (~0.88), SVM-RBF (~0.87). 

### 2. Modified MNIST Digit Classification and Clustering
- **Objective:** Classify 50,000 handwritten digits (0-9) and explore clustering structures.
- **Methods:** Dimensionality reduction (KPCA, UMAP), classification (SVM, RF, NN), clustering (K-means, DBSCAN, Agglomerative).
- **Results:** KPCA + SVM/RF/NN ~83% validation accuracy.

### 3. CATs vs DOGs Image Classification
- **Objective:** Classify 64x64 grayscale cat and dog images; assess supervised/unsupervised learning and simulation effects.
- **Models:** CNN, SVM, KNN, Logistic Regression, Naive Bayes; PCA + clustering.
- **Results:** CNN validation accuracy up to 95%; SVM classical models ~80–85%.

### 4. Bagging vs Boosting on Noisy Genomic Data
- **Objective:** Compare ensemble methods on multi-class genomic data under varying label noise (0–70%).
- **Models:** Random Forest (Bagging), Gradient Tree Boosting (Boosting).
- **Results:** Baseline recall: RF ~99%, Boosting ~98% at 0% noise.

### 5. Brooklyn House Prices Prediction
- **Objective:** Predict sale prices using structured data, geospatial analysis, and XAI.
- **Models:** Linear Regression, XGB Classifier (binary & quartile classification).
- **Results:** XGB Classifier accuracy ~79.7% (binary), ~60% (quartiles); geospatial prediction R² ~0.86–0.87.

### 6. Cancer Subtype Classification
- **Objective:** Predict six cancer subtypes from gene expression data; test PCA, feature selection, and noise robustness.
- **Models:** Logistic Regression, KNN, QDA.
- **Results:** Logistic Regression + F-score selection maintained highest accuracy and recall.

### 7. Customer Classification
- **Objective:** Predict customer segments using structured attributes.
- **Models:** Decision Trees, Random Forest, Logistic Regression.
- **Results:** Validation accuracy ~75%.

### 8. Customer Segmentation
- **Objective:** Group customers into meaningful clusters for marketing or analysis.
- **Models:** K-Means, Agglomerative Clustering.
- **Results:** Silhouette score ~0.42.
