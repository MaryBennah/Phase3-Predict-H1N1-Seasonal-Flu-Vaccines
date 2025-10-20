# Business Understanding / Problem Definition
To predict whether people got H1N1 and seasonal flu vaccines using information shared about their backgrounds, opinions, and health behaviors

## Context
Vaccination is a cornerstone of public health, protecting individuals and communities through both direct immunity and herd immunity. Lessons from past campaigns, such as the 2009 H1N1 influenza pandemic, provide valuable insights for guiding current and future vaccination efforts, including for emerging diseases like COVID-19. Understanding the factors that influence vaccine uptake can help public health authorities design targeted interventions to improve coverage.

## Stakeholder
The primary stakeholders are public health authorities, such as the CDC, who monitor vaccine coverage and plan immunization campaigns. 
Insights from this analysis can identify populations less likely to get vaccinated and inform resource allocation decisions.

## Problem Statement
This project aims to predict whether an individual received the H1N1 or seasonal flu vaccine based on demographic, behavioral, and opinion-based survey responses. 
Predictive modeling can help:
1. Identify key factors associated with vaccine uptake.
2. Estimate vaccination probability for individuals or populations.
3. Guide targeted public health messaging and interventions.

## Scope and Evaluation
The analysis focuses on one vaccine type (H1N1 or seasonal) and includes:
1. Exploratory Data Analysis (EDA) to understand distributions and relationships.
2. Feature engineering and preprocessing to prepare the data for modeling.
3. Model training using classification algorithms.

Evaluation using accuracy, precision, recall, F1-score, and primarily ROC-AUC to measure predictive performance.

# Business & Data Understanding
## Stakeholder & Problem Context:
  1. Stakeholder: CDC or public health authorities.
  2. Problem: Predict the likelihood of individuals receiving H1N1 and seasonal flu vaccines to target public health interventions.

# Data Summary:
1. 36 columns: respondent_id, 35 features, 2 targets (h1n1_vaccine, seasonal_vaccine)
2. Mixed types: numeric, categorical, binary, ordinal.
3. Multilabel classification problem.
