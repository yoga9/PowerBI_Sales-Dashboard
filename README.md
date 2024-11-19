
# Sales Dashboard

**The Objective of the Sales Dashboard / Business Problem:**

The objective of the report is to analyze and present comprehensive insights into sales, profit, orders, profit margin, and various comparisons. It aims to provide a clear understanding of key performance indicators and trends using Power BI. The report objectives can be summarized as follows:

**Steps to follow for an end-to-end Power BI Project:**

1) Gather Data - Load data into Power BI Desktop, dataset is a Excel file.

2) Power Query – Data Extract, Transform & Load
Power Query Editor in Power BI is a powerful tool for data cleaning and transformation. Used it to Clean and transform the data to make it suitable for analysis. This may involve removing duplicates, handling missing values, merging datasets, or creating calculated columns.

3) Create a Date Table - To work with Data Analysis Expressions (DAX) time intelligence functions, there’s a prerequisite model requirement:
Code for Creating Date Table in Power BI:

```
DAX DateTable = 
ADDCOLUMNS (
    //CALENDAR(DATE(2020,1,1), DATE(2024,12,31)),
    CALENDARAUTO(),
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

4) Create Data Model in Power BI Desktop - Design and create a data model that represents the relationships between different tables in data. This step is crucial for accurate analysis and visualization.

5) Develop Reports in Power BI Desktop - Use the Power BI Desktop application to create reports based on the data model. Add visualizations such as charts, tables to represent the data effectively. Apply filters, slicers, and drill-through functionalities to allow users to interact with the data.


### Snapshot of Overwiew DashboardPage (PowerBI Desktop)

![Overview Page](https://github.com/user-attachments/assets/eb62792b-9dcb-439b-99df-0a14cc383d6c)


### Snapshot of Order Detail Page - Hide
With the help of the Filter functionality in Power BI to view the Detailed page. It’s a fantastic approach to obtain a more detailed look at the entity data you choose for your Drill through the filter.

![Order Details Page](https://github.com/user-attachments/assets/082022e4-210c-4606-95d1-a337fa36288b)



**Conclusion of Power BI Superstore Sales Dashboard Project:**

Conclusion for the year 2022: Sales Insights

Here are the key insights summarized for each Insights:

1) Total Sales: $733K, a 20.4% increase from the previous year.

2) Total Profit: $93.4K, a 14.2% increase from the previous year.

3) Total Orders: 1,687, a 28.3% increase from the previous year.

1.1) Sales by State: Visual representation shows sales distribution across different states.

1.2) Sales by Segment: Consumer segment leads with $331.9K, a 21.1% increase.

1.3) Sales by Top 10 Manufacturers: "Other" category tops with $96.5K in sales.

1.4) Sales by Category: Technology category leads with $271.7K, a 20.0% increase.

1.5) Sales by Sub-Category: Phones sub-category leads with $105.3K, a 33.4% increase.

1.6) Sales by Top 10 Customers: Raymond Buch is the top customer with $14.2K in sales.

