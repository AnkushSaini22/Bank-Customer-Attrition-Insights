## Bank-Customer-Attrition-Insights-and-Product-Management-Strategy

## Project Overview

This project analyzes a dataset of bank customers to derive insights into customer attrition (whether a customer has left the bank). The goal is to understand key patterns and factors contributing to customer exits and improve business strategies to reduce churn. 

The dataset contains the following key columns:
- **CustomerId**: Unique identifier for each customer.
- **Surname**: Surname of the customer.
- **CreditScore**: Customer's credit score.
- **Geography**: Country of the customer.
- **Gender**: Customer's gender (Male/Female).
- **Age**: Customer's age.
- **Tenure**: Number of years the customer has been with the bank.
- **Balance**: Account balance of the customer.
- **NumOfProducts**: Number of bank products the customer uses.
- **HasCrCard**: Whether the customer has a credit card (1 if yes, 0 if no).
- **IsActiveMember**: Whether the customer is an active member (1 if yes, 0 if no).
- **EstimatedSalary**: The customer's estimated salary.
- **Exited**: Whether the customer exited (1 if yes, 0 if no).
- **Complain**: Whether the customer has complained (1 if yes, 0 if no).
- **Satisfaction Score**: Customer satisfaction score.
- **Card Type**: Type of card the customer holds (e.g., DIAMOND, GOLD).
- **Point Earned**: Points earned by the customer.

## Problem Statement

The primary objective of this analysis is to uncover patterns related to customer attrition. Specifically, we focus on:
- Understanding what factors influence customer exits (`Exited` = 1).
- Identifying patterns between different customer characteristics (e.g., age, tenure, geography, etc.) and attrition rates.
- Analyzing relationships between customer engagement metrics (e.g., satisfaction score, balance, card type) and their likelihood to exit.
- Generating visualizations to communicate key insights clearly.

## Key Insights and Findings

1. **Attrition Rates by Geography and Demographics**
   - The **Geography** column helped in segmenting customers based on their countries (France, Spain, Germany), and comparing attrition rates within each country.
   - We observed patterns in **Gender**, **Age**, and **Balance** that impact the likelihood of exiting the bank. For instance, certain countries and demographic groups (e.g., females in certain age brackets) have higher attrition rates.

2. **Impact of Card Type and Customer Products**
   - Customers who hold **Diamond** or **Gold** cards tend to have different attrition patterns compared to other card types. A more in-depth analysis showed that customers with fewer **NumOfProducts** or no credit card (`HasCrCard = 0`) are more likely to exit.

3. **Satisfaction Score and Exits**
   - A **lower Satisfaction Score** correlates with a higher probability of attrition. The analysis revealed that dissatisfied customers (those with lower satisfaction scores) are significantly more likely to leave the bank.
   
4. **Tenure and Balance Correlation**
   - Customers with a **higher tenure** (longer bank relationship) are less likely to leave. Additionally, a **higher account balance** correlated with lower attrition rates.

5. **Complaints and Exits**
   - Customers who have lodged complaints tend to have higher attrition rates. Complaints appear to be a strong predictor of exits, with the number of complaints being a potential indicator of dissatisfaction.

6. **Gender-wise Analysis**
   - By grouping data based on **Gender**, the analysis showed differing attrition rates between male and female customers, with males exhibiting slightly higher attrition rates in some regions.

## Key Analysis Steps

1. **Data Preprocessing**:
   - The dataset was cleaned and preprocessed, handling missing values and ensuring the correct data types were used for each column.
   - Outliers and inconsistent data points were addressed to ensure valid analysis.

2. **Exploratory Data Analysis (EDA)**:
   - We explored various aspects of the data to identify trends and relationships between features, such as age, balance, and card type.
   - Visualizations like bar charts, histograms, and heatmaps were generated to observe the distribution and correlation of key variables with the target variable `Exited`.

3. **Grouping and Aggregation**:
   - Data was grouped by various features like **Geography**, **Gender**, **Card Type**, and **Tenure** to analyze how these factors contribute to customer exits.
   - For each feature, we computed the sum of `Exited` to understand the number of exits per group, creating visualizations for comparison.

4. **Visualization**:
   - **Bar Charts** and **Stacked Bar Charts** were used to visualize the relationship between categorical variables (e.g., `Geography`, `Gender`, `Card Type`) and customer exits.
   - **Histograms** were plotted for numerical variables like `EstimatedSalary` to understand how salary ranges influence attrition.

## Solutions Implemented

- **Predictive Modeling**: While the focus of this analysis was on data exploration, it lays the groundwork for predictive modeling. Future work would involve using machine learning algorithms (like Logistic Regression, Decision Trees, or Random Forests) to predict customer attrition based on the insights gained.

- **Customer Retention Strategies**: Based on the analysis, strategies to reduce attrition can be developed, such as:
  - Targeting dissatisfied customers with personalized offers.
  - Providing higher-value services or products to customers with fewer products.
  - Improving engagement with customers having low tenure or low satisfaction scores.

## Code Implementation Summary

- **Data Grouping**: We used pandas' `groupby` function to group data by various columns and calculate the sum of exits within each group.
- **Visualizations**: The analysis used `matplotlib` and `plotly` for generating various graphs like bar charts, histograms, and heatmaps, which helped in drawing insights from the data.
- **Correlation Analysis**: We used correlation matrices and heatmaps to identify potential relationships between numerical columns (e.g., `CreditScore`, `Balance`, `Tenure`) and the target variable `Exited`.

---

## Installation Instructions

To run the analysis on your local machine, you will need the following Python packages:

```bash
pip install pandas matplotlib plotly seaborn
```



This README provides a concise summary of your analysis and the findings, making it easy for others to understand the purpose, process, and outcomes of your project.
