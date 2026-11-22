#  YES Bank Customer Churn & Retention Analytics Dashboard

An end-to-end **Power BI Data Analytics Project** focused on analyzing customer churn, understanding attrition patterns, and identifying opportunities to improve customer retention at YES Bank.

The project uses an interactive, multi-page Power BI dashboard to transform banking customer data into meaningful business insights, helping management identify high-risk customer segments and develop targeted retention strategies.

---

##  1. Business Problem

Customer churn is a major challenge for banking institutions because losing customers affects revenue, profitability, and long-term customer relationships.

YES Bank needs a centralized analytics solution to understand:

- Why are customers leaving the bank?
- Which geographical regions experience higher customer attrition?
- Which age groups and gender segments have higher churn?
- How does customer activity status relate to customer exits?
- Which high-value customers have left the bank?
- How can the bank improve customer retention?

**Business Goal:** Develop an interactive Power BI dashboard to monitor customer churn, identify potential risk segments, and support data-driven customer retention strategies.

---

##  2. Project Objectives

- Analyze overall customer churn and retention performance.
- Track key performance indicators (KPIs), including total customers, exited customers, churn rate, and retention rate.
- Identify customer attrition patterns across geography, gender, age, and credit card categories.
- Compare average tenure between exited and retained customers.
- Identify high-value exited customers using estimated salary.
- Analyze monthly churn and retention trends.
- Provide actionable recommendations to improve customer retention.

---

##  3. Dataset Overview

The project uses a banking customer churn dataset containing customer demographic, financial, and behavioral information.

### Key Attributes

| Attribute | Description |
|---|---|
| Customer ID | Unique customer identification |
| Credit Score | Customer credit score |
| Geography | Customer location |
| Gender | Customer gender |
| Age | Customer age |
| Tenure | Number of years associated with the bank |
| Balance | Customer account balance |
| Products | Number of bank products owned |
| Credit Card | Credit card ownership status |
| Active Member | Customer activity status |
| Estimated Salary | Estimated annual customer salary |
| Exited | Customer churn status |

**Data Model:** 1 Fact Table and 6 Dimension Tables.

---

##  4. Tools & Technologies

| Tool | Purpose |
|---|---|
| Power BI Desktop | Dashboard development and visualization |
| Power Query | Data cleaning and transformation |
| DAX | Calculated measures and KPI development |
| Data Modeling | Star Schema and relationship management |
| Microsoft Excel | Data inspection and validation |

---

##  5. Project Workflow

1. **Data Understanding:** Explored the dataset and identified relevant business attributes.
2. **Data Cleaning:** Handled missing values, duplicates, inconsistent entries, and data types using Power Query.
3. **Data Modeling:** Designed a Star Schema with a central fact table and supporting dimension tables.
4. **DAX Development:** Created measures for customer count, churn percentage, retention percentage, and average tenure.
5. **Dashboard Development:** Built five interactive report pages with charts, KPI cards, slicers, and navigation.
6. **Business Analysis:** Evaluated churn patterns and developed recommendations to improve customer retention.

---

##  6. Data Model

Implemented a Star Schema approach to organize customer information and simplify analytical reporting.

**Fact Table:**
- `Bank_Churn`

**Dimension Tables:**
- `CustomerInfo`
- `Geography`
- `Gender`
- `Credit Card`
- `Category`
- `ActiveCustomer`

The model supports customer segmentation, geographical comparisons, and churn analysis.

A dedicated Date table is required for reliable month sorting and time-based analysis; its implementation should be verified in the final model.

---

##  7. Key DAX Measures

Developed DAX measures to calculate important business KPIs.

| DAX Measure | Business Purpose |
|---|---|
| Total Customers | Calculates the overall customer base |
| Total Exit Customer Count | Counts customers who exited the bank |
| Total Retain Customers | Counts customers retained by the bank |
| Churn Percentage | Calculates the percentage of exited customers |
| Retention Percentage | Calculates the percentage of retained customers |
| Average Tenure of Exited Customers | Measures the average tenure of customers who left |
| Average Tenure of Retained Customers | Measures the average tenure of retained customers |

### Core KPI Formulas

**Churn Rate:**

$$\text{Churn Rate} = \left(\frac{\text{Exited Customers}}{\text{Total Customers}}\right) \times 100$$

**Retention Rate:**

$$\text{Retention Rate} = \left(\frac{\text{Retained Customers}}{\text{Total Customers}}\right) \times 100$$

---

##  8. Dashboard Pages & Visualizations

The Power BI report consists of five interactive pages.

