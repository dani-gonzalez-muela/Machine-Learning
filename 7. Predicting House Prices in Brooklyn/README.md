# Brooklyn House Prices Prediction and Analysis

## Project Focus
Analysis and prediction of Brooklyn house sale prices (2003–2017) using public datasets, machine learning models, and explainable AI, with geospatial visualization.

## Key Components

### 1. Data Cleaning & Transformation
- Original dataset: 390,883 rows, 110 features; removed columns with >25% nulls and rows with remaining nulls.
- Transformed sale dates and prices to present value (3% risk-free rate) and removed zero-priced rows (~100K).
- One-hot encoded categorical features, resulting in cleaned dataset of 192,205 rows × 336 columns.

### 2. Data Visualization
- Tableau dashboards to explore temporal trends, average sale prices by health area, zip code, and tax class.
- Observed US housing market trends, high-value areas (Brooklyn Heights, Downtown Fulton, Williamsburg South).

### 3. Predictive Modeling
- **Regression:** Simple linear regression gave poor performance (~16% R²).
- **Binary Classification (above/below median price):** Tested 7 models; XGB Classifier best (accuracy ~79.7%, precision ~80%, recall ~79.5%).
- **Quartile Classification:** XGB Classifier again best (~60% accuracy/precision/recall).

### 4. Explainable AI (XAI)
- SHAP analysis identified key features: gross square feet, year of sale, XCoord, assessed total value, Census Tract 2010.
- Visualized feature impact on predicted price classes via Tableau dashboards.

### 5. Geospatial Analysis
- Estimated Longitude/Latitude from XCoord/YCoord using small subset + linear regression (accuracy ~0.86–0.87).
- Visualized 200K points using Plotly Express and KeplerGL; filtered by neighborhood and year built.
- Produced neighborhood evolution video (e.g., Brooklyn Heights, 1850s–present).

## Key Insights
- XGB Classifier is robust for both binary and quartile classification.
- SHAP values provide interpretable feature importance.
- Geospatial visualization highlights neighborhood trends despite imperfect coordinates.
- Temporal and spatial trends in Brooklyn real estate align with historical events and urban development.
