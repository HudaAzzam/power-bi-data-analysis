# power-bi-data-analysis
this is a collection of microsoft power bi dashboards I cearaed during Egypt digital bioneers scholarship (DEPI) round 2 

# Disclaimer:
The information provided in these dashboards are not factual and is for illustrative purposes only.

1. Power BI pharmacy Sales Dashboard
Overview
This Power BI dashboard provides an interactive visualization of sales data, leveraging advanced DAX calculations, bookmarks, tooltips, and drill-through functionalities. It allows users to analyze sales performance per item, region, and category with deep insights.

Features
✅ DAX Measures – Advanced calculations including TotalAmountPerItem, dynamic filtering, and aggregations
✅ Bookmarks & Navigation – Custom bookmarks for seamless navigation
✅ Tooltips & Drill-Through – Contextual insights using tooltips and drill-through pages
✅ Filters & Slicers – User-friendly filters for granular analysis
✅ Data Cleaning & Transformation – Handling missing, duplicate, and inconsistent records


Key DAX Measures
Total Sales Amount Per Item
DAX
نسخ
تحرير
TotalAmountPerItem = 
VAR ItemCode = 'sales-jan'[item code]
VAR ItemDescription = 'sales-jan'[item description]

RETURN
CALCULATE(
    SUM('sales-jan'[amount]),
    FILTER(
        'sales-jan',
        'sales-jan'[item code] = ItemCode &&
        'sales-jan'[item description] = ItemDescription
    )
)

🚀 Usage
Load the PBIX File: Open new_sales_2.pbix in Power BI
Data Connection: Ensure that sales.data.xlsx is properly linked
Interact with Dashboard:
Use slicers for filtering by Date, Item, Region
Hover over tooltips for detailed insights
Click on drill-through pages for deeper analysis

