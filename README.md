# Predictive Analysis of Medical Insurance Payment Durations in South Africa

### A Case Study of LA Health

**Postgraduate Diploma Capstone Project | University of the Western Cape | 2025**

**Author:** Yolisa Velebayi  
**Specialisation:** Data Analytics and Business Intelligence

**Technologies:** Python | Pandas | NumPy | Scikit-learn | Machine Learning | Power BI | Excel | Google Colab

---

## Project Overview

This project explores the use of data analytics and machine learning to predict medical insurance claim payment durations in South Africa, using LA Health as a case study.

Delayed medical insurance payments can affect healthcare providers' cash flow, operational efficiency, and relationships with patients and medical schemes. Understanding the factors associated with these delays can help organisations improve claims processing and financial planning.

The project applies the **CRISP-DM (Cross-Industry Standard Process for Data Mining)** framework to analyse historical medical insurance claims, identify factors influencing payment timelines, develop predictive models, and generate actionable business insights.

The analysis combines Python-based machine learning with business intelligence techniques to support data-driven decision-making.

## Business Problem

Medical insurance claims are not always settled within consistent timeframes. While some claims are processed quickly, others experience significant delays.

These inconsistencies create financial uncertainty for healthcare providers and may affect service delivery and patient satisfaction.

The primary research question was:

**What determines the time frame for processing private medical insurance payments in South Africa?**

The project also investigated:

- How reliably payment durations can be predicted using historical claims and financial data.
- Whether Prescribed Minimum Benefit (PMB) status influences payment timelines.
- Whether contracted and non-contracted healthcare providers experience different payment durations.
- Which financial, demographic, and administrative variables are most strongly associated with payment delays.

## Project Objectives

The main objectives were to:

1. Explore and clean historical medical insurance claims data.
2. Identify patterns and trends in payment durations.
3. Investigate financial, demographic, and administrative factors associated with payment delays.
4. Develop and compare machine learning regression models.
5. Evaluate model performance using appropriate regression metrics.
6. Identify the most influential variables affecting predictions.
7. Generate predicted payment durations and compare them with actual values.
8. Provide practical recommendations for improving claims processing efficiency.

## Tools and Technologies

| Technology | Application |
|---|---|
| Python | Data preprocessing, analysis, and machine learning |
| Pandas | Data cleaning, manipulation, and transformation |
| NumPy | Numerical calculations |
| Scikit-learn | Regression modelling, feature selection, and evaluation |
| Matplotlib | Data visualisation |
| Seaborn | Statistical visualisation |
| Microsoft Excel | Dataset storage and inspection |
| Google Colab | Python development and execution |
| Jupyter Notebook | Documentation of analytical code and results |
| Power BI | Interactive dashboard development and business intelligence |

## Dataset Description

The original dataset contained approximately **50,000 medical insurance invoice records**.

Following data preprocessing, the research analysed **18,967 records**, as reported in the final research report.

The dataset included patient demographics, healthcare provider information, financial variables, and administrative characteristics.

### Key Variables

| Category | Variables |
|---|---|
| Patient Demographics | Patient Age, Gender |
| Financial Information | Total Cashflow, Total Turnover, Total Outstanding |
| Medical Insurance | PMB Status, Medical Aid Option |
| Healthcare Providers | Service Centre, Specialty, Contract Status |
| Administrative Information | Debtor Status, Invoice and Capture Dates |
| Target Variable | Payment_Duration |

The target variable, `Payment_Duration`, was calculated using the difference between the latest and earliest capture dates, measured in days.

## Project Methodology

The project followed the six stages of the CRISP-DM framework.

### 1. Business Understanding

The first stage involved identifying the business problem associated with unpredictable medical insurance payment timelines.

The objective was to understand the factors associated with delayed payments and assess whether historical claims data could support payment-duration predictions.

### 2. Data Understanding

Exploratory analysis was conducted to examine the dataset's structure, variables, distributions, and relationships.

Activities included:

- Reviewing available columns and data types.
- Identifying missing values and duplicate records.
- Examining numerical variables using descriptive statistics.
- Analysing payment-duration distributions.
- Investigating relationships between financial variables and payment durations.
- Comparing payment durations across different claim and provider categories.

### 3. Data Preparation

The dataset underwent preprocessing to improve its suitability for statistical analysis and machine learning.

**Duplicate Removal**

Duplicate records were identified and removed to improve data quality.

**Missing Value Treatment**

- Numerical missing values were handled using mean imputation.
- Selected categorical missing values were assigned an `Unknown` category.

**Outlier Treatment**

The Interquartile Range (IQR) method was applied to selected numerical variables to identify and remove outliers.

**Feature Encoding**

Categorical variables were transformed into numerical representations using one-hot encoding.

**Feature Selection**

Relevant variables were selected for predictive modelling, including financial information, patient demographics, medical insurance characteristics, and healthcare provider details.

### 4. Exploratory Data Analysis (EDA)

Exploratory data analysis was performed to identify trends and relationships associated with medical insurance payment durations.

The analysis examined:

- Distribution of payment durations.
- Descriptive statistics of numerical variables.
- Average payment duration by PMB status.
- Average payment duration by provider contract status.
- Payment durations across healthcare service centres.
- Payment durations across medical specialties.
- Relationships between financial variables and payment duration.

