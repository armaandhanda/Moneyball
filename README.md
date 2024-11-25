# Moneyball: Predictive Analytics for Baseball Player Performance

## Overview

This project explores the predictive analytics behind baseball player performance, inspired by the book *Moneyball* by Michael Lewis. Using player statistics, we implement various predictive models such as linear regression, decision trees, and random forests to evaluate the impact of individual player metrics on Wins Above Replacement (WAR), a critical baseball statistic. We further analyze the out-of-sample performance of these models and experiment with advanced techniques like cross-validation and XGBoost.

---

## Objectives

1. **Explore Baseball Player Data:**
   - Analyze salary distributions, player positions, and performance metrics.
   - Identify correlations between player statistics and WAR.
2. **Build Predictive Models:**
   - Implement and evaluate linear regression, decision trees, random forests, and XGBoost.
   - Optimize models using cross-validation and parameter tuning.
3. **Assess Model Performance:**
   - Compare models using RMSE, R², and MAE metrics.
   - Examine the trade-offs between model accuracy, interpretability, and complexity.
4. **Provide Practical Insights:**
   - Recommend the best model for evaluating free agents.
   - Offer actionable insights for baseball team managers.

---

## Key Features

1. **Data Exploration and Visualization:**
   - Salary distribution histograms by player position.
   - Correlation matrix for player statistics.
   - Interactive scatterplots for salary vs. hits.

2. **Regression Analysis:**
   - Simple and multiple linear regression models to predict WAR.
   - Inclusion of positional and year-based dummy variables.

3. **Training, Testing, and Cross-Validation:**
   - Out-of-sample evaluation using an 80/20 train-test split.
   - 5-fold cross-validation for robust model performance assessment.

4. **Tree-Based Models:**
   - Decision trees with limited and unlimited depths.
   - Random forest for feature importance and predictive accuracy.

5. **Advanced Techniques:**
   - XGBoost for non-linear modeling with parameter tuning.
   - Comparison of baseline and tuned XGBoost models.

6. **Model Performance Metrics:**
   - Root Mean Squared Error (RMSE)
   - Coefficient of Determination (R²)
   - Mean Absolute Error (MAE)

---

## Tools and Libraries

- **Languages:** R
- **Libraries:**
  - Data Manipulation: `tidyverse`, `dplyr`
  - Visualization: `ggplot2`, `plotly`, `corrplot`
  - Modeling: `caret`, `rpart`, `randomForest`, `xgboost`
  - Utilities: `jtools`, `scales`

---

## Data Description

The dataset includes professional baseball player statistics from 1998 to 2013 with 1,878 observations and 274 variables. Key features used in the analysis:
- **Performance Metrics:** WAR, Hits, Runs, At Bats, Home Runs, On-Base Percentage (OBP), and more.
- **Demographics:** Player Age and Position.
- **Financial Metrics:** Player Salary.

---

## Results

### 1. **Top Model Performances**
| Model                      | RMSE   | R²     | MAE   |
|----------------------------|--------|--------|-------|
| Linear Regression (5-Fold CV) | 0.892 | 0.7855 | 0.670 |
| XGBoost (Tuned)            | 0.906 | 0.7478 | 0.684 |
| Random Forest              | 1.021 | 0.6932 | 0.730 |
| Decision Tree              | 1.134 | 0.6050 | 0.859 |

**Best Model:** Linear Regression with 5-Fold Cross-Validation achieved the highest R² and lowest RMSE, making it the most reliable and interpretable model for predicting WAR.

### 2. **Key Insights**
- **Most Important Variables:** On-Base Percentage (OBP), Runs (R), and Batting Average (BA) are the top predictors of WAR.
- **Correlation Analysis:** Hits and At Bats exhibit the strongest positive correlation (0.98), while Strikeouts (SO) negatively correlate with WAR.
- **Salary Insights:** First Basemen (1B) and Designated Hitters (DH) have the highest average salaries.

### 3. **Advanced Models**
- **XGBoost Tuning:** Parameter tuning improved RMSE and R² but required significant computation.
- **Decision Trees:** Simple trees offer interpretability but underperform due to limited complexity.

---

## Usage

### 1. Clone the Repository
```bash
git clone https://github.com/<username>/moneyball-predictive-analytics.git
cd moneyball-predictive-analytics
