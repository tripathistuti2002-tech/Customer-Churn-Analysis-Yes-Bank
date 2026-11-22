# Yes Bank Customer Churn & Retention Analytics Dashboard

An interactive Power BI dashboard designed to help Yes Bank understand why customers leave, identify high-risk customer segments, and guide targeted retention strategies.



---

## Table of Contents
- [1. Project Overview](#1-project-overview)
- [2. Business Problem](#2-business-problem)
- [3. Objectives](#3-objectives)
- [4. Dataset](#4-dataset)
- [5. Data Model](#5-data-model)
- [6. Data Preparation](#6-data-preparation)
- [7. DAX Measures](#7-dax-measures)
- [8. Dashboard Pages](#8-dashboard-pages)
- [9. Key Findings](#9-key-findings)
- [10. Recommendations](#10-recommendations)
- [11. Tools & Skills](#11-tools--skills)

---

## 1. Project Overview
Yes Bank is a private-sector bank offering savings and current accounts, loans, credit cards, and wealth management across India. Rising customer attrition has directly impacted long-term profitability and customer lifetime value (CLV).

This project builds a **multi-page interactive Power BI dashboard** backed by a **Star Schema** data model, enabling management to monitor churn and retention trends, compare customer segments, and identify high-value customers who exited.

---

## 2. Business Problem
Customer retention is a core strategic priority, yet management lacks a centralized report to evaluate churn patterns, customer demographics, and regional performance. Identifying at-risk segments and measuring retention initiatives manually is slow and fragmented.

**Goal:** Equip decision-makers with an interactive analytics solution that transforms raw banking data into actionable retention strategies.

---

## 3. Objectives
- Build a unified, interactive view of churn and retention performance.
- Track core KPIs: **Total Customers**, **Total Exited Customers**, **Churn Rate**, **Retention Rate**, and **Average Tenure**.
- Compare attrition across **geography, gender, age, and credit card category**.
- Identify **high-value exited customers** (by estimated salary) to support targeted win-back campaigns.
- Enable dynamic cross-filtering by **Year, Month, Gender, Geography, and Credit Card Category**.
- Deliver data-backed recommendations to reduce future customer attrition.

---

## 4. Dataset
The dataset comprises **1 fact table** and **6 dimension tables**:

| Table | Type | Description |
| :--- | :--- | :--- |
| `Bank_Churn` | **Fact** | One record per customer: age, tenure, credit score, estimated salary, active status, exit status, year, and month |
| `CustomerInfo` | **Dimension** | Customer profile details (e.g., surname) |
| `Geography` | **Dimension** | Customer geographical location |
| `Gender` | **Dimension** | Customer gender |
| `Credit card` | **Dimension** | Credit card tier/category |
| `Category` | **Dimension** | Account status classification (Exited vs. Retained) |
| `ActiveCustomer` | **Dimension** | Membership activity status (Active vs. Inactive) |

---

## 5. Data Model
The report uses a **Star Schema** architecture with `Bank_Churn` at the center surrounded by lookup dimensions:

```text
   Gender          Geography       Credit card
      \                |                /
       \               |               /
        +--------- Bank_Churn --------+
       /               |               \
      /                |                \
  Category      ActiveCustomer     CustomerInfo

---
---

## 6. Data Preparation
Performed in **Power Query**:
- Audited and standardized column data types.
- Validated one-to-many relationships between dimension tables and the central fact table.
- Handled missing values, duplicates, and inconsistent entries.
- Renamed technical columns into clean, business-friendly labels.
- Built a dedicated **Date table** to support accurate time-intelligence calculations.
- Verified lookup integrity across all dimension keys.

---

## 7. DAX Measures

| Measure | Purpose |
| :--- | :--- |
| `Total Customers` | Total count of customers in the dataset |
| `Total Exit Customer Count` | Count of customers who closed/exited their accounts |
| `Total Retain Customers` | Count of customers who remained with the bank |
| `Churn Percentage` | Share of total customers who exited |
| `Retention Percentage` | Share of total customers who were retained |
| `Average Tenure of Exited Customers` | Mean duration (in years) exited customers stayed before leaving |
| `Average Tenure of Retained Customers` | Mean duration (in years) active retained customers have stayed |


---

## 6. Data Preparation
Performed in **Power Query**:
- Audited and standardized column data types.
- Validated one-to-many relationships between dimension tables and the central fact table.
- Handled missing values, duplicates, and inconsistent entries.
- Renamed technical columns into clean, business-friendly labels.
- Built a dedicated **Date table** to support accurate time-intelligence calculations.
- Verified lookup integrity across all dimension keys.

---

