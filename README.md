# Empowering Business Insights: Revenue Analysis in Sports Manufacturing

## Overview

This repository contains a comprehensive data analytics project focused on revenue analysis for multiple products. The project utilizes Extract-Load-Transform (ELT) processes with data stored in Excel and CSV files. The data is then loaded onto Power BI for further transformation and analysis, culminating in the creation of a detailed and insightful revenue analysis dashboard.

## Project Structure

### 1. Extract

The raw dataset in the form of comma separated files (csv) and excel files is extracted from a gooogle drive link where it is stored for access. The file/folder structure and their contents is as described below: 
- Folder: `USSales`
  - Contains the `sales` table for USA. Additionally, it also contains the `product`, `manufacturer`, and  `geography` tables. 
- Folder: `InternationalSales`
  - Contains the `sales` table for the rest of the world i.e., Canada, Australia, Germany, Japan, Nigeria etc.

### 2. Load 

After extraction, the raw data is loaded directly into the target system, i.e., Power BI. The loading process is completed without significant transformation.

### 3. Transform

Once the data is in the target system, transformations and data processing occur within the system. This step involves applying transformations directly within Power BI using the `Query Editor` tool. The editor provides a robust set of data transformation capabilities to clean, reshape, and enrich your data before it is loaded into the Power BI model. The steps involved are described below:
1) **Promoted Headers**: The top row was selected to reflect the header of the table.
2) **Removed Redundant Rows**: Removed rows that did not belong to any record to clean the dataset.
3)  **Datatype Conversion**: Converted datatype based on the column e.g., `Zip` from whole number to text to include leading zeros.
4)  **Fill Up/Down**: Utilized the "Fill Down" or "Fill Up" options to propagate values within a column based on the preceding or following values. This is useful for filling missing data.
5)  **Split Columns**: Split a column into multiple columns based on delimiters such as underscore, comma, etc., for breaking down combined information into individual components. For example to extract state from address.
6)  **Deleting Redundant Columns**: Removed columns that were no longer required.
7)  **Renaming Columns**: Renamed columns to provide more meaningful and concise names.
8)  **Appended Queries**: Combined data from  the `International Sales` tables using with the `US Sales` table. This was applied to perform joins and consolidate data since both tables shared the schema/structure.
9)  **Conditional Columns**: Created new columns based on specified conditions for introducing calculated columns such as defining customer category based on sum of sales, etc.
10)  **Measures**: Created multiple measures - a type of calculation that is used to perform aggregations, or other operations on the data in your dataset. Measures are typically created using the `DAX (Data Analysis Expressions)` language, which is a formula language used in Power BI for creating custom calculations. These are created using the report view, are reusable across visulaizations, and respond dynamically to changes in the report's context.

### 4. Analysis and Insights

VanArsdel, a manufacturer and distributor of sporting goods, operates globally with offices in the United States and various other countries. The company's sales encompass both the domestic market and international territories. Amidst the dynamic growth of the sporting goods market, competitors present formidable challenges in terms of sales. The objective is to conduct a thorough analysis and develop a comprehensive revenue/sales dashboard. This dashboard aims to provide crucial insights into the comparative performance of VanArsdel against its competitors, facilitating proactive decision-making.

![model view](https://github.com/HassanMahmoodKhan/Data-Driven-Product-Analytics/assets/97694796/722b35ea-e56d-4692-934e-8c6db2d53399)

The data model employed is the STAR schema for business intelligence systems. We have five tables:
- **Product**: This table contains information about the product including a primary key, `ProductID` and foreign key, `ManufacturerID`. It also contains other information such as product price, currency, category, etc. This table is categorized as a dimension table under the star schema.
- **Sales**: It contains information related to the revenue generated and units sold for the products. It is an instance of the fact table under the star schema.
- **Manufacturer**: It contains information about the various manufacturers including VanArsdel and it's competitors. An instance of dimension table.
- **Geography**: Another descriptive/dimension table that holds data related to country, region, state, city, etc., where the product is sold.
- **Date**: This table represents the temporal details of the sales and contains columns such as date, year, month of sale, etc.


#### Objective

To boost company sales, I aim to deliver insights that are simple and easy to understand but also readily digestible. The approach involves presenting information in a clear and straightforward manner, making it accessible to a wide audience and empowering them to make informed decisions swiftly, fostering a more agile and responsive sales strategy for overall growth

### 5. Dashboard

 To access the Power BI report file that contains the data model, relationships, visualizations related to the final revenue analysis dashboard - please use this [Google Drive Link](https://drive.google.com/file/d/1xT8o33NH7S1VjbFjbVRrcwBtNP78ytsI/view?usp=sharing).
 
![dashboard thumbnail](https://github.com/HassanMahmoodKhan/Empowering-Business-Insights-Revenue-Analysis-in-Sports-Manufacturing/assets/97694796/b218c73a-f2b8-4e9e-8976-ba6cdd1377b5)


### 6. Deployment

For deployment purposes, I have published the report using Power BI Desktop to the [Power BI App](https://app.powerbi.com/) which allows stakeholders to view and consume the report.

## Requirements

This section contains the requirements needed to run the report. Please refer to the list below:
- Microsoft Power BI Desktop Version: 2.126.927.0 64-bit
- Microsoft Power BI App Account
- Microsoft Excel

## License

This repository employs the Apache 2.0 license. For more information, please refer to the license.

