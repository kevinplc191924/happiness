# Regression and prediction of the World Happiness Score
This notebook explores factors influencing subjective happiness using regression-based modeling. Drawing on data from the World Happiness Report, it applies feature selection (Lasso), correlation analysis, and linear regression techniques to assess the relative impact of variables such as social support, GDP per capita, freedom, and life expectancy.

To ensure robustness, the analysis includes cross-validation and compares three different models—linear regression, decision tree classifier, and random forest regressor—to predict happiness scores based on the most significant features. Among these, the random forest regressor demonstrates the best generalization performance.

All steps are documented to support reproducibility and ongoing refinement. Future work will aim to incorporate additional features, fine-tune the best model, and further assess performance in terms of predictive power.

---
# Regression and prediction: new dataset
The notebook `happiness_2` applies the same modeling techniques used in `happiness` to train models and predict happiness scores. It uses a larger, machine learning-optimized dataset to enhance prediction.

The results position the random forest regressor as the model with the best performance.

---
# Model fine-tuning: grid search optimization
To enhance model performance, a grid search with cross-validation was applied to the Random Forest Regressor in `happiness_3`. By systematically tuning `n_estimators`, `max_depth`, and `min_samples_split`, the model achieved its best configuration with an R² of 0.7993 and RMSE of 0.4971.

While inflation-related features were tested, they contributed little to predictive power and were ultimately excluded. In contrast, social and health features consistently emerged as the most influential drivers of happiness scores—reinforcing the idea that well-being is shaped more by social and health conditions than by short-term economic fluctuations.

---
