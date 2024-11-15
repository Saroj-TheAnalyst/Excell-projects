# Excel and Power BI Projects

## Repository Overview
This repository contains various Excel and Power BI projects focused on data analysis, reporting, and visualization. The projects cover topics like sales analysis, data cleaning, and the use of advanced Excel and Power BI techniques to extract actionable insights from datasets.

## Files Included

1. **Power BI - Final Project.xlsx**
   - This file is part of a Power BI project that involves data analysis and visualization.
   - The dataset and transformations have been set up for further analysis in Power BI.

2. **Data Cleaning Excel Tutorial.xlsx**
   - This file is a tutorial on how to clean and prepare data in Excel. It demonstrates various techniques such as removing duplicates, handling missing values, and applying filters.

3. **My_Excel_Project_Dataset.xlsx**
   - A dataset for an Excel project. It covers sales, regions, and products, and includes pre-built formulas and pivot tables for analysis.

4. **README.md**
   - This file provides an overview of the repository and guidance on how to use the datasets and files provided.

## Power BI Project: Power BI - Final Project

### Overview
The Power BI project in this repository focuses on sales data analysis. The main goal is to provide insightful visualizations and DAX calculations to analyze sales trends, product performance, and regional sales.

### Setup Instructions
1. **Download Power BI Desktop** if you don't already have it installed: [Download Power BI Desktop](https://powerbi.microsoft.com/downloads/)
2. **Load the Data**:
   - Open Power BI Desktop.
   - Click on `Get Data` > `Excel` and select the `Power BI - Final Project.xlsx` file.
   - Import the necessary tables from the Excel file.

3. **Data Transformation**: In Power BI, use the Power Query editor to clean the data as needed. Apply steps like:
   - Removing unnecessary columns.
   - Changing data types (e.g., Date fields to Date).
   - Renaming columns for clarity.

4. **Creating Visualizations**: Build visualizations such as:
   - **Bar Charts** for sales by region and category.
   - **Line Charts** for sales trends over time.
   - **Tables** to display detailed sales information.

5. **DAX Calculations**: Perform key DAX calculations such as:
   - **Total Sales**: 
     ```DAX
     Total Sales = SUM(Sales[SalesAmount])
     ```
   - **YoY Growth**:
     ```DAX
     YoY Growth = 
     DIVIDE(
         SUM(Sales[SalesAmount]) - CALCULATE(SUM(Sales[SalesAmount]), SAMEPERIODLASTYEAR('Date'[Date])),
         CALCULATE(SUM(Sales[SalesAmount]), SAMEPERIODLASTYEAR('Date'[Date])),
         0
     )
     ```

### Key Insights
This Power BI report helps uncover important insights such as:
- **Sales Growth**: Year-over-year performance analysis.
- **Top Products**: The best-performing products based on sales.
- **Regional Sales Performance**: Breakdown of sales by region.

## Excel Projects

### 1. **Data Cleaning Excel Tutorial**
   - This file provides an introduction to Excel data cleaning techniques.
   - It covers removing duplicates, handling missing data, applying filters, and basic text manipulations.

### 2. **My_Excel_Project_Dataset**
   - This dataset contains information on sales, regions, and products.
   - The project includes pivot tables, charts, and formulas to analyze data within Excel.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For any questions, feel free to reach out to me:

- **Email**:  sarojpokhrel41@gmail.com
- **GitHub**: [Saroj-TheAnalyst](https://github.com/Saroj-TheAnalyst)