The findings supported feature selection and model development.

### 5. Machine Learning Model Development

Five regression algorithms were developed and evaluated to predict payment duration.

| Model | Description |
|---|---|
| Linear Regression | Baseline model for identifying linear relationships |
| Lasso Regression | Linear regression with regularisation |
| Decision Tree Regressor | Captures nonlinear relationships through decision rules |
| Gradient Boosting Regressor | Ensemble model that improves predictions sequentially |
| Random Forest Regressor | Ensemble model combining multiple decision trees |

The dataset was divided into:

- **70% Training Data**
- **30% Testing Data**

Models were trained using the training dataset and evaluated using the testing dataset.

### 6. Model Evaluation

Model performance was assessed using the following metrics:

**Mean Absolute Error (MAE)**

Measures the average absolute difference between actual and predicted payment durations.

**Mean Squared Error (MSE)**

Measures the average squared prediction error, giving greater weight to larger errors.

**Root Mean Squared Error (RMSE)**

Expresses prediction error in the same unit as payment duration, which is days.

**R-squared (R²)**

Measures the proportion of variation in payment duration explained by the model.

## Machine Learning Results

The **Random Forest Regressor** achieved the strongest predictive performance among the five models evaluated.

### Best Performing Model

| Metric | Result |
|---|---:|
| Model | Random Forest Regressor |
| Mean Absolute Error (MAE) | 4.96 days |
| R-squared (R²) | 0.189 |
| Explained Variation | Approximately 18.9% |

### Model Comparison

The research identified the following results:

- **Random Forest:** Best-performing model, achieving the highest R².
- **Gradient Boosting:** Second-best-performing model.
- **Linear Regression:** Demonstrated limited predictive performance.
- **Lasso Regression:** Demonstrated limited predictive performance.
- **Decision Tree:** Showed evidence of overfitting and produced a negative R².

Although Random Forest outperformed the other models, its R² of 0.189 indicates that a substantial proportion of the variation in payment duration remained unexplained.

The results highlight the potential of machine learning for claims analysis while demonstrating the need for additional predictors and further model improvement.

## Feature Importance Analysis

Feature importance analysis was conducted using the Random Forest model to identify the variables contributing most strongly to payment-duration predictions.

The most influential features identified in the research included:

1. Total Cashflow
2. Total Turnover
3. Patient Age
4. Contract Status
5. PMB Status

These findings suggest that financial characteristics, patient demographics, and healthcare provider arrangements are relevant when predicting claim payment durations.

Feature importance reflects a variable's contribution to the model's predictions and does not necessarily establish a causal relationship.

## Key Research Findings

### 1. Payment Duration

The analysis found that most payments were completed within approximately two weeks, although some claims experienced longer delays.

| Measure | Result |
|---|---:|
| Average Payment Duration | 11.4 days |
| Median Payment Duration | 9 days |

The payment-duration distribution was positively skewed, indicating that a smaller number of claims experienced substantially longer processing periods.

### 2. PMB vs Non-PMB Claims

| Claim Category | Average Payment Duration |
|---|---:|
| PMB Claims | 11.73 days |
| Non-PMB Claims | 10.61 days |

PMB claims experienced longer average payment durations than non-PMB claims.

### 3. Contracted vs Non-Contracted Providers

| Provider Category | Average Payment Duration |
|---|---:|
| Contracted Providers | 10.82 days |
| Non-Contracted Providers | 15.22 days |

Non-contracted healthcare providers experienced longer average payment durations than contracted providers.

These differences highlight the relevance of provider contracting arrangements when investigating claims processing efficiency.

### 4. Prediction Limitations

The machine learning models were more successful in predicting typical payment durations than unusually long delays.

The analysis identified underestimation of payment durations in some complex or high-risk cases.

This suggests that additional information about claims processing, administrative procedures, and payment behaviour could improve future predictive performance.

## Power BI Dashboard

A Power BI dashboard was developed to visualise and communicate the results of the predictive analysis.

The dashboard allowed actual and predicted payment durations to be compared across different demographic, financial, and healthcare provider categories.

The dashboard included:

- Average actual payment duration.
- Average predicted payment duration.
- Prediction error.
- Distribution of actual payment durations.
- Distribution of predicted payment durations.
- Actual versus predicted payment durations by age group.
- Payment-duration comparisons by service centre.
- Payment-duration comparisons by medical specialty.
- Interactive filters for claim and provider characteristics.

The dashboard supported the identification of payment patterns, prediction differences, and areas requiring further investigation.

The prediction dataset used for dashboard development is included as File 4 in the repository.

## Business Recommendations

Based on the research findings, the following recommendations were proposed.

### 1. Improve Claims Processing Efficiency

Investigate opportunities to automate routine administrative tasks and reduce unnecessary manual processing.

### 2. Strengthen Healthcare Provider Relationships

Review provider contracting arrangements and investigate factors contributing to longer payment durations among non-contracted providers.

### 3. Improve Monitoring of Payment Delays

Use analytical dashboards to identify unusual payment patterns, compare provider performance, and monitor delays.

### 4. Improve Predictive Modelling

Explore additional claims-processing and administrative
