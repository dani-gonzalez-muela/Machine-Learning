# Bagging vs Boosting on Noisy Multi-Class Genomic Data

## Project Focus
Comparative analysis of Bagging (Random Forest) and Boosting (Gradient Tree Boosting) classifiers on genomic datasets with injected label noise (0–70%), evaluating performance and feature importance stability.

## Key Components

### 1. Data & Noise Injection
- Dataset: 2000 genomic features, 6 classes (BC, GBM, KI, LU, OV, U), no missing values.
- Synthetic label noise: 0%, 20%, 45%, 70% by reassigning class labels.
- Noisy datasets stored as `.npy` files for efficient reuse.

### 2. Bagging (Random Forest)
- Bootstrap aggregating with n_estimators=20.
- Evaluated weighted recall; performance decreases linearly with noise (baseline ~99% at 0% noise).
- Feature importance computed via permutation; number of "important" features rises with noise (53 → 842).
- Top features at 0% noise mostly lost under noise.

### 3. Boosting (Gradient Tree Boosting)
- Sequential weak learners (max_depth=3, n_estimators=15) correcting previous errors.
- Weighted recall decreases with noise (baseline ~98% at 0% noise).
- Feature importance more stable and consistent across noise levels (50–100 features), less sensitive than bagging.

### 4. Comparison & Insights
- Both methods show near-identical recall at 0% noise and degrade gracefully with increasing noise.
- Boosting provides more stable top feature selection, aiding interpretability in genomic contexts.
- Bagging is simple and effective, but boosting better mitigates spurious feature effects from noise.
- Common key features (e.g., Features 3, 1871) captured biological signal shared by both methods.
