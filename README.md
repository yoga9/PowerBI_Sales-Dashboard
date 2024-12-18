# SuperStore Sales Dataset 2019-2022: Data Analysis PowerBI Report

#### Introduction
The SuperStore dataset comprises a comprehensive sales record from a superstore, containing 9,994 entries across 19 distinct fields. The dataset includes order details, anonymized customer information, product specifics, and financial metrics. This report analyzes various aspects of the dataset to extract meaningful insights.

#### Data Overview
The dataset includes the following columns:

- **Order Details**: `order_id`, `order_date`, `ship_date`
- **Customer Information**: `customer`
- **Product Details**: `manufactory`, `product_name`
- **Segmentation**: `segment`, `category`, `subcategory`
- **Geographical Information**: `region`, `zip`, `city`, `state`, `country`
- **Financial Metrics**: `discount`, `profit`, `quantity`, `sales`, `profit_margin`

**The Objective of the Sales Dashboard / Business Problem:**

The objective of the report is to analyze and present comprehensive insights into sales, profit, orders, profit margin, and various comparisons. It aims to provide a clear understanding of key performance indicators and trends using Power BI. The report objectives can be summarized as follows:

**Steps to follow for an end-to-end Power BI Project:**

1) Gather Data - Load data into Power BI Desktop, dataset is a Excel file.

2) Power Query – Data Extract, Transform & Load
Power Query Editor in Power BI is a powerful tool for data cleaning and transformation. Used it to clean and transform the data to make it suitable for analysis. This may involve removing duplicates, handling missing values, merging datasets, or creating calculated columns.

here, For Imported Dataset - Changes the required transformation such as duplicate check, format the data types of the required fields.

3) Create a Date Table - To work with Data Analysis Expressions (DAX) time intelligence functions, there’s a prerequisite model requirement:
Code for Creating Date Table in Power BI:

```
DAX DateTable = 
ADDCOLUMNS (
    CALENDAR(DATE(2019,1,1), DATE(2022,12,31)),
    // CALENDARAUTO(),
    "Year", YEAR([Date]),
    "Quarter", "Q" & FORMAT(CEILING(MONTH([Date])/3, 1), "#"),
    "Quarter No", CEILING(MONTH([Date])/3, 1),
    "Month No", MONTH([Date]),
    "Month Name", FORMAT([Date], "MMMM"),
    "Month Short Name", FORMAT([Date], "MMM"),
    "Month Short Name Plus Year", FORMAT([Date], "MMM,yy"),
    "DateSort", FORMAT([Date], "yyyyMMdd"),
    "Day Name", FORMAT([Date], "dddd"),
    "Details", FORMAT([Date], "dd-MMM-yyyy"),
    "Day Number", DAY ( [Date] )
)
```

4) Create Data Model in Power BI Desktop - Design and create a data model that represents the relationships between Main table and Date Table. This step is crucial for accurate analysis and visualization.

5) Develop Reports in Power BI Desktop - Use the Power BI Desktop application to create reports based on the data model. Add visualizations such as KPI cards, map, charts, tables to represent the data effectively. Apply filters, slicers, and drill-through functionalities to allow users to interact with the data.


### Snapshot of Superstore Dashboard Page (PowerBI Desktop)

The dashboard typically includes various visual elements like charts, graphs, and maps to represent data insights. The dynamic feature represent sales,profit,orders insights:

Sales Overview: A summary of total sales, profit, and orders with % increase/decrease compared with Previous year.

Geographical Distribution: Maps showing sales distribution across different states.

Segment Analysis: Bar charts displaying by different segments like Consumer, Corporate, and Home Office data with custom data lables in dynamic.

Top 10 Manufacturers and Customers: Highlighting the top manufacturers and customers by sales or profit or orders data with custom data lables in dynamic.

Category and Sub-Category Performance: Charts showing sales, profit and orders by different product categories and sub-categories data with custom data lables in dynamic.

These visuals elements help in quickly understanding the key metrics and trends.

### Superstore Sales Insights
Defaultly Sales Insights shown while open the report with repect to the selected date range, likewise able to view Profit and Order metics based on the dynamic parameter selection.

![image](https://github.com/user-attachments/assets/00d88939-0373-4346-b1f9-3b4732706219)

### Snapshot of Order Detail Page
With the help of the Custom Slicer Panel, Filter and Bookmark functionality in Power BI to view the Detailed page. It’s a fantastic approach to obtain a more detailed look at the entity data in granular level.

![image](https://github.com/user-attachments/assets/1615bc90-c5d6-413f-81f4-cd500d1872d5)

**Conclusion of Power BI Superstore Sales Dashboard Project:**

**Conclusion for the year 2022: Sales Insights**

Here are the key insights summarized for each Insights:

1) Total Sales: $733K, a 20.4% increase from the previous year.

2) Total Profit: $93.4K, a 14.2% increase from the previous year.

3) Total Orders: 1,687, a 28.3% increase from the previous year.

1.1) Sales by State: Visual representation shows sales distribution across different states in which California leads with $146.4K.

1.2) Sales by Segment: Consumer segment leads with $331.9K, a 11.8% increase.

1.3) Sales by Top 10 Manufacturers: "Other" category tops with $96.5K in sales.

1.4) Sales by Category: Technology category leads with $271.7K, a 20.0% increase.

1.5) Sales by Sub-Category: Phones sub-category leads with $105.3K, a 33.4% increase.

1.6) Sales by Top 10 Customers: Raymond Buch is the top customer with $14.2K in sales.

**Conclusion for the year 2022: Profit Insights**

Here are the key insights summarized for each Insights:

2.1) Profit by State: The highest profit by state is concentrated in the eastern and central United States, in which California leads with $29.4K.

2.2) Profit by Segment:  The Consumer segment generated the highest profit at $45.6K, with a 27.5% increase.

2.3) Profit by Category: Technology category generated the highest profit at $50.7K, with a 27.5% increase.

2.4) Profit by Sub-Category: The highest profit by sub-category is from Copiers at $25.0K, with a 41.1% increase.

2.5) Profit by Top 10 Manufacturers: Canon is the top manufacturer by profit, generating $20.3K.

2.6) Profit by Top 10 Customers: Raymond Buch is the top customer by profit, generating $6.8K.

**Conclusion for the year 2022: Orders Insights**

Here are the key insights summarized for each Insights:

3.1) Orders by State: Visual representation shows orders distribution across different states, in which California leads with 344 orders.

3.2) Orders by Segment: Consumer segment leads with 876 orders, a 34.6% increase.

3.3) Orders by Top 10 Manufacturers: "Other" category tops with 556 orders.

3.4) Orders by Category: Office Supplies lead with 1,272 orders, a 34.5% increase.

3.5) Orders by Sub-Category: Binders have the highest orders at 432, a 22.4% increase.

3.6) Orders by Top 10 Customers: Emily Phan is the top customer with 8 orders.

#### Conclusion
The SuperStore dataset provides valuable insights into sales performance, profitability, orders, and customer purchasing behavior. These insights can guide strategic decisions in inventory management, marketing, and sales optimization to enhance overall business performance. Overall, The Sales dashboard effectively presents key metrics and insights through a combination of KPI, charts, graphs, and maps for tracking and analyzing sales performance.

Dataset Link: https://www.kaggle.com/datasets/timchant/supstore-dataset-2019-2022/data
