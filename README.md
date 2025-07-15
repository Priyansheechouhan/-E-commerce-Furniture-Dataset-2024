# -E-commerce-Furniture-Dataset-2024

## 📊 Product Sales Prediction: Model Training and Evaluation

This project focuses on predicting product sales using machine learning models based on features such as product title, price, discount, and shipping information. The models trained include Random Forest Regressor and Gradient Boosting Regressor.

## 📁 Dataset Overview

The dataset includes the following features:

- `productTitle`: Title of the product (converted to numeric using TF-IDF)
- `title_length`: Length of the product title
- `originalPrice`: Original price of the product
- `price`: Current price of the product
- `sold`: Number of units sold (target variable)
- `tagText`: Shipping tag (e.g., "Free shipping")
- `has_free_shipping`: Binary indicator for free shipping
- `price_bin`: Binned price categories
- `discount_pct`: Discount percentage
- TF-IDF features derived from `productTitle`

## 🛠️ Data Preprocessing

- **TF-IDF Transformation** applied to `productTitle` with a maximum of 100 features.
- Dropped non-numeric columns such as `tagText` and `price_bin`.
- Performed train-test split (80% training, 20% testing).
- Standardized all numeric features using `StandardScaler`.

## 🤖 Model Training & Evaluation

### 🔹 Random Forest Regressor
- RMSE: 130.737  
- MAE: 35.157  
- R² Score: -2.117

### 🔹 Gradient Boosting Regressor
- RMSE: 204.197  
- MAE: 35.834  
- R² Score: -6.604

**Note:** Both models showed poor performance, with negative R² scores, suggesting poor generalization to the test set.

## 🔍 Feature Importance

Top 10 features identified by the Random Forest Regressor:

1. adjustable (0.180)  
2. round (0.122)  
3. simple (0.116)  
4. chair (0.107)  
5. swing (0.086)  
6. portable (0.081)  
7. shelf (0.049)  
8. stand (0.046)  
9. originalPrice (0.041)  
10. folding (0.039)

## 📊 Visualizations

- A bar plot of the top 20 important features was generated to visualize feature impact.

## ⚠️ Challenges & Limitations

- Negative R² scores indicate poor model performance.
- Potential overfitting or lack of relevant features.
- Possible data quality issues or noise in the dataset.

## ✅ Recommendations

- Add new features like product category, brand, or reviews.
- Try advanced text vectorization (Word2Vec, BERT).
- Perform hyperparameter tuning.
- Experiment with other models such as XGBoost or neural networks.
- Use cross-validation for better evaluation.

## 📌 Conclusion

Though the models performed poorly, the feature importance analysis revealed useful insights into which product listing elements might influence sales. Further work should include improved feature engineering, richer data, and more robust models.

