# SmokeBan Analysis — Effect of Workplace Smoking Bans on Smoking Behaviour

## 📖 Overview

This project evaluates the impact of **workplace smoking bans** on individual smoking behaviour using the **SmokeBan dataset (n = 10,000)**. The analysis applies statistical and machine learning techniques to determine whether policy interventions significantly reduce smoking prevalence after adjusting for demographic factors.

Conducted entirely in **R Markdown**, this project demonstrates a full end-to-end data science workflow — from data exploration and assumption testing to predictive modelling and policy interpretation.

---

## ❓ Research Question

> Does the presence of a workplace smoking ban significantly reduce the probability that an individual is a smoker, after controlling for age, education, ethnicity, and gender?

---

##  Dataset

The dataset contains **10,000 observations** with no missing values, ensuring high statistical reliability.

| Variable | Type | Description |
|----------|------|-------------|
| `smoker` | Binary (Outcome) | Current smoking status (yes/no) |
| `ban` | Binary (Key Predictor) | Workplace smoking ban status (yes/no) |
| `age` | Continuous | Age (18–88 years) |
| `education` | Ordinal (5 levels) | Highest educational attainment |
| `afam` | Binary | African-American identity |
| `hispanic` | Binary | Hispanic identity |
| `gender` | Binary | Gender (male/female) |

---

## Methodology

A rigorous analytical pipeline was implemented:

###  Descriptive Analysis
- Frequency distributions and proportions  
- Cross-tabulations of smoking status vs predictors  

###  Data Visualisation
- Bar charts and histograms  
- Forest plots (odds ratios)  
- Predicted probability curves  

###  Assumption Testing
- Multicollinearity: Variance Inflation Factor (VIF)  
- Linearity: Box-Tidwell test  
- Outliers: Cook’s Distance  
- Sample adequacy: Events Per Variable (EPV)  

###  Statistical Testing
- Chi-square test of independence  

###  Predictive Modelling
- **Binary Logistic Regression** to estimate smoking probability  

###  Model Evaluation
- Nagelkerke R²  
- Hosmer–Lemeshow goodness-of-fit test  
- AIC and model deviance  

---

## Results

| Predictor | Odds Ratio | 95% CI | p-value | Interpretation |
|-----------|-----------|--------|---------|----------------|
| **Smoking Ban (yes)** | **0.778** | 0.707 – 0.857 | < 0.001 | **22.2% lower odds of smoking** |
| Education (per level ↑) | 0.613 | 0.585 – 0.643 | < 0.001 | 38.7% lower odds per level |
| Hispanic (yes) | 0.544 | 0.464 – 0.638 | < 0.001 | 45.6% lower odds |
| Gender (female) | 0.838 | 0.761 – 0.922 | < 0.001 | 16.2% lower odds vs male |
| Age | 0.992 | 0.988 – 0.996 | < 0.001 | 0.8% lower odds per year |
| African-American (yes) | 0.869 | 0.728 – 1.037 | 0.119 | Not statistically significant |

### Model Statistics
- **Chi-square:** χ² = 77.54, df = 1, p < 0.001  
- **Effect size:** Cramér's V = 0.088 (small but meaningful)  
- **Nagelkerke R²:** 0.081  

---

## Summary

> Individuals exposed to workplace smoking bans are approximately **22% less likely to smoke**, even after controlling for demographic characteristics.

This provides strong empirical support for smoking ban policies as effective public health interventions.

---

## Conclusion

Workplace smoking bans have a **statistically significant and independent effect** on reducing smoking behaviour. Among all predictors, **education emerges as the strongest determinant**, highlighting the importance of socio-economic and awareness factors in shaping health behaviours.

These findings align with public health policy frameworks such as Nigeria’s **National Tobacco Control Act (2015)** and reinforce the value of regulatory interventions in reducing population-level health risks.

---
