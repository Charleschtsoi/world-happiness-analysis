# World Happiness Analysis (2015-2019)

Statistical analysis of World Happiness Report data to identify key drivers of national well-being across 158 countries.

This is Phase 1 of a multi-phase project:

Phase 1 (Current): Regression analysis and variable importance modeling

Phase 2 (Upcoming): Interactive Streamlit dashboard for data exploration

Phase 3 (Vision): Decision support tool for evidence-based policymaking

Long-term goal: Support GovTech and policymakers in making statistically-informed governance decisions that improve citizen well-being.

## Overview

This project analyzes five years of World Happiness Report data to understand which factors most strongly predict national happiness scores. Through regression modeling and cross-validation, we identify the relative importance of economic, social, and governance factors.

## Key Findings

- **GDP per capita** is the strongest predictor (standardized β = 0.65)
- All six factors are statistically significant (p < 0.01)
- Social support and healthy life expectancy show substantial effects
- Model achieves test RMSE of 0.42 with strong generalization
- **Critical insight**: Raw coefficients are misleading - standardization reveals true variable importance

## Project Structure

world-happiness-analysis/

├── notebooks/

├── Phase_3&4_Visual_Analysis&_Statistical_Estimation.ipynb 

├── Phase_5_Regression_Analysis.ipynb

├── Phase_6_Model_Selection_&Standardized_Variable_Importance_Analysis.ipynb

└── Phase_7_Regularization.ipynb 

├── data/

└── happiness_clean_2015_2019.csv

├── World Happiness Analysis.docx

└── README.md

## Methodology

**Data Cleaning:**
- Schema harmonization across 5 years
- Country name standardization
- Outlier filtering (IQR method, k=3.0)

**Modeling:**
- Multiple linear regression (OLS)
- Train-test split (70/30)
- 5-fold cross-validation
- Heteroskedasticity-robust standard errors (HC3)

**Variables:**
- Outcome: Happiness score (0-10 scale)
- Predictors: GDP per capita, social support, healthy life expectancy, freedom, generosity, corruption perceptions

## Tools & Technologies

- Python 3
- pandas, numpy
- statsmodels, scikit-learn
- matplotlib, seaborn
- Jupyter Notebook

## Results

Model 5 selected as optimal balance of accuracy and interpretability:
- Test RMSE: 0.4200
- Adjusted R²: 0.76
- All predictors significant at p < 0.01

**Standardized Coefficients (Variable Importance):**
1. GDP per capita: 0.65
2. Social support: 0.45
3. Healthy life expectancy: 0.38
4. Freedom: 0.32
5. Corruption (negative): -0.18
6. Generosity: 0.12

## Key Insights

**Standardization matters:** Without standardizing predictors, freedom appeared to be the strongest factor due to its larger raw coefficient. Standardization reveals GDP's true dominance.

**Balanced development needed:** All six dimensions contribute significantly - no single factor drives happiness alone.

## Author

Charles Tsoi  
Data Analytics Project  
November 2025

## License

This project is available for educational and portfolio purposes.
