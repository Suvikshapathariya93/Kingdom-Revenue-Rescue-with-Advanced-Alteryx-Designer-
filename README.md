# 🐉 Kingdom Revenue Rescue

### Advanced Alteryx Designer | End-to-End E-Commerce Analytics & Automation

> **A portfolio-grade Alteryx project demonstrating advanced data preparation, transformation, blending, analytics, workflow design, validation, optimization, and automation.**

![Alteryx](https://img.shields.io/badge/Alteryx-Designer-blue)
![Data Analytics](https://img.shields.io/badge/Focus-Data%20Analytics-orange)
![SQL](https://img.shields.io/badge/SQL-Data%20Analysis-lightgrey)
![Status](https://img.shields.io/badge/Project-Completed-success)

---

## 🎯 Project Overview

**Kingdom Revenue Rescue** is an end-to-end e-commerce analytics solution built in **Alteryx Designer**.

The project simulates a real-world analytics requirement where business stakeholders need a reliable view of:

* Revenue
* Profitability
* Product performance
* Regional performance
* Returns
* Shipping performance
* Customer and order trends

The objective is not simply to clean a dataset.

The objective is to demonstrate how an **advanced Alteryx workflow can transform raw operational data into a validated, reusable, BI-ready analytical dataset.**

---

# 🏢 Business Problem

Kingdom Commerce has experienced increasing sales, but management is concerned about declining profitability and inconsistent customer experience.

The leadership team wants to understand:

> **Where are we making money, where are we losing money, and what operational factors are contributing to the problem?**

The existing process relies heavily on manually prepared files, making it difficult to:

* Combine multiple sources consistently
* Detect data-quality problems
* Calculate business metrics
* Identify loss-making products
* Monitor returns
* Analyze shipping performance
* Produce repeatable reporting datasets

### Business Goal

Build a scalable Alteryx pipeline that converts raw operational data into a **single source of truth for business reporting and decision-making.**

---

# 🧙 The Data Alchemist Mission

This project is the **Final Boss** of my gamified Alteryx learning journey.

Instead of memorizing individual tools, the capstone focuses on applying Alteryx to a realistic business problem.

```text
Raw Data
   ↓
Data Profiling
   ↓
Data Quality
   ↓
Data Preparation
   ↓
Data Blending
   ↓
Business Logic
   ↓
Advanced Transformations
   ↓
Validation
   ↓
Aggregation
   ↓
Optimization
   ↓
BI-Ready Output
```

---

# 🛠️ Technology Stack

| Technology           | Purpose                          |
| -------------------- | -------------------------------- |
| **Alteryx Designer** | Primary ETL & analytics platform |
| CSV / Excel          | Source data                      |
| SQL                  | Analytical validation            |
| Python               | Optional validation / automation |
| Tableau / Power BI   | Optional visualization           |
| GitHub               | Version control & documentation  |

---

# 📂 Data Sources

The project uses publicly available e-commerce / retail datasets.

### Primary Dataset

**Sample Superstore**

Contains information including:

* Orders
* Customers
* Products
* Categories
* Regions
* Sales
* Quantity
* Discount
* Profit
* Shipping

### Secondary Dataset

**Returns**

Used to enrich order-level information with return status.

---

# 🏗️ Solution Architecture

```text
                    ┌───────────────────┐
                    │   Orders Source      │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Data Profiling &     │
                    │ Quality Checks       │
                    └─────────┬─────────┘
                              │
                              ▼
                    ┌───────────────────┐
                    │ Data Preparation     │
                    │ & Standardization    │
                    └─────────┬─────────┘
                              │
                              ▼
        ┌─────────────────────┴───────────────────┐
        │                                         │
        ▼                                         ▼
┌───────────────┐                         ┌────────────────┐
│ Returns Data    │                         │ Reference Data    │
└───────┬───────┘                         └───────┬────────┘
        │                                         │
        └──────────────────┬──────────────────────┘
                           ▼
                    ┌───────────────┐
                    │ Data Blending   │
                    │ & Join Logic    │
                    └───────┬───────┘
                            ▼
                    ┌───────────────┐
                    │ Transformation  │
                    │ & Metrics       │
                    └───────┬───────┘
                            ▼
                    ┌───────────────┐
                    │ Data Quality    │
                    │ Validation      │
                    └───────┬───────┘
                            ▼
                    ┌───────────────┐
                    │ Aggregation &   │
                    │ Analytics       │
                    └───────┬───────┘
                            ▼
                    ┌───────────────┐
                    │ BI-Ready        │
                    │ Output          │
                    └───────────────┘
```

---

# 🚀 Advanced Alteryx Skills Demonstrated

This project intentionally goes beyond basic Input → Filter → Output workflows.

## 1. Advanced Data Preparation

* Input Data
* Select
* Auto Field
* Data Cleansing
* Filter
* Unique
* Sort
* Record ID
* Sample

### Demonstrated capability

> Preparing inconsistent operational data for downstream analytics while controlling field types, structure, and data quality.

---

# 2. Data Blending & Join Strategy

The workflow combines multiple business datasets using appropriate keys.

### Techniques

* Join
* Union
* Join Multiple
* Field standardization
* Key validation
* Unmatched-record analysis

### Join Validation

The workflow explicitly checks:

```text
Matched Records
      +
Unmatched Left Records
      +
Unmatched Right Records
```

This prevents silent data loss caused by incorrect joins.

---

# 3. Advanced Formula Engineering

Business metrics are created directly within the workflow.

### Profit Margin

```text
Profit / Sales
```

### Shipping Duration

```text
DateTimeDiff(Ship Date, Order Date, "days")
```

### Return Flag

```text
IF [Returned] = "Yes"
THEN 1
ELSE 0
ENDIF
```

### Profitability Classification

```text
IF [Profit] > 0 THEN "Profitable"
ELSEIF [Profit] = 0 THEN "Break Even"
ELSE "Loss Making"
ENDIF
```

### Shipping Classification

```text
IF [Shipping Days] <= 3 THEN "Fast"
ELSEIF [Shipping Days] <= 6 THEN "Normal"
ELSE "Delayed"
ENDIF
```

---

# 4. Date Intelligence

The workflow derives analytical time dimensions including:

* Order Year
* Order Quarter
* Order Month
* Month Number
* Shipping Duration
* Order-to-Ship interval

This allows the final dataset to support time-series analysis and BI reporting.

---

# 5. Business-Level Aggregation

Multiple analytical layers are generated.

### Product Level

* Sales
* Profit
* Quantity
* Orders
* Return Rate
* Profit Margin

### Category Level

* Revenue
* Profit
* Quantity
* Average Discount
* Profit Margin

### Regional Level

* Sales
* Profit
* Orders
* Return Rate

### Monthly Level

* Sales
* Profit
* Orders
* Returns

---

# 6. Analytical Ranking

Products are ranked to identify:

### 🥇 Top Performers

Top products by:

* Sales
* Profit
* Quantity

### 🔴 Risk Products

Products with:

* High sales
* Negative profit

### 💀 Loss Makers

Products where:

```text
Profit < 0
```

This transforms raw transactional data into actionable business intelligence.

---

# 7. Data Quality Framework

A dedicated validation layer is included before final output.

### Checks

* Null critical fields
* Duplicate Order IDs
* Invalid dates
* Invalid numeric values
* Negative quantities
* Missing join keys
* Unexpected categories
* Join mismatches
* Duplicate output records

### Conceptual flow

```text
Source
  ↓
Validation
  ↓
Valid Records -----→ Main Pipeline
  ↓
Invalid Records
  ↓
Data Quality Output
```

This makes data-quality issues visible instead of silently removing them.

---

# 8. Workflow Optimization

The project includes an optimization phase.

### Optimization techniques considered

* Remove unnecessary fields early
* Filter records before expensive transformations
* Minimize unnecessary joins
* Reduce repeated calculations
* Use appropriate data types
* Avoid unnecessary Browse tools in production
* Reuse transformation logic
* Separate development and production outputs

### Before vs After

```text
Version 1
Raw Data
   ↓
Transform
   ↓
Join
   ↓
Filter
   ↓
Aggregate

Version 2
Input
   ↓
Select Required Fields
   ↓
Filter Early
   ↓
Validate
   ↓
Join
   ↓
Transform
   ↓
Aggregate
   ↓
Output
```

The goal is to demonstrate that the workflow is not only correct, but also designed with performance and maintainability in mind.

---

# 🔄 Reusability & Automation

Where appropriate, reusable logic can be converted into a **Standard Macro**.

### Example

```text
Raw Sales File
      ↓
Reusable Cleaning Macro
      ↓
Standardized Dataset
```

The macro can be reused when new files follow the same structure.

### Automation Concepts

The project can also be extended using:

* Dynamic Input
* Dynamic Rename
* Control Parameters
* Batch processing
* Standard Macros
* Workflow dependencies
* Scheduled execution through an Alteryx Server environment

---

# 📊 Final Business Metrics

The final analytical dataset supports metrics such as:

| Metric                | Description                         |
| --------------------- | ----------------------------------- |
| Total Sales           | Overall revenue                     |
| Total Profit          | Overall profitability               |
| Profit Margin         | Profit relative to sales            |
| Total Orders          | Number of orders                    |
| Return Rate           | Percentage of returned orders       |
| Average Discount      | Average discount applied            |
| Shipping Delay Rate   | Percentage of delayed orders        |
| Average Shipping Days | Average order-to-ship duration      |
| Loss-Making Products  | Products generating negative profit |

---

# 🔎 Business Questions Answered

The final workflow should answer:

### Revenue

1. What is total revenue?
2. Which category generates the highest revenue?
3. Which region generates the highest revenue?

### Profitability

4. Which category generates the highest profit?
5. Which products are loss-making?
6. Which products have high sales but negative profit?

### Returns

7. What is the overall return rate?
8. Which categories have the highest return rate?
9. Which regions have the highest number of returns?

### Shipping

10. What percentage of orders are delayed?
11. Which region has the highest shipping delay rate?
12. Does shipping performance differ across product categories?

---

# 🧠 Key Analytical Insight

A key objective of this project is to move beyond:

> **"What happened?"**

toward:

> **"Why might it be happening?"**

For example:

```text
High Sales
     +
Negative Profit
     ↓
Potential Pricing / Discount Problem
```

or:

```text
High Shipping Delays
        +
High Return Rate
        ↓
Potential Operational Problem
```

These relationships should be **validated using the data**, rather than assumed.

---

# 📦 Final Deliverables

The repository contains:

```text
capstone/
│
├── README.md
│
├── workflows/
│   ├── kingdom_revenue_rescue.yxmd
│   └── optimized_workflow.yxmd
│
├── macros/
│   └── data_cleaning_macro.yxmc
│
├── outputs/
│   ├── final_business_dataset.csv
│   ├── product_summary.csv
│   ├── regional_summary.csv
│   └── monthly_summary.csv
│
├── screenshots/
│   ├── workflow_overview.png
│   ├── data_quality.png
│   ├── join_validation.png
│   ├── transformation.png
│   └── final_output.png
│
└── insights/
    └── business_insights.md
```

---

# 📸 Workflow Showcase

## End-to-End Workflow

> Add your Alteryx workflow screenshot here.

```text
loading...
```

---

## 🔍 Data Quality Layer

> Add screenshot of your validation process here.

```text
loading...
```

---

## 🔗 Join Validation

> Add screenshot showing matched and unmatched records.

```text
loading...
```

---

# 📊 Optional BI Layer

The final dataset can be connected to a BI platform to create an executive dashboard.

### Suggested Dashboard

```text
┌─────────────────────────────────────────────┐
│             KINGDOM COMMERCE                        │
│            EXECUTIVE OVERVIEW                       │
├──────────┬──────────┬──────────┬────────────┤
│  SALES   │  PROFIT  │ ORDERS   │ RETURN %           │
├──────────┴──────────┴──────────┴────────────┤
│                                                     │
│       Revenue & Profit Trend                        │
│                                                     │
├─────────────────────┬───────────────────────┤
│ Category Performance│ Regional Performance          │
├─────────────────────┴───────────────────────┤
│           Product Risk Analysis                     │
├─────────────────────────────────────────────┤
│ Shipping & Returns Analysis                         │
└─────────────────────────────────────────────┘
```

---

# 🧪 Validation Strategy

The workflow is considered production-ready only after validating:

### Record-Level Validation

```text
Source Record Count = Expected Processed Record Count
```

### Join Validation

```text
Matched + Unmatched Left = Left Input
```

### Aggregation Validation

```text
Aggregated Sales = Validated Transaction Sales
```

### Business Metric Validation

Selected metrics are independently checked using SQL or another analytical method where applicable.

---

# 🏆 Project Outcome

The completed solution demonstrates the ability to build an analytics workflow that follows a realistic data engineering / BI lifecycle:

```text
                BUSINESS PROBLEM
                       ↓
                    RAW DATA
                       ↓
                 DATA PROFILING
                       ↓
                  DATA QUALITY
                       ↓
                  DATA BLENDING
                       ↓
                  TRANSFORMATION
                       ↓
                 BUSINESS METRICS
                       ↓
                   VALIDATION
                       ↓
                   AGGREGATION
                       ↓
                   OPTIMIZATION
                       ↓
                   BI-READY DATA
                       ↓
                 BUSINESS INSIGHTS
```

---

# 💼 Skills Demonstrated

### Alteryx Designer

* Input Data
* Select
* Filter
* Formula
* Data Cleansing
* Unique
* Sort
* Join
* Union
* Join Multiple
* Summarize
* Cross Tab
* Dynamic Input
* Standard Macro
* Workflow optimization
* Data validation
* Error handling

### Analytics

* KPI development
* Profitability analysis
* Product analysis
* Regional analysis
* Return analysis
* Shipping analysis
* Time-series preparation
* Business problem solving

### Engineering Mindset

* Reusable workflows
* Modular design
* Data-quality validation
* Performance optimization
* Maintainability
* BI-ready outputs

---

# 🌟 What Makes This Project Different?

This project is intentionally designed to demonstrate more than knowledge of individual Alteryx tools.

It demonstrates the ability to:

> **Understand a business problem → design a data pipeline → validate the data → engineer business metrics → optimize the workflow → produce decision-ready outputs.**

That is the difference between **knowing Alteryx** and **using Alteryx professionally**.

---

# 🎮 Final Boss Status

```text                                 
         🐉 CHAOS ENGINE DEFEATED
           ADVANCED DATA ALCHEMIST         
```

---

## 👩‍💻 Author

**Suviksha Pathariya**

BI Developer | Data Engineer | Data Analytics

### Core Skills

`Alteryx` `SQL` `Python` `Tableau` `Power BI` `Data Engineering` `Business Intelligence`

---

## ⭐ If You Find This Project Useful

Feel free to ⭐ the repository and explore the individual levels of the **Data Kingdom** learning journey.

> **Build workflows. Solve problems. Defeat the Chaos Engine.**
