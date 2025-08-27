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
  - data/ # Datasets used and created
    - WHI_inflation.csv
    - happy_new.csv
    - happy_normalized.csv
    - world_happiness.csv
  - happiness.ipynb # Initial linear modelling and model comparison
  - happiness_2.ipynb # Modelling using the normalized data
  - happiness_3.ipynb # Fine-tuning the Random Forest Regressor
  - README.MD
  - .gitignore
  - environment.yml
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

# 📊 Model Fine-Tuning for Happiness Prediction
This notebook focuses on optimizing the previously identified best model—Random Forest—using hyperparameter tuning to improve predictive accuracy. The performance gains are modest but measurable. The process can be found in `happiness_3.ipynb`.

## 🔍 Key Analytical Steps
- Baseline
  - Reused Forest following early findings to establish reference scores.
  - Fitted the model again, including inflation features —which did not improve the performance—.
  - `n_estimators = 100`, `max_depth = 5`, `min_samples_split = 5`.
  - Initial Random Forest results: `RMSE = 0.5294`, `R² = 0.7724`.

- Hyperparameter Tuning
  - Used `GridSearchCV` to explore combinations of `n_estimators`, `max_depth`, `min_samples_split`.

- Best parameters for Random Forest Regressor:
  - `n_estimators = 300`
  - `max_depth = 10`
  - `min_samples_split = 4`
  - Random Forest results after tuning: `RMSE = 0.4971`, `R² = 0.7993`
  - Improvement is present but not significative.

- Feature Importance

  Top predictors remain consistent, although the last two—corruption and generosity—showed more relative importance.
  - Social support
  - GDP per capita
  - Healthy life expectancy
  - Perceptions of corruption
  - Generosity


📈 Key Takeaways
- Inflation-related features were ultimately excluded. They did not significantly enhanced model performance.
- Hyperparameter tuning yields slight improvements in accuracy.
- Final Random Forest model is marginally better but not transformative.
- Feature importance remains stable, reinforcing the reliability of social/health predictors.

---
