# Regression and prediction of the World Happiness Score
This notebook explores factors influencing subjective happiness using regression-based modeling. Drawing on data from the World Happiness Report, it applies feature selection (Lasso), correlation analysis, and linear regression techniques to assess the relative impact of variables such as social support, GDP per capita, freedom, and life expectancy.

To ensure robustness, the analysis includes cross-validation and compares three different models —linear regression, decision tree classifier, and random forest regressor— to predict happiness scores based on the most significant features. Among these, the random forest regressor demonstrates the best generalization performance.

All steps are documented to support reproducibility and ongoing refinement. Future work will aim to incorporate additional features, fine-tune the best model, and further assess performance in terms of predictive power.