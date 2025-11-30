# Customer Shopping Behavior Analysis 🛍️

## 📌 Project Overview
This project analyzes customer shopping behavior using a transactional dataset of **3,900 purchases** across various product categories. The goal is to uncover insights into spending patterns, customer segmentation, and product preferences to guide strategic business decisions.

The project follows a full data analysis pipeline: **Data Cleaning (Python) → Data Storage & Analysis (PostgreSQL) → Visualization (Power BI).**

## 🛠️ Tech Stack
* **Python (Pandas):** Data cleaning, preprocessing, and feature engineering.
* **SQL (PostgreSQL):** Structured data querying and business logic analysis.
* **Power BI:** Interactive dashboard for visual storytelling.

## 📂 Dataset Description
The dataset consists of **3,900 rows and 18 columns**, capturing:
* **Customer Demographics:** Age, Gender, Location, Subscription Status.
* **Purchase Details:** Item Purchased, Category, Purchase Amount, Size, Color, Season.
* **Behavioral Metrics:** Discounts Applied, Previous Purchases, Frequency, Ratings.

## 🔄 Project Workflow

### 1. Data Cleaning & Feature Engineering (Python)
Before analysis, the raw data was processed to ensure quality:
* **Handling Missing Data:** Imputed missing values in the `Review Rating` column using the median rating of each product category.
* **Feature Engineering:**
    * Created `age_group` by binning customer ages (Young Adult, Middle-aged, Adult, Senior).
    * Derived `purchase_frequency_days` from purchase data.
* **Standardization:** Renamed columns to snake_case and removed redundant features (e.g., `promo_code_used`).
* **Database Integration:** Connected Python to PostgreSQL to load the cleaned data.

### 2. Exploratory Data Analysis (SQL)
Key business questions were answered using SQL queries:
* **Revenue Analysis:** Compared revenue by gender (Male: $157k vs. Female: $75k).
* **Customer Segmentation:** Identified "Loyal," "New," and "Returning" customers.
* **Product Performance:** Found top products by rating (Gloves, Sandals) and category.
* **Subscription Behavior:** Analyzed spending differences between subscribers ($59.49 avg) and non-subscribers ($59.87 avg).
* **Shipping:** Compared average spend across Standard vs. Express shipping.

### 3. Dashboard & Visualization (Power BI)
An interactive dashboard was built to visualize the findings.

![Power BI Dashboard](dashboard_image.png)
*(Note: Please refer to the 'dashboard_image.png' in the repo to see the full visualization)*

**Key Dashboard Metrics:**
* **Total Customers:** 3.9K
* **Average Purchase Amount:** $59.76
* **Average Review Rating:** 3.75

## 📊 Key Insights & Business Recommendations
Based on the analysis, the following recommendations were derived:
1.  **Boost Subscriptions:** Only 27% of customers are subscribers. Exclusive benefits should be promoted to increase this base.
2.  **Loyalty Programs:** The "Loyal" segment consists of 3,116 customers. Specific rewards should be targeted here to maintain retention.
3.  **Targeted Marketing:**
    * **Demographics:** "Young Adults" generate the highest revenue ($62k), followed by Middle-aged customers.
    * **Seasonality:** Tailor campaigns based on top-performing seasonal products.
4.  **Product Positioning:** Highlight top-rated products (e.g., Gloves, Sandals) in marketing campaigns to build trust.

## 🚀 How to Run
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/kabirkohli123/Customer_Shopping_Behavior_Analysis.git](https://github.com/kabirkohli123/Customer_Shopping_Behavior_Analysis.git)
    ```
2.  **Python Setup:**
    * Install requirements: `pip install pandas sqlalchemy psycopg2`
    * Run the cleaning script to process data and upload to SQL.
3.  **SQL Analysis:**
    * Import the cleaned data into PostgreSQL.
    * Run the provided `.sql` scripts to generate insights.
4.  **Power BI:**
    * Open the `.pbix` file to view the interactive dashboard.

---
*Author: Kabir Kohli*
