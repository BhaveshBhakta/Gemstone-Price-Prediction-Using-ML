## Gemstone Price Prediction

### Project Overview

This project aims to predict the **price of gemstones** based on their physical and quality characteristics. By analyzing features such as carat weight, cut, color, clarity, and dimensions, the goal is to develop a regression model that can accurately estimate the price of a gemstone. This can be a valuable tool for jewelers, appraisers, and consumers in the gem market.

-----

### Technical Highlights

  * **Dataset**: [Kaggle - Gemstone Price Prediction](https://www.kaggle.com/datasets/colearninglounge/gemstone-price-prediction)
  * **Size**: 26967 entries, 11 columns
  * **Key Features**:
      * carat, cut, color, clarity, depth, table, x, y, z (dimensions).
  * **Approach**:
      * **Data Cleaning**: Rows with missing values (in the 'depth' column) were dropped. The `Unnamed: 0` column, an irrelevant index, was also dropped.
      * **Exploratory Data Analysis**: Histograms, Boxplots, and a heatmap were used for visualization to understand data distributions and correlations.
      * **Label Encoding**: Applied to all columns, including categorical features like 'cut', 'color', and 'clarity', as well as the numerical features and the target 'price' (as per the notebook).
      * **Regression Task**: Predicting `price`.
      * **Models Used**:
          * Linear Regression, Ridge, XGBoost Regressor, Random Forest Regressor, AdaBoost Regressor, Gradient Boosting Regressor, Bagging Regressor, Decision Tree Regressor, SVR, K-Nearest Neighbors Regressor.
  * **Best R2 Score**:
      * 0.990 with XGBoost Regressor.
      * 0.989 with Random Forest Regressor.
      * 0.988 with Bagging Regressor.
      * The high R2 scores for ensemble models indicate that these characteristics are excellent predictors of a gemstone's price.

-----

### Purpose and Applications

  * Enable jewelers and appraisers to **estimate gemstone prices** accurately.
  * Assist consumers in understanding the value of a gemstone before making a purchase.
  * Identify the key factors that influence gemstone pricing.
  * Support data-driven decision-making in the gem trade and supply chain.

-----

### Installation

Clone the repository:

```bash
git clone https://github.com/BhaveshBhakta/Gemstone-Price-Prediction-Using-ML.git
cd Gemstone-Price-Prediction-Using-ML
```

Install the necessary libraries:

```bash
pip install pandas numpy seaborn matplotlib scikit-learn xgboost
```

-----

### Collaboration

We welcome contributions to improve the project. You can help by:

  * Re-evaluating the preprocessing step of applying Label Encoding to numerical features; consider using standard scaling for numerical features and only applying encoding to categorical ones.
  * Performing comprehensive hyperparameter tuning and cross-validation for all regression models to maximize predictive performance.
  * Exploring advanced feature engineering techniques, such as creating new features from existing dimensions (e.g., volume).
  * Adding explainability (e.g., SHAP or LIME) to understand which gemstone characteristics are the most significant drivers of price.