### Page 1: Home Dashboard
- YES Bank-inspired landing page.
- Project title and dashboard navigation.
- Navigation buttons to access different analytical pages.

### Page 2: Customer Churn Overview

**Purpose:** Provides an executive-level overview of customer attrition and retention performance.

**KPIs:**
- Total Customers
- Total Exited Customers
- Churn Percentage
- Retention Percentage
- Average Tenure of Exited Customers

**Visualizations:**
- Monthly Churn Rate Trend – Line Chart
- Customers by Geography and Active/Inactive Status – Bar Chart
- Churn Rate by Gender – Pie Chart

**Filters:** Year, Month.

### Page 3: Customer Demographics

**Purpose:** Analyzes customer distribution and demographic patterns.

**Visualizations:**
- Exited Customers by Credit Card Category – Clustered Bar Chart
- Customers by Geography and Credit Card Category – Stacked Bar Chart
- Customer Distribution by Gender – Pie Chart

**Filters:** Geography, Gender.

### Page 4: Churn Factors Analysis

**Purpose:** Identifies customer segments and factors associated with higher attrition.

**Visualizations:**
- Churn Rate by Geography and Gender – Matrix
- Exited vs. Retained Customers by Geography – Clustered Column Chart
- Exited vs. Retained Customers by Age – Line Chart
- Average Tenure of Exited vs. Retained Customers – Bar Chart
- Top 10 Exited Customers by Estimated Salary – Table

**Filters:** Credit Card Category, Gender.

### Page 5: Retention Analysis

**Purpose:** Evaluates customer retention performance and customer loyalty patterns.

**KPIs:**
- Retention Percentage
- Total Retained Customers

**Visualizations:**
- Monthly Retention Rate Trend – Area Chart
- Retained Customers and Retention Rate by Geography and Gender – Combo Chart
- Retained Customers by Gender – Doughnut Chart
- Exits by Credit Card Category – Doughnut Chart

**Filters:** Year, Gender.

---

##  9. Key Business Questions Answered

The dashboard is designed to answer the following business questions:

1. What is the overall customer churn rate?
2. How many customers have exited compared to retained customers?
3. Which geographical region has the highest customer attrition?
4. Which gender segment experiences higher churn?
5. Which age groups contribute most to customer exits?
6. How does customer tenure differ between exited and retained customers?
7. Which credit card category has the highest number of exits?
8. How does customer activity status relate to churn?
9. What are the monthly churn and retention trends?
10. Who are the top 10 high-value customers who exited the bank?

---

##  10. Business Recommendations

Based on the analytical framework, the following strategies can support customer retention:

- **Targeted Retention Campaigns:** Focus on customer segments and geographical regions with higher churn rates.
- **High-Value Customer Recovery:** Prioritize personalized win-back campaigns for high-value exited customers.
- **Early Engagement:** Identify tenure patterns associated with customer exits and introduce proactive engagement.
- **Customer Re-engagement:** Develop targeted campaigns for inactive customers.
- **Performance Monitoring:** Track monthly churn and retention KPIs to evaluate the effectiveness of retention initiatives.
- **Customer Segmentation:** Design personalized banking offers based on customer demographics and product categories.

---

##  11. Skills Demonstrated

- Power BI Dashboard Development
- Data Cleaning & Transformation
- Power Query
- DAX Calculations & Measures
- Star Schema Data Modeling
- Data Visualization
- KPI Development
- Customer Segmentation
- Business Intelligence
- Exploratory Data Analysis
- Business Problem Solving
- Data-Driven Decision Making

---

##  12. Project Quality & Validation

The dashboard was reviewed for analytical accuracy and visualization quality.

Key improvements identified during the review include:

- Correcting monthly churn and retention trend axes.
- Using churn percentage instead of gender ID counts.
- Comparing exited and retained customer tenure using separate measures.
- Applying a Top 10 filter to high-value exited customers.
- Correcting visual fields to display actual retained and exited customer counts.
- Adding a dedicated Date table for accurate month sorting.
- Removing duplicate DAX measures and validating data relationships.
- Cross-checking dashboard KPIs against the source dataset.

These validation steps help ensure reliable reporting and meaningful business insights.

---

##  13. Project Outcome

Developed a multi-page interactive Power BI dashboard that brings customer churn and retention analytics into a centralized reporting solution.

The project demonstrates how Power BI, DAX, Power Query, and data modeling can be combined to analyze customer behavior, monitor business KPIs, identify customer attrition patterns, and support strategic retention decisions.

---

**Project Category:** Business Intelligence & Data Analytics  
**Domain:** Banking & Financial Services  
**Primary Tool:** Microsoft Power BI  
**Author:** Stuti Tripathi
