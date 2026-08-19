# Sales Performance Analysis Python and PowerBI Project

![Sales Performance Analysis](Images/image%201.png)

## 📊 Project Overview

The **Sales Performance Analysis Python and PowerBI Project** is an end-to-end data analytics project focused on analyzing sales, profitability, customer segments, products, countries, discounts, and sales trends.

The project uses **Python for data cleaning, feature engineering, exploratory data analysis (EDA), and business insight generation**, followed by **Power BI for interactive visualization, KPI reporting, dashboard development, and AI-powered insights**.

The objective of this project is to transform raw sales data into meaningful business insights that can help identify high-performing products and markets, understand segment profitability, evaluate the impact of discounts, and identify areas requiring strategic improvement.

---

# 📌 Key Insights

## Key Performance Indicators

| KPI | Value |
|---|---:|
| 🧾 Total Orders | **700** |
| 💰 Total Sales | **$118.73M** |
| 📈 Total Profit | **$16.89M** |
| 📊 Profit Margin | **14.23%** |
| 📦 Units Sold | **1M** |

---

## 🔍 Business Insights

### 1.  USA Generates the Highest Sales

The **USA** is the highest-performing country in terms of total sales, making it the most significant market represented in the dashboard.

This indicates that the USA contributes a substantial portion of the company's overall revenue and should remain a key market for future growth strategies.

---

### 2.  Paseo, VTT and Velo Are the Top-Selling Products

**Paseo, VTT, and Velo** consistently rank among the top-selling products across the countries covered by the dashboard.

This is not simply an overall average — the same three products lead the product rankings across individual countries as well.

This consistency indicates strong and widespread demand for these products across different markets.

---

### 3.  Government and Small Business Lead in Sales

The **Government** and **Small Business** segments generate the highest sales.

- **Government**
  - Sales: **$52.50M**
  - Profit Margin: **21.69%**

- **Small Business**
  - Sales: **$43.43M**
  - Profit Margin: **9.77%**

---

### 4.  Enterprise Segment Is Running at a Loss

The **Enterprise** segment is operating at a loss despite carrying a significant share of sales volume.

| Period | Sales | Loss Margin | Loss |
|---|---:|---:|---:|
| Overall | $19.61M | -3.13% | $614.55K |
| 2013 | $4.05M | -4.78% | $193.76K |
| 2014 | $15.56M | -2.70% | $420.79K |

Although the loss margin improved from **-4.78% in 2013 to -2.70% in 2014**, the Enterprise segment still requires attention.

Since the segment carries a considerable sales volume, improving its cost structure could have a significant positive impact on overall profitability.

---

### 5.  Channel Partners Deliver the Highest Profit Margin

The **Channel Partners** segment delivers the highest profit margin among the segments.

- Sales: **$1.80M**
- Profit: **$1.32M**
- Profit Margin: **73.13%**

The underlying record-level data indicates that the manufacturing cost for this segment is relatively low compared with the selling price.

As a result, even with comparatively lower sales volume, Channel Partners generate exceptionally strong profitability.

---

### 6.  Discounted Products Drive the Bulk of Sales

Products sold without a discount contribute the smallest share of total sales.

| Discount Band | Share of Sales |
|---|---:|
| Medium | **32.66%** |
| High | **31.48%** |
| Low | **29.17%** |
| None | **6.69%** |

Products with **no discount** account for only **6.69%** of total sales, while the Medium, High, and Low discount bands collectively contribute the majority of revenue.

This suggests that discounting plays an important role in driving demand and converting sales.

---

# 💡 Business Recommendations

### 1.  Promote Montana and Carretera

Products such as **Montana** and **Carretera** can be promoted through targeted advertising campaigns and strategic discounts to help close the gap with the top-selling products.

### 2.  Reduce Enterprise Segment Costs

The Enterprise segment generates a major share of sales but currently operates at a loss.

Reducing manufacturing and other operational costs could significantly improve overall profitability.

### 3.  Invest in Channel Partner Marketing

Channel Partners already generate the highest profit margin.

Increasing their sales volume through targeted marketing and partner-focused strategies could provide highly efficient profit growth.

### 4.  Maintain Strategic Discounts

Undiscounted products consistently contribute the smallest share of total sales.

Maintaining at least a low level of discounting may help sustain demand and improve revenue generation.

---

# 📊 Power BI Dashboard

![Power BI Sales Dashboard](Images/image%202.png)

The Power BI dashboard provides an interactive view of the company's sales performance through KPIs, charts, slicers, and AI-generated insights.

---

# 🔄 Project Workflow

## 1.  Dataset Overview

The project starts with a sales dataset containing **700 sales records** and information related to customers, products, sales transactions, discounts, costs, profitability, and dates.

### Dataset Columns

