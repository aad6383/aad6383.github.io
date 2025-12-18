---
layout: page
title: Statistical Foundations — Housing Price Analysis
description: Interaction modeling, predictive regression, and model comparison using the Ames Housing dataset
img: assets/img/istockphoto-1488938957-612x612
importance: 1
category: work
---

## 📌 Project Overview

This project applies core statistical modeling principles to analyze housing price dynamics in the **Ames, Iowa Housing dataset**. The work consists of two complementary analyses:

1. **Inference-focused analysis** examining whether the relationship between living area and sale price differs across neighborhoods  
2. **Prediction-focused analysis** comparing multiple regression models using both internal validation metrics and external Kaggle performance  

Together, these analyses highlight how statistical modeling choices impact interpretability, generalization, and predictive accuracy.

**Course:** MSDS 6371 – Statistical Foundations for Data Science  
**Author:** Aayush Dalal  
**Institution:** Southern Methodist University  
**Date:** December 2025

---

## 🧪 Analysis 1 — Neighborhood Interaction Effects

### Research Question
Do different neighborhoods exhibit **different price–area relationships**, or does living area affect sale price uniformly across locations?

### Methodology
An **interaction regression model** was fit using homes from three neighborhoods:
- BrkSide (baseline)
- Edwards
- NAmes  

Above-ground living area was rescaled (per 100 sq. ft.) for interpretability. The interaction terms allow the **slope of sale price vs. living area** to vary by neighborhood.

### Key Findings
- BrkSide shows the **strongest price sensitivity** to living area
- Edwards exhibits a substantially weaker slope
- NAmes falls between the two  

Confidence intervals for neighborhood-specific slopes showed **clear separation**, confirming statistically meaningful differences.

### Model Validation
- Residual diagnostics showed no severe violations of linearity or normality
- Influential observations were identified via Cook’s distance but retained as legitimate market cases

**Conclusion:**  
Neighborhood acts as a **significant effect modifier**, and interaction terms are necessary for valid inference.

---

## 📈 Analysis 2 — Predictive Modeling & Model Comparison

### Objective
Determine which regression model best predicts housing prices on **unseen data**, balancing accuracy and overfitting risk.

### Models Compared
- **SLR:** SalePrice ~ GrLivArea  
- **MLR (2 predictors):** GrLivArea + FullBath  
- **Stepwise MLR:** AIC-selected multivariable model  

### Evaluation Metrics
- Adjusted R²  
- PRESS (leave-one-out prediction error)  
- AIC  
- Kaggle leaderboard score (external validation)

### Results Summary
- The **stepwise model** achieved excellent in-sample fit but performed poorly on Kaggle, indicating **overfitting**
- The **two-predictor model** achieved the best out-of-sample performance
- The simple linear model served as a reasonable but limited baseline

**Conclusion:**  
Moderate model complexity provided the best generalization, reinforcing the importance of validation beyond training metrics.

---

## 📊 Interactive R Shiny Application

To complement the statistical analyses, an interactive **R Shiny application** was developed to visualize the relationship between living area and sale price.

The app allows users to:
- Filter by neighborhood (NAmes, Edwards, BrkSide)
- Adjust point transparency and size
- Toggle a fitted regression line

<iframe
  src="https://aayushdalal2025.shinyapps.io/StatisticalFoundationsProject/"
  width="100%"
  height="900"
  style="border: none;"
></iframe>

---

## 📄 Full Project Report (PDF)

The complete written report includes model formulations, diagnostics, confidence intervals, interpretation, and well-commented R code.

<a href="{{ site.baseurl }}/assets/pdf/Aayush_Dalal_Statistical_Foundations_Project.pdf" target="_blank">
  Download Full Statistical Foundations Report (PDF)
</a>

---

## 🧠 Key Takeaways

- Interaction terms are essential when contextual variables (e.g., neighborhood) modify relationships  
- Strong in-sample metrics do not guarantee predictive performance  
- Simpler, interpretable models can outperform complex alternatives on unseen data  
- Statistical foundations remain critical for responsible data science modeling
