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

## 📊 Extended Happiness Regression
This notebook builds on the initial analysis by applying regression models to a larger, machine learning–optimized dataset. The goal remains to predict happiness scores using socio-economic indicators, but with improved data quality and broader feature coverage. The file `happiness_2.ipynb` contains this work.

## 🔍 Key Analytical Steps
- Data Preparation
  - Loaded a refined dataset with more rows and cleaner formatting.
  - Verified column types and handled missing values.

- Feature Selection
  - Applied Lasso regression to identify relevant predictors.
  - Correlation analysis used to assess multicollinearity.
- Model Training and Evaluation
  - Compared Linear Regression, Decision Tree, and Random Forest models.
  - Used RMSE and R² metrics for performance evaluation.
  - Random Forest again outperformed other models, confirming its robustness on larger datasets.
- Feature Importance
  - Visualized top predictors from the Random Forest model.
  - Social support, GDP per capita, and healthy life expectancy ranked highest.

## 📈 Key Takeaways
- Larger datasets improve model generalization and reduce overfitting.
- Random Forest remains the most reliable model for this task.
- Feature importance is consistent with the first notebook, reinforcing the relevance of social and health indicators.

---

# Model fine-tuning: grid search optimization
To enhance model performance, a grid search with cross-validation was applied to the Random Forest Regressor in `happiness_3`. By systematically tuning `n_estimators`, `max_depth`, and `min_samples_split`, the model achieved its best configuration with an R² of 0.7993 and RMSE of 0.4971.

While inflation-related features were tested, they contributed little to predictive power and were ultimately excluded. In contrast, social and health features consistently emerged as the most influential drivers of happiness scores—reinforcing the idea that well-being is shaped more by social and health conditions than by short-term economic fluctuations.

---
