# Tableau-Performance-Optimization-Interactive-Dashboard
Project Overview

This project is based on the Online Retail II dataset and was created in Tableau Public. The main goal is to analyse e-commerce sales while applying practical ideas for data preparation, performance optimization, interactive visualization, and dashboard design.

Objectives

Prepare and clean the retail transaction data.

Combine the two yearly datasets using a UNION.

Remove cancelled and invalid transactions.

Create useful calculated fields and KPIs.

Build interactive sales and customer analysis dashboards.

Add geographic analysis using a Country Map.

Improve dashboard usability without adding unnecessary visual complexity.

Dataset

The project uses the Online Retail II dataset from the UCI Machine Learning Repository.

Main fields include:

Invoice

StockCode

Description

Quantity

InvoiceDate

Price

Customer ID

Country

The two yearly sheets, 2009–2010 and 2010–2011, were combined for analysis.

Data Preparation

The following data-source filters were applied:

Excluded invoices beginning with C because they represent cancellations.

Quantity >= 1

Price >= 0

Customer ID nulls were retained at the data-source level so that valid sales transactions were not unnecessarily removed.

Calculated Fields

Sales

[Quantity] * [Price]

Total Orders

COUNTD([Invoice])

Total Customers

COUNTD([Customer ID])

Average Order Value

SUM([Sales]) / COUNTD([Invoice])

Day of Week

DATENAME('weekday', [InvoiceDate])

Sales Hour

DATEPART('hour', [InvoiceDate])

Worksheets

The workbook contains:

KPI Summary – Key business performance indicators.

Monthly Sales Trend – Monthly sales movement.

Sales by Country – Country-level sales comparison.

Customer Analysis – Customer sales performance.

Sales by Day Hour – Sales patterns by day and hour.

Country Map – Geographic distribution of sales.

Dashboards

E-Commerce Sales Analysis

Provides the overall sales view using KPIs, monthly sales trends and country performance.

Customer Sales Analysis

Focuses on customer performance and sales patterns by day and hour.

Geographic Sales Analysis – Final Dashboard

The Country Map is used as the main visual. The recommended final layout contains:

Dashboard title

Year filter

Country filter

KPI Summary

Large Country Map

Sales-based colour scale

Informative map tooltips

Optional country selection filter action

Performance Optimization

Performance was considered during both data preparation and dashboard design. Unnecessary transactions were removed early using data-source filters. Calculated fields were kept simple, and dashboards were designed with a controlled number of visuals. Interactive filters, tooltips and map actions provide useful exploration without unnecessarily increasing dashboard complexity.

Interactivity

Users can:

Select a year.

Select one or more countries.

Hover over countries to see detailed sales information.

Select a country to filter related views when dashboard actions are enabled.

Key Insights

The dashboards help users understand overall sales performance, monthly trends, important markets, customer contribution, time-based sales behaviour and the geographic distribution of revenue.

Tools Used

Tableau Public

Microsoft Excel

GitHub

UCI Online Retail II Dataset

Project Files

Task5(3).twb – Tableau workbook

Task5_Tableau_Final_Report.docx – Detailed project report

README.md – Project documentation

Conclusion

This project demonstrates how Tableau can be used not only to create charts but also to build an efficient and interactive analytical experience. The final geographic dashboard adds another layer of exploration by allowing users to understand sales performance across countries.
