# TechnoServe Case Study – Sales Pipeline Conversion Analysis
>  Project Description

TechnoServe is a fictional SaaS (Software-as-a-Service) startup specializing in cloud-based solutions for small and medium enterprises. While the company has a broad portfolio and 600+ employees, it is facing a decline in sales pipeline conversion rates — dropping from 35% in FY 2019-20 to 25% at present.

Since revenue is highly dependent on client acquisition and consumption of services, this decline poses a serious business challenge. The goal of this project is to leverage data analysis and machine learning to understand the root causes of low conversion and provide actionable recommendations.

# Objectives

Develop 4–5 hypotheses for low lead conversion using the dataset and industry context.

Map the issue to a data science problem and outline the solution approach.

Conduct Exploratory Data Analysis (EDA) to identify variables most relevant to conversion.

Discuss at least 3 ML models that could be applied to solve this classification problem.

Define evaluation metrics that align with both the imbalanced nature of the data and business 
outcomes.

# Technologies used 
numpy - version 2.2.6
pandas - version 2.3.0
matplotlib - version 3.10.3
seaborn - version 0.13.2
statsmodels - version 0.14.4
sklearn - version 1.7.0
scipy - version 1.15.3

# Approach

1. Hypothesis Generation

Potential reasons for low conversions could include:

Market saturation and high competition in key cities (Mumbai, Delhi, Bengaluru).

Small-revenue clients (≤100K) dominating the pipeline with higher price sensitivity.

ERP Implementation deals being complex and prone to longer cycles, increasing drop-offs.

Sales velocity and iterations not strongly correlated with conversions, requiring multivariate analysis.

2. Data Science Problem Framing

Problem Type: Binary classification (Won = 1, Loss = 0).

Goal: Predict conversion likelihood for new opportunities and identify key drivers.

Preprocessing: One-hot encoding of categorical variables, scaling numerical variables, handling imbalance with resampling/weights.

3. Exploratory Data Analysis (EDA)

Target Distribution: ~77% Loss vs ~23% Won.

Key Drivers Identified: Technology type, City, Client revenue sizing, Opportunity size.

Sales Velocity: Similar medians across Wins and Losses → not a strong standalone predictor.

4. Candidate Models

Logistic Regression – baseline, interpretable, good for quick insights.

Random Forest / Gradient Boosting (XGBoost, LightGBM) – handle non-linear interactions, robust with categorical + numerical features.

Artificial Neural Networks (ANNs) – useful for capturing complex feature interactions; requires more tuning.

5. Evaluation Metrics

Since the dataset is imbalanced, accuracy is not enough. Instead, we track:

Precision & Recall – to check model’s ability to identify true wins.

F1-Score (for 'Won') – balances precision and recall.

ROC-AUC / PR-AUC – overall model quality.

Recall@K – measures if top-ranked leads include true wins (important for sales prioritization).

Converted Revenue Uplift – ties model predictions back to actual business outcomes.

# Conclusion

The project shows that city, technology type, and client size are stronger predictors of conversions compared to velocity alone. By leveraging ML models and evaluation metrics aligned with business KPIs, TechnoServe can implement a lead scoring system that helps sales teams focus on high-probability opportunities, thereby improving overall pipeline conversion rates.