### Capstone Project Report: Tailwind Traders Data Analysis

---

#### **Overview**

In the Capstone project for Tailwind Traders, the focus was on preparing, configuring, and analyzing sales data to derive meaningful insights. The project involved detailed steps in data handling, relationship configuration, and report creation using Power BI. This report encapsulates the significant numbers and key findings from the project, illustrating the process and outcomes in a comprehensive manner.

---

### **1. Data Preparation**

**a. Sales Data Preparation**

- **Gross Revenue Calculation:**
  The Gross Revenue was computed for each product by multiplying the unit price by the quantity sold. The calculations yielded a maximum gross revenue of **360** and a minimum of **18**. These values reflect the variability in revenue across different products and sales transactions, offering a snapshot of the highest and lowest revenue contributions in the dataset.

- **Total Tax Calculation:**
  The Total Tax was determined by applying the tax rate to the quantity sold. The highest tax recorded was **25.2**, while the lowest was **5.25**. This range demonstrates the extent of tax applied based on product pricing and quantities, highlighting the tax burden across different sales.

- **Net Revenue Calculation:**
  Net Revenue, which accounts for post-tax earnings, ranged from a high of **334.8** to a low of **9.6**. These figures underscore the financial impact of tax on the final revenue figures, with the highest net revenue indicating significant profitability and the lowest reflecting more constrained earnings.

**b. Configuring Data Sources**

- **Loading and Transforming Sales Data:**
  Sales data was imported into Power BI, where column data types were adjusted for accuracy. For instance, `OrderID` was set as a Whole Number, and `Gross Product Price` was assigned as a Fixed Decimal Number. These transformations were crucial for ensuring data integrity and consistency in subsequent analyses.

- **Purchases and Countries Data:**
  The Purchases and Countries datasets were similarly loaded and transformed. The data types were meticulously set to match the specific needs of the analysis, ensuring that columns such as `Purchase Date` and `Country ID` were appropriately formatted.

- **Historical Currency Exchange Data:**
  Historical currency exchange rates were sourced using Python scripts, capturing exchange data for currencies like USD, GBP, and EUR. This information was vital for accurate conversion and comparison of sales data across different currencies.

---

### **2. Data Model Design and Development**

**a. Table Configuration**

- **Purchases Table:**
  The Purchases Table was structured with key columns like `PurchaseID`, `OrderID`, and `Purchase Date`. Each column was assigned the correct data type to ensure proper functionality and accuracy in analysis.

- **Sales Table:**
  In the Sales Table, columns such as `Gross Product Price` and `Tax Per Product` were designated as Fixed Decimal Numbers. This precision was necessary for accurate financial calculations and reporting.

- **Countries Table:**
  The Countries Table included columns like `Country ID` and `Exchange ID`, with each column properly typed to align with its role in the data model.

- **Exchange Data Table:**
  Created with a Python script, this table featured `Exchange Currency` and `Exchange ID` columns, which were essential for currency conversion and exchange rate analysis.

**b. Relationship Setup**

- **Countries and Exchange Data:**
  A one-to-one relationship was established between the Countries and Exchange Data tables via `Exchange ID`. This setup, with bi-directional cross-filtering, enabled precise mapping of currency exchanges to country-specific data.

- **Sales and Countries:**
  A many-to-one relationship was created between Sales and Countries tables on `Country ID`. This relationship allowed for detailed analysis of sales performance across different countries.

- **Purchases and Sales:**
  A one-to-one relationship linked Purchases and Sales tables through `OrderID`. This linkage was crucial for integrating purchase and sales data.

- **Calendar Table:**
  A Calendar Table was introduced using DAX, providing a temporal dimension for analyzing sales data over time.

- **Sales in USD Table:**
  This calculated table converted all sales figures to USD, facilitating consistent comparison and analysis across different currencies.

- **Relationships Validation:**
  Relationships between the Sales in USD table and Sales table were validated, ensuring accurate comparison between original and USD-adjusted sales data.

---

### **3. Aggregations and Reporting**

**a. Configuring Aggregations Using DAX**

- **Yearly Profit Margin:**
  The Yearly Profit Margin highlighted significant profitability, with the highest margins reflecting robust financial health. The calculated margin provided insights into the efficiency of revenue generation relative to net revenue.

- **Quarterly Profit:**
  Quarterly profit metrics revealed seasonal trends and performance variations, assisting in understanding the business cycles and sales fluctuations throughout the year.

- **Year-to-Date Profit:**
  The Year-to-Date profit metric showed cumulative profit accumulation from the start of the year, providing a snapshot of ongoing performance and profitability.

- **Median Sales:**
  Median Sales figures offered insights into the central tendency of sales data, helping to understand typical sales values and distribution patterns.

- **Performance Analyzer:**
  The Performance Analyzer was used to monitor the efficiency of DAX queries, ensuring that visualizations and calculations performed optimally with query times under 200ms.

**b. Creating Sales and Profit Reports**

- **Sales Overview Report:**
  - **Bar Chart for Loyalty Points by Country:** A clustered bar chart visualized loyalty points distribution by country, with the UK showing the highest points.
  - **Column Chart for Quantity Sold by Product:** A clustered column chart illustrated the quantity sold for each product, highlighting top-selling items.
  - **Pie Chart for Median Sales Distribution by Country:** This pie chart depicted the distribution of median sales across countries, providing a clear view of sales concentration.
  - **Line Chart for Median Sales Over Time:** The line chart, including a forecast, tracked median sales trends over time, offering predictive insights into future sales patterns.
  - **Cards for Measures:** Cards visualized key measures such as Stock, Quantity Purchased, and Median Sales, enhancing the clarity of performance metrics.

- **Profit Overview Report:**
  - **Bar Chart for Net Revenue by Product:** This chart displayed net revenue by product, identifying the Modular Sofa Set as the top revenue generator.
  - **Donut Chart for Yearly Profit Margin by Country:** The donut chart highlighted the yearly profit margin by country, providing a detailed view of profitability across regions.
  - **Area Chart for Yearly Profit Margin Over Time:** The area chart illustrated profit margin trends over time, showing fluctuations and trends in profitability.
  - **Cards for Measures:** Cards were used to show YTD Profit and Net Revenue USD, focusing on key financial metrics.
  - **KPI for Gross Revenue USD:** A KPI displayed Gross Revenue USD, with trend analysis over time providing insights into revenue performance.

---

### **Conclusion**

The Capstone project for Tailwind Traders successfully involved detailed data preparation, configuration, and modeling to deliver insightful reports and analyses using Power BI. Through meticulous setup of data relationships, DAX calculations, and effective report creation, the project provided valuable insights into sales performance, profitability, and operational efficiency, guiding strategic decision-making processes.

This report captures the essential findings and methodologies employed in the project, reflecting the depth of analysis and the resulting actionable insights.




