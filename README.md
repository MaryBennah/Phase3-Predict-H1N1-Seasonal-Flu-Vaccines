# Business Understanding / Problem Definition
## Project Goal:
Predict whether individuals received the H1N1 or seasonal flu vaccines using information about their demographics, opinions, and health behaviors.

## Context
Vaccination is a cornerstone of public health, protecting individuals and communities through direct immunity and herd immunity. Lessons from past campaigns, such as the 2009 H1N1 influenza pandemic, provide insights for guiding current and future vaccination efforts, including for emerging diseases like COVID-19. Understanding factors that influence vaccine uptake can help public health authorities design targeted interventions to improve coverage.

## Stakeholders
Primary stakeholders include public health authorities such as the CDC, WHO, UNICEF, and national Ministries of Health. Predictive insights from this analysis can help identify populations less likely to get vaccinated and guide resource allocation decisions.

## Problem Statement
This project aims to predict whether an individual received the H1N1 or seasonal flu vaccine based on demographic, behavioral, and opinion-based survey responses.
Predictive modeling can:
1. Identify key factors associated with vaccine uptake.
2. Estimate vaccination probability for individuals or populations.
3. Guide targeted public health messaging and interventions.

## Scope and Evaluation
The analysis focuses on one vaccine type (H1N1 or seasonal) and includes:
1. Exploratory Data Analysis (EDA) to understand distributions and relationships.
2. Feature engineering and preprocessing to prepare data for modeling.
3. Model training using classification algorithms.
4. Evaluation using accuracy, precision, recall, F1-score, and primarily ROC-AUC to measure predictive performance.

## Business Value
Predictive insights enable public health officials to:
1. Identify groups with lower vaccination rates.
2. Design more effective, data-driven vaccination campaigns.
3. Allocate resources efficiently to increase overall vaccine coverage.

## Models Used
1. Baseline: Logistic Regression
Simple, interpretable, and provides insight into important predictors.
Achieved ROC-AUC of 0.839 (H1N1) and 0.854 (Seasonal flu).

2. Random Forest
Captures complex interactions and is robust to missing/noisy data.
Slightly lower ROC-AUC (~0.827) but provides feature importance insights.

3. Final Model: Multi-Output Logistic Regression
Predicts both H1N1 and seasonal vaccine probabilities simultaneously.
Higher ROC-AUC compared to Random Forest.
Produces probability estimates to prioritize outreach effectively.

## Key Predictors

1. Doctor recommendation – Strongest influence on vaccination.
2. Perceived vaccine safety and effectiveness – Beliefs directly affect uptake.
3. Health worker status – Healthcare workers vaccinate at higher rates.
4. Household characteristics – Number of adults and children influences likelihood.
