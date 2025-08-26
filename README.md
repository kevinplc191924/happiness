# 🌍 World Happiness Regression Analysis
## 🎯 Description
This notebook explores factors influencing subjective happiness using regression-based modeling. Drawing on data from the World Happiness Report, it applies feature selection (Lasso), correlation analysis, and linear regression techniques to assess the relative impact of variables such as social support, GDP per capita, freedom, and life expectancy. The work can be found in the `happiness.ipynb` notebook.

## 📊 Project insights
- Random Forest emerged as the most accurate model, better capturing nonlinear relationships between happiness and its predictors. The goal was to predict happiness scores using socio-economic indicators. The initial feature selection was performed using Lasso regression and correlation analysis. Then three models were compared—Linear Regression, Decision Tree, and Random Forest—using the set of relevant features previously identified.

## 🔍 Key Analytical Steps
1. Data Cleaning and Preparation → Drop nulls, standardize column names, and select relevant features.
2. Exploratory Data Analysis → Correlation heatmaps and scatter plots to visualize relationships.
3. Feature Selection → Lasso regression to identify impactful variables.
4. Modeling → Train and evaluation of a Linear Regression, Decision Tree, and Random Forest. Use RMSE and R² for performance comparison.
5. Interpretation → Feature importance from Random Forest highlights GDP, social support, and health as key drivers.

## 🧰 Libraries used

- `pandas` →	Data manipulation
- `numpy` →	Numerical operations
- `matplotlib` → Visualization
- `seaborn` →	Enhanced plotting
- `sklearn` →	Modeling and evaluation

## 📁 Project Structure
```text
- happiness/
  - data/
    - WHI_inflation.csv
    - happy_new.csv
    - happy_normalized.csv
    - world_happiness.csv
  - happiness.ipynb # Initial linear modelling and model comparison
  - happiness_2.ipynb # Modelling using the normalized data
  - happiness_3.ipynb # Fine-tuning the Random Forest Regressor
  - README.MD
  - .gitignore
  - requirements.txt
```
*Note: All steps are documented to support reproducibility and ongoing refinement. Future work will aim to incorporate additional features, fine-tune the best model, and further assess performance in terms of predictive power.*

---

# Regression and prediction: new dataset
The notebook `happiness_2` applies the same modeling techniques used in `happiness` to train models and predict happiness scores. It uses a larger, machine learning-optimized dataset to enhance prediction.

The results position the random forest regressor as the model with the best performance.

---
# Model fine-tuning: grid search optimization
To enhance model performance, a grid search with cross-validation was applied to the Random Forest Regressor in `happiness_3`. By systematically tuning `n_estimators`, `max_depth`, and `min_samples_split`, the model achieved its best configuration with an R² of 0.7993 and RMSE of 0.4971.

While inflation-related features were tested, they contributed little to predictive power and were ultimately excluded. In contrast, social and health features consistently emerged as the most influential drivers of happiness scores—reinforcing the idea that well-being is shaped more by social and health conditions than by short-term economic fluctuations.

---
