This project is an interactive Financial Analysis Dashboard built in Power BI using a sample financial dataset.

The dashboard provides insights into:

-Sales Performance  
-Order Volume  
-Profitability       
-Profit Margin   
-Discount Analysis  
-Product Performance   
-Segment Analysis  
-Country-wise Performance  
-Time-based Trends  

The objective was to transform raw financial data into meaningful business insights using data modeling, DAX measures, and interactive visualizations.

![Dashboard Preview](https://github.com/Sundhar-CMA/PowerBI-Financial-Analysis-Dashboard/blob/20e5bbe9932909ab8f01451377ae8008d3edc50d/Dash%20board%20Preview%201.png)

Key Performance Indicators (KPIs)
The dashboard tracks:
Total Sales,Total Orders,Total Profit,Profit Margin %,Total Discounts
Each KPI includes a comparison against the previous year.

Business Questions Answered

-Sales Performance  
-What are total sales?  
-How do sales compare to last year?  
-Which countries generate the highest sales?  
-Profitability Analysis  
-What is the current profit margin?  
-Which country has the highest profit margin?  
-Which customer segment is most profitable?  
-Discount Analysis  
-How much discount is being offered?  
-Which discount band contributes the most?  
-Product Analysis  
-Which products generate the highest sales?  
-Top 3 products by sales amount  
-Trend Analysis  
-Monthly sales trend  
-Year-over-year performance comparison  
-Data Model 
-Fact Table 

Financials  Contains:

-Sales Amount  
-Profit  
-Discounts  
-Product  
-Segment  
-Country  
-Date  
-This acts as the central fact table.

Dimension Table : Date Table   

Custom date table created using DAX, Includes:   
-Date  
-Month Number  
-Month Name  
-Year  
Purpose:
-Time Intelligence calculations  
-Year-over-Year comparisons  
-Trend analysis

![Dashboard Preview](https://github.com/Sundhar-CMA/PowerBI-Financial-Analysis-Dashboard/blob/20e5bbe9932909ab8f01451377ae8008d3edc50d/Dashboard%20preview%203.png)


Measures Table : Analysis  
Created to store all DAX measures separately.

Benefits:

-Cleaner model    
-Better organization  
-Easier maintenance  
-DAX Measures Used  
-Basic Aggregations  
-Orders = SUM(...)  
-Sales Amount = SUM(...)  
-Profit = SUM(...)  
-Discount Offered = SUM(...)  
Purpose:
-Aggregate business metrics from transactional data.

![Dashboard Preview](https://github.com/Sundhar-CMA/PowerBI-Financial-Analysis-Dashboard/blob/20e5bbe9932909ab8f01451377ae8008d3edc50d/Dashboard%20preview%202.png)


Previous Year Calculations    
-Order LY = CALCULATE([Orders],DATEADD('Date Table'[Date],-1,YEAR))   
Similar logic used for:   
-Sales Amount LY  
-Profit LY  
-Discount Offered LY  
-Profit Margin LY  
Purpose:
-Compare current performance against previous year.

Profit Margin  
-Profit Margin = DIVIDE([Profit],[Sales Amount])  
Purpose:
-Measure profitability efficiency.

Top 3 Products  
-Top 3 Products by Sales =CALCULATE([Sales Amount],TOPN(3,
ALLSELECTED(Financials[Product]),[Sales Amount],DESC))    
Purpose:
-Identify highest revenue-generating products.

Highlight Measure
-Top Highlight =IF(ISBLANK([Top 3 Products by Sales]),0,1)
Purpose:
-Used for conditional formatting and highlighting top products.

Power BI Features Used  
-Data Modeling  
-Star-schema approach  
-Fact and Dimension separation  
-One-to-many relationship  
-DAX Functions  
-SUM  
-CALCULATE 
-DATEADD  
-TOPN  
-ALLSELECTED  
-IF  
-ISBLANK  
-Visualizations  
-KPI Cards  
-Bar Charts  
-Column Charts  
-Donut Chart  
-Line Chart  
-Matrix Table  
-Conditional Formatting  

Used to highlight important metrics and improve dashboard readability.

Skills Demonstrated  
-Financial Analysis  
-KPI Design  
-Data Modeling  
-DAX Development  
-Time Intelligence  
-Dashboard Design  
-Business Performance Analysis  
-Data Visualization  
