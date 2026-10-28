# Big Data Retail Analytics

## Project Overview

This project analyzes retail transaction data to identify sales trends, top-performing products, revenue by country, and customer purchasing behavior. The analysis was performed using Python in Google Colab.

The project demonstrates data cleaning, exploratory data analysis, data aggregation, visualization, and rule-based customer segmentation using a real-world retail dataset.

## Objectives

- Analyze retail revenue across different countries.
- Identify products generating the highest revenue.
- Examine monthly revenue trends.
- Segment customers based on spending, purchase frequency, and recency.
- Generate visualizations and export analysis results for further exploration.

## Technologies Used

- **Python** — data analysis and processing
- **Pandas** — data cleaning, aggregation, and manipulation
- **Matplotlib** — data visualization
- **Google Colab** — cloud-based notebook environment
- **GitHub** — project version control and portfolio presentation

## Dataset

The project uses the **Online Retail** dataset from the UCI Machine Learning Repository.

The dataset contains approximately 542,000 transaction records with information such as invoice numbers, product descriptions, quantities, unit prices, invoice dates, customer IDs, and countries.

Dataset source: [UCI Machine Learning Repository — Online Retail](https://archive.ics.uci.edu/dataset/352/online+retail)

## Project Workflow

### 1. Data Loading
Loaded the retail transaction dataset into a Pandas DataFrame.

### 2. Data Cleaning
- Checked missing values and duplicate records.
- Removed duplicate rows.
- Removed records missing essential fields.
- Excluded non-positive quantities and unit prices for the sales analysis.
- Created a revenue column using quantity multiplied by unit price.

### 3. Revenue Analysis
Analyzed revenue by country and product to identify the highest-performing markets and products.

### 4. Monthly Sales Analysis
Aggregated revenue by month and plotted the trend over the period covered by the dataset.

### 5. Customer Segmentation
Calculated customer-level spending, number of distinct invoices, and days since the last recorded purchase. Applied illustrative rules to categorize customers as High Value, At Risk, Dormant, or Other Active.

These segments are exploratory labels based on the chosen thresholds, not official labels supplied by the dataset.

### 6. Results Export
Exported analysis tables as CSV files and charts as PNG images for documentation and further analysis.

## Repository Contents

```text
big-data-retail-analytics/
├── Big_Data_Retail_Analytics.ipynb
├── results/
│   ├── revenue_by_country.csv
│   ├── revenue_by_product.csv
│   ├── monthly_revenue.csv
│   ├── customer_segments.csv
│   ├── revenue_by_country.png
│   ├── revenue_by_product.png
│   ├── monthly_revenue_trend.png
│   └── customer_segmentation.png
└── README.md
```

*The `results/` folder should contain the exported files after you upload and organize them in GitHub.*

## How to Run

1. Open the notebook `Big_Data_Retail_Analytics.ipynb` in GitHub.
2. Click **Open in Colab** if the option is available, or download the notebook and upload it to [Google Colab](https://colab.research.google.com/).
3. Run the notebook cells in order.
4. If necessary, install `openpyxl` in a notebook cell using `%pip install openpyxl`.
5. Review the tables, visualizations, and exported results.

An internet connection is required to download the original dataset.

## Key Deliverables

- Revenue analysis by country
- Revenue analysis by product
- Monthly revenue trend
- Customer segmentation table and visualization
- Exported CSV tables and PNG charts
- Reproducible Google Colab notebook

## Current Scope and Limitations

This repository currently documents a Python-based retail analytics workflow. Although the project is motivated by big-data analytics, **Hadoop HDFS and Apache Hive have not yet been implemented or validated as part of this workflow**.

The customer segmentation uses manually defined thresholds and is not a trained machine-learning classification model. The results reflect historical data in the dataset and should not be interpreted as current retail performance.

## Future Improvements

- Integrate Apache Hadoop HDFS for distributed data storage.
- Use Apache Hive for SQL-based querying and aggregation.
- Compare results from Hive queries with Python-based analysis.
- Explore scalable processing with Apache Spark.
- Develop a dashboard for interactive retail analytics.
