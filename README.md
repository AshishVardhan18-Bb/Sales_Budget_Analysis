# Sales and Budget Analysis

### Dashboard Link : https://app.powerbi.com/view?r=eyJrIjoiOTg3MjlhZDctMDNiOC00NDdjLWJjNDQtMzZmZTYzNjUyZTYxIiwidCI6IjM0ODNhYmVlLWI2MmMtNDcwYS04MTQ2LTczYTAzOTk3NzZiYyJ9 

## Problem Statement

Steven  - Sales Manager:
Hi Ashish
I hope you are doing well. We need to improve our internet sales reports and want to move from static reports to visual dashboards.
Essentially, we want to focus it on how much we have sold of what products, to which clients and how it has been over time.
Seeing as each sales person works on different products and customers it would be beneficial to be able to filter them also.
We measure our numbers against budget so I added that in a spreadsheet so we can compare our values against performance. 
The budget is for 2021 and we usually look 2 years back in time when we do analysis of sales.
Let me know if you need anything else!

// Steven



### Steps followed 

- Step 1 : Load data into Power BI Desktop, dataset is a csv file.
- Step 2 : So, let us create measures firstly create a measure for the sales_amount also called as the revenue. 
  Sales = SUM(FACT_InternetSales[SalesAmount])
- Step 3 : Create one more measure called as Budget for tha Budget_Amount called as Budget_Amount. Budget_Amount = SUm(Budget[Budget])
- Step 4 : Create one more measure as Sales-Budget which shows the difference between actual sales and budgeted sales. A positive result means sales exceeded expectations, while a negative result indicates underperformance as Sales-Budget = [Sales]-[Budget_Amount]
- Step 5 :Create one more measure as Sales/budget which gives the ratio of actual sales to budgeted sales. A result above 1 means sales exceeded the budget, while below 1 indicates sales fell short. Sales/Budget = DIVIDE([Sales],[Budget_Amount],0)
- Step 6 :Create one more measure Total Purchase Value = SUM(FACT_InternetSales[SalesAmount])  which gives us the total purchase value 
- Step 7 :Create one more measure Number of Purchases = COUNTROWS(SUMMARIZE(FACT_InternetSales, FACT_InternetSales[SalesOrderNumber], FACT_InternetSales[CustomerKey])) which shows total number of unique purchases by counting distinct sales order numbers for each customer in the FACT_InternetSales table. It provides the count of individual transactions or orders made by customers.
- Step 8 : Visual filters (Slicers) were added for four fields named "Product color", "Customer City","Sub Category","Category","Product Name" & "Date".
- Step 9 : A dynamic card visual which displays the change in budget or amount by comparing sales with the budget. It indicates whether the value has increased or decreased, based on the provided sales and budget figures
- Step 10 : Using a gauge visual with sales as the actual value and budget as the target shows how close the actual sales are to the budgeted amount. The gauge helps visualize performance at a glance, indicating whether sales are below, meeting, or exceeding the budget target, with a clear visual representation of progress toward the goal.
- Step 11 : A clustered column chart and a Line Chart is used with months, sales, and budget displays sales and budget amounts side by side for each month. This visual makes it easy to compare actual sales to the budget for each time period, helping identify patterns, overperformance, or underperformance throughout the months

- Step 12 : Using two bar charts—one displaying sales by product name and the other by salesperson—allows for a clear comparison of sales performance. The first chart highlights which products are driving sales, while the second shows the contribution of each salesperson, making it easy to analyze both product and individual performance side by side.
- Step 13 : Two matrices displaying sales by product name and by salesperson, with months included, provide detailed insights into both product and individual sales performance over time. The product matrix shows how each product performs across different months, while the salesperson matrix reveals monthly sales contributions by each person, helping track trends and performance across both dimensions.
- step 14 : A Map Visual has been used to display the location of customers and also to display the areas which are showing maximum sales 
- step 15 :A scatter plot for cross-selling prediction uses customer name, number of purchases, and total purchase value to visualize relationships between these variables. Each point represents a customer, with the number of purchases plotted on one axis and total purchase value on the other. This visualization helps identify patterns, such as clusters of high-value customers or potential cross-selling opportunities, enabling targeted marketing strategies based on customer behavior
- Step 14 : Calculated column was created in which, customers were grouped into various age groups.


# Snapshot of Dashboard (Power BI Service)


 
![Dashboard_upload](https://github.com/user-attachments/assets/4ee0680b-5c0c-449b-90ae-d47bcb09d024)

# Insights

A single page report was created on Power BI Desktop & it was then published to Power BI Service.

Following inferences can be drawn from the dashboard;

### [1] Total Number of Customers = 18400

   Number of Customers (Male) = 9331 (50.71 %)

   Number of Customers (Female) = 9097 (49.44 %)

   So,there is equal contribution of men and women in the sales 


           
### [2] Sales and Budget Monthly Analysis

   1)	January – Sales = 13,98,748
                  Budget = 16,00,000
We can see that the sales has underperformed according to the Budget given 
2)	February – Sales = 12,75,488
                  Budget = 16,00,000
We can see that the sales has underperformed according to the Budget given 
3)	March – Sales = 14,23,390
                Budget = 20,00,000
We can see that the sales has underperformed according to the Budget given 
4)	April – Sales = 14,46,358
                Budget = 20,00,000
We can see that the sales has underperformed according to the Budget given 
5)	May – Sales = 16,43,470
                 Budget = 22,00,000
We can see that the sales has underperformed according to the Budget given 
6)	June – Sales = 21,98,337
                 Budget = 22,00,00
We can see that the sales has underperformed according to the Budget given 
7)	July – Sales = 18,16,234
                 Budget = 15,00,000
We can see that the sales has overperformed according to the Budget given 
8)	August – Sales = 20,74,982
                 Budget = 15,00,000
We can see that the sales has overperformed according to the Budget given 
9)	September – Sales = 19,33,673
                  Budget = 15,00,000
We can see that the sales has overperformed according to the Budget given 
10)	October – Sales = 22,08,452
                  Budget = 15,00,000
We can see that the sales has overperformed according to the Budget given 
11)	November – Sales = 23,18,875
Budget = 15,00,000
We can see that the sales has overperformed according to the Budget given
12)	 December – Sales = 24,98,862
     Budget = 20,00,000
We can see that the sales has overperformed according to the Budget given


  
  ### [3] Sales By Category
  
  a) Bikes = 2,11,99,197 (95.32%)
  b) Clothng = 3,39,772 (1.53%)
  c) Accesories = 7,00,759 (3.15%)


 ### [4] Top 5 Customers with Highest Sales
  a) jOrdan Turner - 15,999
  b) Maurice shann - 12,909
  c) Janet Munoz - 12,489
  d) Lisa Cai - 11,469
  e) Lacey Zheng - 11,248
 
