![RDB](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Connecting%20To%20RDB.png)

## Introduction:
In today’s data driven world, organizations rely heavily on insights derived from data to drive strategic decision-making and enhance operational efficiency. Microsoft Power BI stands as a powerful tool in this landscape, offering robust capabilities for connecting to various data sources, transforming raw data into meaningful insights, and creating interactive visualizations and reports.

## Table of Contents

- [Overview](#Overview)
- [Data Sources](#Data-Sources)
- [Connecting To A Relational Database](#Connecting-To-A-Relational-Database)
- [How To Connect To Data In Your Database](#How-To-Connect-To-Data-In-Your-Database)
- [Importing Data By Writing An SQL Query](#Importing-Data-By-Writing-An-SQL-Query)
- [Change Data Source Setting](#Change-Data-Source-Setting)
- [Conclusion](#Conclusion)
- [Reference](#Reference)
  
## Overview:

This document focuses on utilizing Microsoft Power BI for data analysis, forming part of a series of documentation projects aimed at exploring various methods for connecting to your data source. This document seeks to underscore the critical significance of selecting an appropriate data source connection method and to offer comprehensive guidance on the diverse approaches available for establishing connectivity to your data source prior to initiating any essential data transformations tailored to your analytical objectives.

The primary goal of this endeavor is to establish a dependable repository for your data, fostering operational efficiency and ensuring the accuracy of reporting in alignment with the business requirements.

The method by which you establish connectivity to your data source holds considerable importance, as it directly influences the efficiency of your analytical tools and shapes the user experience. Moreover, it plays a pivotal role in determining the effectiveness, precision, and trustworthiness of the analytical processes and resulting reports.


## Data Sources:
Sometimes, you may be required to build Microsoft Power BI reports, with data sourced from various databases and files. These data sources vary, with some housed in Microsoft SQL Server and others in Microsoft Excel, yet they are all interconnected.

![Data Sources](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Data%20sources.png)

Prior to report creation, it's essential to extract data from the various data sources. As the interaction with the sources differ, familiarizing yourself with the intricacies of the source platforms is imperative to report building within Power BI.

#### Data Sources:

1.	Files
2.	Relational Data Sources | Create Dynamic Reports with Parameters
3.	NoSQL Database 
4.	Online Services
5.	Azure Analysis Services


This documentation project focuses on RDB-Relational Databases.

## Connecting to a Relational Database (RDB):

![RDB Connection](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/RDB%20PBI%20Connection.png)

Imaginary Inc. is an organization that uses a relational database for sales; it connects directly to the database using Power BI, instead of using exported flat files.
Connecting Power BI to your database will help you to monitor the progress of your business and identify trends, so you can forecast sales figures, plan budgets, and set performance indicators and targets. Power BI Desktop can connect to many relational databases that are either in the cloud or on-premises.

## How To Connect To Data In Your Database:

#### Step I:
Use the Get data feature in Power BI Desktop and select the applicable option for your relational database.

![Get Data](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Get%20Data%20I.png)

#### Step II:
Enter your database server name and a database name in the SQL Server database window. The two options in data connectivity mode are: Import and DirectQuery. Import is selected by default and is the recommended option. 

![Server SignIn](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/SQL%20Svr%20DB%20II.png)

#### Step III:

After you've added your server and database names, you'll be prompted to sign in with a username and password. You'll have three sign-in options:
- Windows - Use your Windows account (Azure Active Directory credentials).
- Database - Use your database credentials. SQL Server has its own sign-in and authentication system that is sometimes used. If your database administrator has given you a unique sign-in to the database, you may enter those credentials on the Database tab.
- Microsoft account - Use your Microsoft account credentials. This option is often used for Azure services.

Select a sign-in option, enter your username and password, and then select Connect.

![Select signin option](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Sign%20In%20III.png)

#### Step IV:

After the database has been connected to Power BI Desktop, the Navigator window displays the data that is available in your data source. You can select a table or entity to preview its contents and make sure that the correct data will be loaded into the Power BI model.
Select the check box(es) of the table(s) that you want to bring in to Power BI Desktop, and then select either the Load or Transform Data option.
- Load - Automatically load your data into a Power BI model in its current state.
- Transform Data - Open your data in Microsoft Power Query, where you can perform actions such as deleting unnecessary rows or columns, grouping your data, removing errors, and many other data quality tasks.

![Select Table](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Select%20Table%20IV.png)

## Importing Data by Writing an SQL Query:

Another way to import data from a relational database is to write an SQL query to specify only the tables and columns that you need.
To write your SQL query, on the SQL Server database window, enter your server and database names, and then select the arrow next to Advanced options to expand this section and view your options. In the SQL statement box, write your query statement, and then select OK.

#### Writing your SQL Statement
Consider the scenario where your database has a large table that is comprised of sales data over several years. Sales data up to 2019 isn't relevant to the report that you're creating. This situation is where SQL is beneficial because it allows you to load only the required set of data by specifying exact columns and rows in your SQL statement and then importing them into your semantic model. You can also join different tables, run specific calculations, create logical statements, and filter data in your SQL query.

The SQL query starts with a Select statement, which allows you to choose the specific fields that you want to pull from your database. In this example, you want to load the ProductID, ProductName, and SalesAmount columns.

SELECT ProductID, ProductName, SalesAmount
FROM specifies the name of the table that you want to pull the data from. In this case, it's the ProductSales table. 

SELECT ProductID, ProductName, SalesAmount
FROM ProductSales

All queries should also have a WHERE clause. This clause will filter the rows to pick only filtered records that you want. In this example, if you want to get recent sales data after January 1st, 2020, add a WHERE clause.

SELECT ProductID, ProductName, SalesAmount
FROM ProductSales
WHERE OrderDate >= ‘1/1/2020’

It's best practice to avoid doing this directly in Power BI. Instead, consider writing a query like this in a view. A view is an object in a relational database, similar to a table. Views have rows and columns and can contain almost every operator in the SQL language.

![SQL statement](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/SQL%20Statement.png)

## Change Data Source Setting:

After you create a data source connection and load data into Power BI Desktop, you can return and change your connection settings at any time. This action is often required due to a security policy within the organization, for example, when the password needs to be updated every 90 days. You can change the data source, edit permissions or clear permissions.

On the Home tab, select Transform data, and then select the Data source settings option.

![data source setting I](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Data%20Source%20change%20I.png)

Select the update option that you need, change the settings as required, and then apply your changes.

![data source setting II](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Data%20Source%20change%20II.png)

You can also change your data source settings from within Power Query. Select the table, and then select the Data source settings option on the Home ribbon. Alternatively, you can go to the Query Settings panel on the right side of the screen and select the settings icon next to Source (or double Select Source). In the window that displays, update the server and database details, and then select OK.

![data source setting III](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Data%20Source%20change%20III.png)

After you have made the changes, select Close and Apply to apply those changes to your data source settings.

## Conclusion:

Throughout this documentary project, we embarked on a journey to explore the process of connecting Power BI to a relational database as a data source. 

Our primary goal was to demonstrate the seamless integration of Power BI with a relational database to extract, transform, and visualize data effectively. We aimed to provide a clear understanding of the steps involved in establishing this connection and harnessing its potential for insightful analytics.

While we achieved our primary objectives, there are areas where further refinement and improvement are warranted. Streamlining the data extraction and transformation processes, optimizing query performance, and implementing robust data governance practices can enhance the efficiency and reliability of Power BI solutions.

Additionally, exploring advanced analytics capabilities within Power BI, such as predictive modeling, machine learning integration, and natural language processing, opens new avenues for extracting deeper insights from relational databases. Investing in training and upskilling initiatives can empower users to leverage these advanced features effectively.

## REFERENCE:
- https://learn.microsoft.com
- https://docs.microsoft.com



