---
layout: default
title: "Multivariate Linear Regression"
categories: projects
permalink: /projects/multivariate-linear-regression/
author_profile: true
---

<link rel="stylesheet" href="/assets/css/main.css">
<link rel="stylesheet" href="/assets/css/academicons.css">
<script src="/assets/js/main.min.js"></script>

# Research on the Performance of Interleaved Melt-blown Nonwoven Materials Based on Multiple Linear Regression and Goal Programming

## Abstract

Melt-blown nonwoven materials possess excellent filtration performance and are widely applied in various fields such as medical and health care, filter materials, and environmental protection. This paper, integrating chemical engineering knowledge and employing statistical methods and machine learning, explores the relationships between process parameters and structural variables, and between structural variables and product performance.

- Question 1: Investigate the patterns of change in structural variables and product performance after interleaving and analyze whether the interleaving rate has an influence on these patterns of change.

- Question 2: Study the relationship between process parameters and structural variables, and predict the structural variable data based on the given acceptance distance and hot air speed.

- Question 3: Research the relationship between structural variables and product performance, as well as the relationships among structural variables and among product performance variables. Combined with Question 2, solve for the process parameter values that maximize the product's filtration efficiency.

- Question 4: Under the conditions that the acceptance distance does not exceed 100cm, the hot air speed does not exceed 2000r/min, the thickness does not exceed 3mm, and the compression resilience rate is not less than 85%, solve for the process parameter values that make the filtration efficiency as high as possible and the filtration resistance as low as possible.

For the first issue, the study investigates the patterns of structural changes and product performance alterations after interleaving. Thickness, porosity, compression resilience, filtration resistance, filtration efficiency, and breathability are taken as features. The optimization rate of structural performance indicators is defined. By calculating the optimization rate of structural performance indicators for different interleaving rates with each feature, it is preliminarily analyzed that interleaving significantly enhances overall product performance. For the sub-question, given the numerous features of structural variables and product performance, the study first conducts the **Shapiro-Wilk test** for normality on the experimental data. Since all features satisfy the normal distribution, **Pearson correlation analysis** is considered to calculate the **Pearson correlation coefficient** between the interleaving rate and each feature, finding that thickness, filtration resistance, and filtration efficiency are positively correlated with the interleaving rate, while porosity, compression resilience, and breathability are negatively correlated. The conclusion's correctness is verified using the **one-way ANOVA method**.

Regarding the second issue, the study examines the relationship between process parameters and structural variables. After preprocessing the annex data and identifying outliers in each group of repeated experiments using the average value of the remaining values in the same group for replacement, it is known from the correlation study of the first issue that the correlation coefficient between process parameters and structural variables is very small, indicating their **nonlinear relationship**. To achieve as high accuracy as possible in predicting structural variables corresponding to 8 process parameters, a process-structure relationship model based on the **BP neural network algorithm** is established. The model iterates to minimize the MSE indicator, and the optimal prediction model for each structural variable is found to forecast the combinations of 8 process parameters.

For the third issue, considering the complex relationship between structural variables and product performance, **canonical correlation analysis** is adopted to analyze, showing that structural variables and product performance are highly correlated with significant statistical significance. When studying the internal relationship between structural variables and product performance, **bivariate correlation analysis** is employed, revealing strong correlations between thickness and porosity, and between filtration efficiency and breathability, all passing the significance test. For the sub-question, considering the direct impact of structural variables on filtration efficiency, a **multiple linear regression model** between filtration efficiency and structural variables is established. Using the multiple precursor test method and backward stepwise regression, it is found that porosity has a minor impact on filtration efficiency, suggesting its exclusion to optimize the model. During the solution process, it is discovered that thickness and compression resilience rate have certain collinearity, making it impossible to directly solve the model. Therefore, a linear regression formula between process parameters and thickness, compression resilience rate is considered, substituted into the multiple linear regression equation to establish a **single-objective programming model**. The results are visualized, finding that when the acceptance distance is 23cm and the hot air speed is 1180r/min, the filtration efficiency reaches its maximum value of 90.9228%.

For the fourth issue, based on the research results of the third question, a **multiple linear regression equation** between filtration resistance and structural variables is established. During the study, it is found that filtration resistance has weak associations with porosity and compression resilience rate, thus excluding both converts the multiple linear regression into a simple linear regression. Combined with the regression linear equation between filtration efficiency and structural variables, a **multi-objective programming model** is established with constraints that the acceptance distance shall not exceed 100cm, hot air speed shall not exceed 2000r/min, thickness should ideally not exceed 3mm, and compression resilience rate should ideally not be lower than 85%, aiming for as high filtration efficiency and as low filtration resistance as possible. To seek more Pareto optimal solutions, the **evolutionary multi-objective optimization algorithm NSGA-II** is considered. The solution finds that when the acceptance distance is 15-27cm and the hot air speed is 1120-1207r/min, the conditions can be met.

**Keywords:** Pearson correlation coefficient; BP neural network; Multiple linear regression model; Multi-objective programming model

<br>

## Diagrams and charts

<img src='/images/Q1_HSC.png' style='width: 65%;'>

<img src='/images/Q2_1_HSC.png' style='width: 48%;'>

<img src='/images/Q2_2_HSC.png' style='width: 48%;'>

<img src='/images/Q2_3_HSC.png' style='width: 48%;'>

## Supervisor and proposition source
Chinese Society for Futures Studies

<br>