| Column | Description |
|---|---|
| **Segment** | Customer/business segment associated with the transaction. |
| **Country** | Country where the sale occurred. |
| **Product** | Product associated with the transaction. |
| **Discount Band** | Discount category applied to the product. |
| **Units Sold** | Number of product units sold. |
| **Manufacturing Price** | Manufacturing cost per unit. |
| **Sale Price** | Selling price per unit. |
| **Gross Sales** | Sales value before discounts are applied. |
| **Discounts** | Discount amount applied to the transaction. |
| **Sales** | Final sales/revenue value after discounts. |
| **COGS** | Cost of goods sold associated with the transaction. |
| **Profit** | Profit generated from the transaction. |
| **Date** | Date on which the transaction occurred. |
| **Month Number** | Numerical representation of the transaction month. |
| **Month Name** | Name of the transaction month. |
| **Year** | Year in which the transaction occurred. |

---

#  2. Python Data Preparation

The raw `sales data.xlsx` file was loaded into a **Jupyter Notebook** for data cleaning and preprocessing.

### Data Cleaning

The following data quality issues were addressed:

- **53 missing values** in the `Discount Band` column were identified and replaced with `None`.
- The `Date` column was converted into the appropriate date/time format.
- The `Units Sold` column was converted from floating-point values to integer values.
- Incorrect/manipulated values in the `Manufacturing Price` column were corrected using the relationship between `COGS` and `Units Sold`.

The result was a cleaner and more reliable dataset suitable for further analysis.

---

#  3. Feature Engineering

Two additional analytical features were created:

### Profit Margin

A **Profit Margin** feature was created to measure profitability relative to sales.

This allows profitability to be compared across products, segments, countries, and other dimensions regardless of their sales volume.

### YearMonth

A **YearMonth** feature was created to provide a chronological month-level representation of the transaction date.

This feature was particularly useful for analyzing monthly sales and profit trends.

---

#  4. KPI Analysis

The primary business KPIs were analyzed using Python:

- **Total Orders**
- **Total Sales**
- **Total Units Sold**
- **Total Profit**
- **Profit Margin**

These KPIs provided a high-level understanding of the overall performance of the business before moving into detailed exploratory analysis.

---

#  5. Exploratory Data Analysis (EDA)

##  Total Sales and Profit by Country

Sales and profit were aggregated at the country level to identify the strongest and weakest geographical markets.

The analysis revealed that **USA generates the highest sales** among the countries represented in the dataset.

Two visualizations were created:

- Total Sales by Countries
- Total Profit by Countries

These visualizations make it easier to compare geographical performance.

---

##  Total Sales and Profit by Segment

Sales and profit were aggregated by customer segment to understand which business segments contribute the most revenue and profitability.

The analysis highlighted:

- Government as the leading sales-generating segment.
- Small Business as another major contributor to sales.
- Enterprise as a high-volume segment with negative profitability.
- Channel Partners as a segment with an exceptionally high profit margin.

Visualizations created:

- Total Sales by Segments
- Total Profit by Segments

---

##  Monthly Sales and Profit Trend

Monthly sales and profit were analyzed to understand how business performance changed over time.

A chronological `YearMonth` feature was used to ensure that the months were displayed in the correct order.

Visualizations created:

- Monthly Sales Trend
- Monthly Profit Trend

These trends help identify changes in revenue generation and profitability across different periods.

---

##  Units Sold, Sales and Profit by Product

Product-level analysis was performed by aggregating:

- Units Sold
- Sales
- Profit

This analysis helped identify the strongest products and compare their contribution to total sales and profitability.

Visualizations created:

- Total Units Sold Contribution
- Product-wise Total Sales
- Product-wise Total Profit

The analysis identified **Paseo, VTT, and Velo** as the leading products across the countries covered by the dashboard.

---

#  6. Exporting the Cleaned Dataset

After completing the data cleaning, preprocessing, feature engineering, and exploratory analysis, the cleaned dataset was exported as:

**`sales data cleaned.xlsx`**

This cleaned file was then used as the source dataset for the Power BI dashboard.

---

#  7. Power BI

The cleaned Excel dataset was imported into **Power Query** as part of the ETL process.

### Power Query

The following steps were performed:

1. Extracted the cleaned sales dataset.
2. Imported `sales data cleaned.xlsx` into Power Query.
3. Verified and corrected the required data types.
4. Loaded the prepared data into Power BI.

This ensured that the dataset used for dashboard development was properly structured and ready for analysis.

---

#  8. DAX Measures

The following DAX measures were created to calculate the primary dashboard KPIs:


Total Orders =
COUNTROWS(sales_data)

Total Sales =
SUM(sales_data[Sales])

Total Profit =
SUM(sales_data[Profit])

Total Profit Margin =
DIVIDE([Total Profit], [Total Sales])

Total Units Sold =
SUM(sales_data[Units Sold])

These measures were used throughout the Power BI dashboard to provide dynamic KPI calculations.

---

#  9. Power BI Visualizations

The dashboard contains the following major visualizations:

###  Total Sales by Country

