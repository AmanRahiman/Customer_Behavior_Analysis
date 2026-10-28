# Customer_Behavior_Analysis
Data Analytics Project using SQL, Python and Power BI


# Customer Behavior Analytics & Prediction

## Overview

This project analyzes customer shopping behavior to identify purchasing patterns, customer segments, and factors influencing customer decisions.

The project follows a complete data analytics workflow:

**Python → EDA & Data Cleaning → SQL Analysis → Power BI Dashboard → Report → Presentation**

The goal is to transform raw customer data into meaningful insights that can support data-driven business decisions.

---

## Dataset

The project uses a **Customer Shopping Behavior Dataset** containing customer demographic, purchase, product, and behavioral information.

Key attributes include:

- Customer ID
- Age
- Gender
- Item Purchased
- Category
- Purchase Amount
- Location
- Size
- Color
- Season
- Review Rating
- Subscription Status
- Shipping Type
- Discount Applied
- Previous Purchases
- Payment Method
- Frequency of Purchases

---

## Tools & Technologies

| Tool | Purpose |
|---|---|
| **Python** | Data loading, cleaning, and exploratory data analysis |
| **Pandas** | Data manipulation and transformation |
| **NumPy** | Numerical analysis |
| **Matplotlib / Seaborn** | Data visualization |
| **SQL** | Data querying and analytical analysis |
| **PostgreSQL / MySQL / SQL Server** | Relational database analysis |
| **Power BI** | Interactive dashboard and visualization |
| **Gamma** | Project presentation / PPT |
| **Jupyter Notebook** | Python-based analysis |
| **Git & GitHub** | Version control and project sharing |

---

## Project Workflow

### 1. Load Dataset

The dataset was loaded into Python using Pandas for initial inspection and analysis.

```python
import pandas as pd

df = pd.read_csv("customer_shopping_data.csv")

df.head()
df.info()
df.describe()
```

---

### 2. Exploratory Data Analysis (EDA)

Performed exploratory analysis to understand:

- Dataset structure and dimensions
- Data types
- Missing values
- Duplicate records
- Numerical distributions
- Categorical variables
- Customer purchasing patterns
- Product and category trends

Visualizations were created to identify patterns and relationships within the data.

---

### 3. Data Cleaning & Transformation

The dataset was prepared for analysis by:

- Handling missing values
- Checking and removing duplicates where required
- Validating data types
- Identifying potential inconsistencies
- Creating useful customer segments
- Transforming variables for analysis

Example customer segmentation:

- **NEW** – 1 previous purchase
- **RETURNING** – 2–10 previous purchases
- **LOYAL** – More than 10 previous purchases

---

### 4. SQL Analysis

The cleaned dataset was loaded into a relational database and analyzed using SQL.

SQL was used for:

- Filtering records
- Aggregating data
- Customer segmentation
- Category-level analysis
- Product-level analysis
- Revenue analysis
- Ranking products
- Identifying top-performing products

Example:

```sql
SELECT category,
       SUM(purchase_amount) AS total_revenue
FROM customer_shopping_data
GROUP BY category
ORDER BY total_revenue DESC;
```

Window functions were also used to identify the **top 3 most purchased products within each category**.

---

### 5. Power BI Dashboard

An interactive Power BI dashboard was created to provide a visual overview of customer behavior and purchasing trends.

The dashboard includes analysis of:

- Total customers
- Total purchases
- Revenue
- Average purchase amount
- Customer demographics
- Product categories
- Customer segments
- Discount usage
- Purchase trends

Interactive filters and visualizations allow users to explore the data from different perspectives.

---

## Dashboard

The Power BI dashboard provides an interactive view of the key business metrics and customer behavior identified during the analysis.

**Dashboard file:** `PowerBI/Customer_Behavior_Dashboard.pbix`

> Add a screenshot of your Power BI dashboard here.

Example:

```text
![Customer Behavior Dashboard](images/dashboard.png)
```

---

## Key Results

The analysis helped identify:

- Major customer purchasing patterns and trends
- High-performing product categories
- Most frequently purchased products
- Differences in purchasing behavior across customer segments
- Relationship between discounts and purchasing activity
- Customer demographic and seasonal purchasing patterns
- Key metrics that can support business decision-making

The findings were summarized in a final analytical report and presentation.

---

## Project Report

A detailed report was prepared covering:

1. Business Problem
2. Dataset Overview
3. Data Cleaning
4. Exploratory Data Analysis
5. SQL Analysis
6. Power BI Dashboard
7. Key Findings
8. Business Insights
9. Conclusion

**Report:** `Report/Customer_Behavior_Analysis_Report.pdf`

---

## Presentation

A project presentation was created using **Gamma** to communicate the analysis, dashboard findings, and key business insights in a concise format.

**Presentation:** `Presentation/Customer_Behavior_Analytics_Presentation.pdf`

---

## How to Run

### Prerequisites

Install the following:

- Python 3.x
- Jupyter Notebook
- MySQL / PostgreSQL / SQL Server
- Power BI Desktop

### 1. Clone the Repository

```bash
git clone https://github.com/yourusername/customer-behavior-analytics.git
cd customer-behavior-analytics
```

### 2. Install Python Dependencies

```bash
pip install pandas numpy matplotlib seaborn jupyter
```

### 3. Run the Jupyter Notebook

```bash
jupyter notebook
```

Open the notebook located in:

```text
notebooks/customer_behavior_analysis.ipynb
```

### 4. Run SQL Analysis

Import the cleaned dataset into your preferred relational database:

**MySQL / PostgreSQL / SQL Server**

Then execute the SQL scripts available in:

```text
sql/
```

### 5. Open the Power BI Dashboard

Open:

```text
PowerBI/Customer_Behavior_Dashboard.pbix
```

If required, update the database connection settings to match your local SQL server.

---

## Project Structure

```text
customer-behavior-analytics/
│
├── data/
│   └── customer_shopping_data.csv
│
├── notebooks/
│   └── customer_behavior_analysis.ipynb
│
├── sql/
│   └── customer_behavior_queries.sql
│
├── PowerBI/
│   └── Customer_Behavior_Dashboard.pbix
│
├── Report/
│   └── Customer_Behavior_Analysis_Report.pdf
│
├── Presentation/
│   └── Customer_Behavior_Analytics_Presentation.pdf
│
├── images/
│   └── dashboard.png
│
└── README.md
```

---

## Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis
- Python
- Pandas & NumPy
- Data Visualization
- SQL
- Relational Databases
- Data Aggregation
- Window Functions
- Customer Segmentation
- Power BI
- Dashboard Development
- Business Intelligence
- Data-driven Decision Making

---

## Conclusion

This project demonstrates an end-to-end data analytics workflow, starting from raw customer data and progressing through **Python-based analysis, data cleaning, SQL querying, Power BI visualization, reporting, and presentation**.

It showcases the ability to transform raw data into structured analysis and communicate insights in a business-friendly format.
