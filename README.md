# Olist E-Commerce Analytics

An end-to-end data analytics project using Python, SQL, PostgreSQL, and Power BI to analyze e-commerce sales, customer behavior, product performance, delivery operations, and customer satisfaction.

> **Project Status:** In Progress

---

## 📌 Project Overview

This project simulates a real-world Data Analyst workflow.

The objective is to take raw e-commerce data, perform data exploration and quality checks, transform and model the data, analyze it using SQL, and build an interactive Power BI dashboard that converts the analysis into actionable business insights.

The project covers the complete analytics lifecycle:

```text
Raw Data
   ↓
Data Exploration
   ↓
Data Quality Assessment
   ↓
Data Cleaning & Transformation
   ↓
PostgreSQL Database
   ↓
SQL Analysis
   ↓
Data Modeling
   ↓
Power BI Dashboard
   ↓
Business Insights & Recommendations
```

---

## 🎯 Business Problem

An e-commerce business wants to better understand its sales performance and customer experience.

The analysis will investigate questions such as:

- How is revenue changing over time?
- Which product categories generate the most revenue?
- Which regions contribute most to sales?
- How many customers make repeat purchases?
- What is the average order value?
- How long does it take for orders to reach customers?
- Where are delivery delays concentrated?
- How does delivery performance relate to customer reviews?
- Which sellers and product categories require further investigation?

The goal is not only to describe the data, but to translate analytical findings into meaningful business insights.

---

## 📊 Dataset

This project uses the **Olist Brazilian E-Commerce Public Dataset**.

The dataset contains multiple relational tables covering areas such as:

- Customers
- Orders
- Order Items
- Payments
- Reviews
- Products
- Sellers
- Geolocation
- Product Category Translation

The dataset contains approximately 100,000 orders and provides enough relational data to perform sales, customer, product, operational, and customer-experience analysis.

**Dataset source:** Olist Brazilian E-Commerce Public Dataset — Kaggle

> Raw dataset files are intentionally kept outside version control and are not uploaded to this repository.

---

## 🧰 Tech Stack

### Programming & Data Analysis

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn

### Database & SQL

- PostgreSQL
- SQL
- SQLAlchemy

### Business Intelligence

- Power BI
- DAX
- Data Modeling

### Development & Version Control

- VS Code / Antigravity IDE
- Jupyter Notebook
- Git
- GitHub

---

## 🔄 Project Workflow

### 1. Data Exploration

Initial profiling of all source tables to understand:

- Number of rows and columns
- Column names
- Data types
- Missing values
- Duplicate records
- Unique identifiers
- Table-level data grain

---

### 2. Data Quality Assessment

Investigate potential data-quality issues such as:

- Missing values
- Duplicate records
- Invalid or inconsistent values
- Unexpected relationships between fields
- Missing dates in different order statuses
- Referential integrity issues

Data will not be removed automatically. Each issue will be investigated based on its business context before deciding how it should be handled.

---

### 3. Data Cleaning & Transformation

Python will be used to:

- Convert data types
- Standardize date fields
- Handle missing values appropriately
- Detect and investigate anomalies
- Prepare analysis-ready datasets
- Perform validation checks

---

### 4. PostgreSQL Database

The cleaned data will be loaded into PostgreSQL.

The database layer will include:

- Table creation
- Primary keys
- Foreign keys
- Relationships
- Data validation queries
- Analytical views

---

### 5. SQL Analysis

SQL will be used to answer business questions using:

- SELECT
- WHERE
- GROUP BY
- HAVING
- CASE WHEN
- JOINs
- CTEs
- Subqueries
- Window Functions
- Ranking
- Time-based analysis

---

### 6. Data Modeling

The project will use a structured analytical data model containing fact and dimension tables where appropriate.

Example conceptual model:

```text
                 dim_customer
                      |
                      |
dim_product ---- fact_orders ---- dim_date
                      |
                      |
                 dim_seller
```

The final model will be documented in the `docs/` folder.

---

### 7. Power BI Dashboard

A multi-page Power BI dashboard will be developed to communicate the analytical results.

Planned dashboard sections include:

#### Executive Overview

- Revenue
- Orders
- Customers
- Average Order Value
- Repeat Customer Rate
- Average Review Score
- Delivery Performance

#### Customer & Product Analysis

- Customer behavior
- Repeat purchases
- Product category performance
- Revenue contribution
- Regional performance

#### Operations & Customer Experience

- Delivery time
- Estimated vs actual delivery
- Late delivery rate
- Seller performance
- Review scores
- Delivery and customer satisfaction analysis

