# LITA_CAPSTONE_CUSTOMERDATA

## Project Title-Customer Segmentation for a Subscription Service

### Table Content

[Project Title](#project-title)

[Project Overview](#project-overview)

[Data Sources](#data-sources)

[Tools Used](#Tools-Used)

[Data Cleaning and Preparation](#Data-Cleaning-and-Preparation)

[Exploratory Data Analysis](#Exploratory-Data-Analysis)

[Data Analysis](#Data-Analysis)

[Data Visualization](#Data-Visualization)

[Recommendation](#Recommendation)

### Project Overview
  In this project, the task is to analyse customer data for a subscription service to identify segments and trends. To explore the dataset and understand customer behaviour, track subscription types and identify key trends in cancellations and renewals.

### Data Sources
  The primary source of data is Customerdata. xlsx. This is a data given as capstone project in partial fulfillment of A 3-month Data Analysis training with Ladies in Tech Africa (LITA), the Incubator Hub.

### Tools Used
- Microsoft Excel [Download Here](https://www.microsoft.com)
  
    1. Data cleaning
  
    2. Analysis
  
    3. Visualisation
       
- SQL- Structured Querying Language for Querying of Data.
- Power BI for Data Visualisation.
- GitHub for Portfolio Building.

### Data Cleaning and Preparation
  At the initial stage of Data cleaning and preparation,the following actions were performed
  
    1. Data loading and Inspection
    
    2. Handling missing variables
    
    3. Removing duplicates
    
    4. Data cleaning and formatting

### Explanatory Data Analysis
      Explanatory Data Analysis involved exploring the data to answer some questions such as:

- Analyse customer data using pivot tables to find subscription patterns.
- Calculate the average subscription duration and identify the most popular subscription types.
- Write SQL queries to extract key insights.
- Create a Power BI dashboard that visualises the insights found in Excel and SQL.

 ### Data Analysis
  Here the line of codes, functions, queries, pivot tables visualisation,DAX expressions used during the analysis  

--- Pivot Tables Visualisation ---

![image](https://github.com/user-attachments/assets/cf29eefb-4c7d-4a2f-b72a-5172d82a86c2)
![image](https://github.com/user-attachments/assets/2416bf78-44fd-4ab1-9ebc-a9992a9d1bfa)
![image](https://github.com/user-attachments/assets/c9712e58-5284-4977-a0c3-579da513484d)
![image](https://github.com/user-attachments/assets/e9ec9688-a70a-4927-963f-f851bb5c4afc)





##### Metrics using Excel Formulas




##### SQL Queries to extract key insights

```SELECT Region, 
COUNT(CustomerID) AS
NumberOfCustomers
FROM Customerdata
GROUP BY Region
```

```SELECT TOP 1
SubscriptionType,
COUNT(CustomerID) AS
CustomerCount
FROM Customerdata
GROUP BY SubscriptionType
ORDER BY CustomerCount
DESC;
```

```SELECT CustomerName
FROM Customerdata
WHERE Canceled = 1
AND DATEDIFF (MONTH, SubscriptionStart, SubscriptionEnd) <= 6
```

```SELECT AVG(DATEDIFF(DAY,SubscriptionStart,
SubscriptionEnd))
AS AverageSubscriptionDuration
FROM Customerdata
```
```SELECT CustomerName
FROM Customerdata
WHERE DATEDIFF(MONTH,
SubscriptionStart, SubscriptionEnd) > 12;
```

```SELECT SubscriptionType,
SUM(Revenue) AS
TotalRevenue
FROM Customerdata
GROUP BY SubscriptionType
```

```SELECT Top 3 Region,
COUNT (CustomerID) AS Cancellations
FROM Customerdata
WHERE Canceled = 1
GROUP BY Region
ORDER BY Cancellations
DESC;
```

```SELECT 
SUM(CASE WHEN
Canceled = 0 THEN 1 ELSE 0 END)
AS ActiveSubscriptions,
SUM(CASE WHEN Canceled = 1 THEN 1 ELSE 0 END) AS
CanceledSubsciptions FROM Customerdata
```



![1customerdata](https://github.com/user-attachments/assets/41813c97-ca6a-409a-bfab-eedaac0f6878)

![2customerdata](https://github.com/user-attachments/assets/aff8cf27-e5cf-4611-a9f0-a23f8bbc123a)

![3customerdata](https://github.com/user-attachments/assets/f157f540-fd9f-42aa-bb04-71f55a992d5a)

![4customerdata](https://github.com/user-attachments/assets/6159fba8-7101-4121-88c7-23c000598df0)

![5customerdata](https://github.com/user-attachments/assets/f1ba7f93-6816-4ac5-840f-ade7eb82ca0b)

![6customerdata](https://github.com/user-attachments/assets/5ed60219-268d-40a1-9fbb-51b16a33cffb)

![7customerdata](https://github.com/user-attachments/assets/5a979c9c-9c0c-4f59-b8ff-b98e810942a3)

![8customerdata](https://github.com/user-attachments/assets/950b5773-8173-4cea-9413-ee0658fb2a56)
