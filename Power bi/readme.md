# Power BI - Final Project

## Project Overview
This Power BI project is focused on analyzing sales data using a variety of visualizations, transformations, and DAX calculations. The goal is to provide actionable insights into the sales performance, trends, and growth.

## Data Source
- The project uses an Excel file, which includes datasets related to sales transactions.
- The datasets are loaded into Power BI for analysis and visualizations.

## Project Structure
1. **Data Transformation**: Using Power Query Editor to clean and prepare the data.
2. **Modeling**: Establish relationships between tables for analysis.
3. **Visualizations**: Create charts, graphs, and tables to visualize the data.
4. **DAX Calculations**: Custom calculations to analyze sales, growth, and other key metrics.

## Setup Instructions

### 1. **Load the Data into Power BI**
   - Open Power BI Desktop.
   - Click on `Get Data` > `Excel`.
   - Load the `Power BI - Final Project.xlsx` file into Power BI.
   - Select the relevant sheets and click `Load`.

### 2. **Data Transformation in Power Query Editor**
   - Use Power Query Editor to apply the following transformations:
     - **Remove unnecessary columns**.
     - **Change data types** for correct interpretation (e.g., Date columns should be Date, Numeric columns should be Decimal).
     - **Rename columns** for clarity.
   - After applying the necessary transformations, click `Close & Apply`.

### 3. **Creating Relationships**
   - Open the `Model` view in Power BI.
   - Create relationships between tables (e.g., link `ProductID` in Sales table to `ProductID` in Products table).
   - Manage relationships as needed.

### 4. **Building Visualizations**
   - Use Power BI’s **Visualizations** pane to create various charts and tables:
     - **Bar Chart**: For sales by region or category.
     - **Line Chart**: For sales trends over time.
     - **Pie Chart**: To show distribution by product or region.
     - **Table/Matrix**: For detailed sales data.

### 5. **DAX Calculations for Key Metrics**
   - **Total Sales**:
     ```DAX
     Total Sales = SUM(Sales[SalesAmount])
     ```
   - **YoY (Year-over-Year) Growth**:
     ```DAX
     YoY Growth = 
     DIVIDE(
         SUM(Sales[SalesAmount]) - CALCULATE(SUM(Sales[SalesAmount]), SAMEPERIODLASTYEAR('Date'[Date])),
         CALCULATE(SUM(Sales[SalesAmount]), SAMEPERIODLASTYEAR('Date'[Date])),
         0
     )
     ```
   - **Cumulative Sales**:
     ```DAX
     Cumulative Sales = 
     CALCULATE(
         SUM('Sales'[SalesAmount]),
         FILTER(
             ALL('Date'[Date]),
             'Date'[Date] <= MAX('Date'[Date])
         )
     )
     ```
   - **Average Sales**:
     ```DAX
     Average Sales = AVERAGE('Sales'[SalesAmount])
     ```

### 6. **Adding Slicers for Filtering**
   - To make your reports interactive, add slicers for filtering data:
     - Drag a field like `Region`, `Category`, or `Date` into the slicer.
     - This allows users to filter visualizations based on these fields.

### 7. **Publishing and Sharing**
   - After building your report, click `Publish` in Power BI Desktop to upload your report to Power BI Service.
   - Once published, you can share the report with others via Power BI Service.

## Key Insights
The goal of this Power BI project is to analyze the sales data and provide insights such as:
- **Sales Growth**: Analyzing year-over-year growth.
- **Top Products**: Identifying the top-selling products.
- **Sales by Region**: Analyzing sales performance by different regions.
- **Cumulative Sales**: Tracking sales over time to monitor performance.

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Contact
For any questions, feel free to reach out to me:

- Email:  sarojpokhrel41@gmail.com
- GitHub: [Saroj-TheAnalyst](https://github.com/Saroj-TheAnalyst)