---

## 📈 Key KPIs

The project will calculate and analyze metrics such as:

| KPI | Description |
|---|---|
| Total Revenue | Revenue generated from analyzed orders |
| Total Orders | Number of orders |
| Total Customers | Number of unique customers |
| Average Order Value | Average revenue per order |
| Repeat Customer Rate | Percentage of customers with repeat purchases |
| Average Review Score | Average customer review rating |
| Average Delivery Time | Average time from purchase to delivery |
| Late Delivery Rate | Percentage of orders delivered after the estimated date |

Final KPI definitions will be documented in the project as the analysis develops.

---

## 📁 Repository Structure

```text
olist-ecommerce-analytics/
│
├── data/
│   ├── raw/
│   └── processed/
│
├── notebooks/
│   └── 01_data_exploration.ipynb
│
├── src/
│   ├── data_cleaning.py
│   ├── data_quality.py
│   └── transformations.py
│
├── sql/
│   ├── 01_schema.sql
│   ├── 02_data_validation.sql
│   ├── 03_analysis_queries.sql
│   └── 04_analytics_views.sql
│
├── powerbi/
│   └── Olist_Ecommerce_Analytics.pbix
│
├── reports/
│   ├── business_insights.md
│   └── data_quality_report.md
│
├── docs/
│   ├── data_dictionary.md
│   └── data_model.png
│
├── .gitignore
├── README.md
└── requirements.txt
```

---

## 🔍 Current Progress

### Completed

- [x] Project structure created
- [x] Raw Olist datasets downloaded and organized locally
- [x] Python virtual environment configured
- [x] Pandas installed
- [x] Initial data loading completed
- [x] Dataset sizes inspected
- [x] Orders table explored
- [x] Missing-value analysis started
- [x] Order status distribution analyzed
- [x] Duplicate order ID check completed
- [x] Git repository initialized
- [x] Initial project commit created
- [x] GitHub repository created
- [x] Local repository connected to GitHub

### In Progress

- [ ] Complete data-quality investigation
- [ ] Create data dictionary
- [ ] Explore all source tables
- [ ] Convert and validate date fields
- [ ] Build Python data-cleaning pipeline

### Planned

- [ ] Load cleaned data into PostgreSQL
- [ ] Create relational database schema
- [ ] Perform SQL analysis
- [ ] Build analytical views
- [ ] Create analytical data model
- [ ] Develop Power BI dashboard
- [ ] Document business insights
- [ ] Write business recommendations
- [ ] Finalize project documentation

---

## 🧠 Skills Demonstrated

This project is designed to demonstrate practical Data Analyst skills including:

- Data Cleaning
- Exploratory Data Analysis
- Data Quality Assessment
- Python / Pandas
- SQL
- Relational Database Design
- Data Modeling
- Statistical Analysis
- KPI Development
- Power BI
- DAX
- Business Intelligence
- Business Problem Solving
- Data Storytelling
- Git & GitHub
- Technical Documentation

---

## 📌 Data Handling

The original raw dataset is not stored in this repository.

The `data/raw/` directory is excluded from version control to keep the repository lightweight and reproducible.

Users reproducing this project should obtain the Olist dataset separately and place the CSV files in:

```text
data/raw/
```

---

## 🚀 Reproducibility

To reproduce the project locally:

1. Clone the repository.
2. Obtain the Olist Brazilian E-Commerce Public Dataset.
3. Place the source CSV files inside `data/raw/`.
4. Create and activate a Python virtual environment.
5. Install the dependencies listed in `requirements.txt`.
6. Run the notebooks and Python scripts.
7. Load the processed data into PostgreSQL.
8. Execute the SQL scripts.
9. Open the Power BI file to explore the final dashboard.

Detailed setup instructions will be added as the project progresses.

---

## 📊 Final Deliverables

The completed project will contain:

- Python exploratory analysis
- Python data-cleaning pipeline
- Data-quality report
- Data dictionary
- PostgreSQL database schema
- SQL analytical queries
- Analytical SQL views
- Data model
- Interactive Power BI dashboard
- Business insights report
- Business recommendations
- Reproducible project documentation

---

## 👤 Author

**Aman Kumar Singh**

MBA — Business Analytics

Interested in Data Analytics, Business Intelligence, SQL, Python, Excel, and Power BI.

---

## 📎 Project Note

This project is being developed incrementally with a focus on understanding the reasoning behind each analytical step rather than simply producing a final dashboard.