**Chart Type:** Clustered Bar Chart

Used to compare sales performance across different countries.

###  Total Sales by Discount Band

**Chart Type:** Column Chart

Used to analyze the contribution of different discount bands to total sales.

###  Product-wise Total Sales

**Chart Type:** Clustered Column Chart

Used to compare total sales generated by individual products.

###  Total Sales Trend

**Chart Type:** Line Chart

Used to visualize the movement of sales over time.

---

#  10. Power BI KPIs

The dashboard contains five primary KPI cards:

* **Total Orders:** 700
* **Total Sales:** $118.73M
* **Total Profit:** $16.89M
* **Total Profit Margin:** 14.23%
* **Total Units Sold:** 1M

These KPIs provide an immediate overview of overall business performance.

---

#  11. Interactive Slicers

Two slicers were added to make the dashboard interactive:

### Segment Slicer

Allows users to filter the dashboard based on customer segment.

### Year Slicer

Allows users to analyze sales performance across different years.

The slicers dynamically update the dashboard visuals and KPIs based on the selected filters.

---

#  12. AI Insights

A special feature of the dashboard is the use of **Power BI's Narrative / AI Insights functionality**.

The AI-powered narrative provides automatically generated explanations of important trends and changes within the report, helping users understand the dashboard without manually interpreting every visualization.

This adds an additional analytical layer to the dashboard beyond traditional charts and KPIs.

---

# 🛠️ Tools & Technologies

| Tool / Technology        | Purpose                                                   |
| ------------------------ | --------------------------------------------------------- |
| **Python**               | Data cleaning, preprocessing, feature engineering and EDA |
| **Jupyter Notebook**     | Python-based analysis environment                         |
| **Pandas**               | Data manipulation and analysis                            |
| **Matplotlib**           | Data visualization                                        |
| **Seaborn**              | Statistical and exploratory visualizations                |
| **Microsoft Excel**      | Raw and cleaned dataset storage                           |
| **Power Query**          | ETL and data transformation                               |
| **Power BI**             | Interactive dashboard and reporting                       |
| **DAX**                  | KPI and analytical measure creation                       |
| **Power BI AI Insights** | Automated narrative and insights                          |


---

# 📂 Project Structure

```text
Sales-Performance-Analysis-Python-and-PowerBI-Project/
│
├── Images/
│   ├── multiple images of the dashboard
│  
│
├── Datasets/
│   ├── sales data.xlsx
│   └── sales data cleaned.xlsx
│
├── Jupyter Notebook/
│   └── Sales Performance Analysis.ipynb
│
├── PowerBI File/
│   └── sales performance analysis dashboard.pbix
│
├── Project Report/
│   ├── Sales_Performance_Analysis_Report_ppt.pdf
│   └── Sales_Performance_Analysis_Report_ppt.pptx
│
└── README.md
```

---

# 🔁 End-to-End Workflow

```text
Raw Sales Data
      │
      ▼
sales data.xlsx
      │
      ▼
Python / Jupyter Notebook
      │
      ├── Data Cleaning
      ├── Missing Value Handling
      ├── Data Type Correction
      ├── Data Validation
      ├── Feature Engineering
      └── Exploratory Data Analysis
      │
      ▼
sales data cleaned.xlsx
      │
      ▼
Power Query
      │
      ├── ETL
      ├── Data Type Validation
      └── Data Loading
      │
      ▼
Power BI
      │
      ├── DAX Measures
      ├── KPI Cards
      ├── Charts
      ├── Slicers
      └── AI Narrative
      │
      ▼
Interactive Sales Performance Dashboard
      │
      ▼
Business Insights & Recommendations
```

---

# 🎯 Project Objectives

The primary objectives of this project were to:

* Clean and prepare raw sales data for analysis.
* Perform exploratory data analysis using Python.
* Identify high-performing countries and products.
* Analyze sales and profitability across customer segments.
* Understand the relationship between discounts and sales.
* Analyze monthly sales and profit trends.
* Build meaningful business KPIs.
* Develop an interactive Power BI dashboard.
* Implement DAX measures for dynamic analysis.
* Add interactive filtering using slicers.
* Utilize Power BI's AI Narrative functionality.
* Generate actionable business recommendations from the analysis.

---

# 📌 Conclusion

This project demonstrates a complete **end-to-end data analytics workflow**, starting from raw Excel data and progressing through Python-based data preparation and exploratory analysis to an interactive Power BI business intelligence dashboard.

The analysis highlights the strongest markets, products, segments, discount strategies, and profitability challenges. In particular, the **USA market, Paseo/VTT/Velo products, Government segment, and Channel Partners** emerge as important areas of opportunity, while the **Enterprise segment** requires significant cost and profitability improvement.

By combining **Python's analytical capabilities with Power BI's visualization, DAX, interactive filtering, and AI-powered insights**, the project transforms raw transactional data into a practical business decision-support solution.
