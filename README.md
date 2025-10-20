# Business Understanding 
## Project Goal:
Predict H1N1 or seasonal flu vaccination status based on survey responses, i.e, their demographics, opinions, and health behaviors.

## Executive Summary
This project predicts whether individuals received H1N1 or seasonal flu vaccines using demographic, behavioral, and opinion survey data. 
The model identifies key factors influencing vaccine uptake and provides actionable insights for public health authorities to design targeted vaccination campaigns.

## Context
Vaccination is a cornerstone of public health, protecting individuals and communities through direct immunity and herd immunity. Lessons from past campaigns, such as the 2009 H1N1 influenza pandemic, provide insights for guiding current and future vaccination efforts, including for emerging diseases like COVID-19. Understanding factors that influence vaccine uptake can help public health authorities design targeted interventions to improve coverage.

## Stakeholders
1. CDC, WHO, UNICEF, and national Ministries of Health, Public health planners, policymakers, vaccination campaign managers.
2. Predictive insights from this analysis can help identify populations less likely to get vaccinated and guide resource allocation decisions.

## Problem Statement
1. Identify key factors influencing vaccine uptake.
2. Estimate vaccination probabilities for individuals or populations.
3. Guide targeted messaging and interventions to increase coverage.

## Scope and Evaluation
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
 Captures complex interactions
 Robust to noisy or missing data
 ROC-AUC: ~0.827
 Provides feature importance insights

3. Final Model: Multi-Output Logistic Regression
Predicts both H1N1 and seasonal vaccine probabilities simultaneously.
Higher ROC-AUC compared to Random Forest.
Produces probability estimates to prioritize outreach effectively.

| Model                            | H1N1 ROC-AUC | Seasonal ROC-AUC | Notes                                             |
| -------------------------------- | ------------ | ---------------- | ------------------------------------------------- |
| Logistic Regression              | 0.839        | 0.854            | Baseline, interpretable                           |
| Random Forest                    | 0.827        | 0.827            | Captures complex interactions, feature importance |
| Multi-Output Logistic Regression | 0.841        | 0.856            | Final model, probability estimates                |


## Key Predictors
1. Doctor recommendation – Individuals are far more likely to vaccinate if recommended by a healthcare provider
2. Perceived vaccine safety & effectiveness – Beliefs about risk and benefit strongly influence uptake
3. Health worker status – Healthcare workers have higher vaccination rates
4. Household characteristics – The Number of adults and children impacts the likelihood

Implication: Campaigns should emphasize vaccine safety and effectiveness and encourage doctors to proactively recommend vaccination.

## Model Performance & Interpretation
1. ROC-AUC: Measures the model’s ability to distinguish vaccinated vs non-vaccinated individuals
2. Recall: Fraction of actual vaccinated individuals correctly predicted (low recall indicates some vaccinated individuals may be missed, so predictions should guide, not replace, interventions)

## Limitations Section
1. Missing data for some predictors (e.g., employment industry, health insurance)
2. Self-reported surveys may include bias or inaccuracies
3. Class imbalance affects recall for vaccinated individuals

## Actionable Public Health Recommendations
1. Target outreach to hesitant populations
2. Leverage healthcare providers to recommend vaccination
3. Emphasize safety and effectiveness in messaging
4. Prioritize resource allocation based on predicted low vaccination probabilities
5. Monitor predictions and adapt strategies with real-world vaccination data

