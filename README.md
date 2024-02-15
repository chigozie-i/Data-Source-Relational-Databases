![RDB](https://github.com/chigozie-i/Data-Source-Relational-Databases/blob/main/Connecting%20To%20RDB.png)

## Introduction:
In today’s data driven world, organizations rely heavily on insights derived from data to drive strategic decision-making and enhance operational efficiency. Microsoft Power BI stands as a powerful tool in this landscape, offering robust capabilities for connecting to various data sources, transforming raw data into meaningful insights, and creating interactive visualizations and reports.

## Table of Contents

- [Overview](#Overview)
- [Data Sources](#Data-Sources)
- [Connecting To Files](#Connecting-To-Files)
- [Connect to File Data](#How-To-Connect-To-Data-In-A-File)
- [Connection Path](#File-Connection-Path)
- [Storage Mode](#Data-Storage-Mode)
- [Lessons Learnt](#Lessons-Learnt)
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


