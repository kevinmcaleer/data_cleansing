# How to Clean and Analyze Traffic Survey Data in Excel (Power Query & Pivot Tables)

This guide walks you through cleaning and analyzing the same car survey data in Excel, using Power Query for data cleansing and Pivot Tables for analysis and visualization.

---

## 1. Import the Data into Excel
- Open Excel and go to the **Data** tab.
- Click **Get Data > From File > From Text/CSV**.
- Select your CSV file (e.g., `dirty_data1.csv`).
- Click **Load** to import the data into a new worksheet.
- Repeat for other CSVs if needed, or combine them in Power Query (see below).

## 2. Combine Multiple CSV Files (Optional)
- Go to **Data > Get Data > Combine Queries > Append**.
- Select the tables/queries you want to combine (e.g., all three class groups).
- Click **OK** to create a single combined table.

## 3. Clean the Data with Power Query
- With your table selected, go to **Data > Get Data > Launch Power Query Editor**.
- In Power Query:
  - **Remove Duplicates**: Select all columns, right-click, and choose **Remove Duplicates**.
  - **Trim Whitespace**: Select columns like 'Car Colour', 'Make', 'Model', then go to **Transform > Format > Trim**.
  - **Standardize Case**: Use **Transform > Format > UPPERCASE** for columns like 'Car Colour', 'Make', 'Model'.
  - **Replace Values**: For typos (e.g., 'BLU' → 'BLUE', 'GRN' → 'GREEN'), select the column, right-click, and choose **Replace Values**.
  - **Handle Missing Data**:
    - For categorical columns, use **Replace Values** to change null/blank to 'UNKNOWN'.
    - For numeric columns like 'Occupants', filter out or replace blanks as needed.
  - **Change Data Types**: Set 'Date' to **Date**, 'Occupants' to **Whole Number**.
  - **Remove Non-Car Entries**: Filter out rows where 'Make' is 'CYCLIST', 'BIKE', etc.
- Click **Close & Load** to return the cleaned data to Excel.

## 4. Create Pivot Tables for Analysis
- Select your cleaned data table.
- Go to **Insert > Pivot Table**.
- Place the Pivot Table in a new worksheet.

### Example Analyses:
- **Most Popular Car Type**: Drag 'Make' to Rows, count 'Make' in Values.
- **Car Model with Most Occupants**: Drag 'Model' to Rows, sum 'Occupants' in Values.
- **Busiest Day**: Drag 'Date' to Rows, count 'Date' in Values.
- **Car Colour Distribution**: Drag 'Car Colour' to Rows, count 'Car Colour' in Values.
- **Vehicles per Day**: Drag 'Date' to Rows, count 'Make' or 'Model' in Values.

## 5. Add Slicers for Interactive Filtering
- Click inside your Pivot Table.
- Go to **PivotTable Analyze > Insert Slicer**.
- Choose fields like 'Car Colour', 'Make', or 'Date'.
- Use slicers to filter and explore your data interactively.

## 6. Create Charts
- With your Pivot Table selected, go to **Insert > Charts**.
- Choose a bar chart, column chart, or line chart to visualize your results.

---

**Tip:** You can refresh your analysis any time by right-clicking the Pivot Table and choosing **Refresh** after updating your data or Power Query steps.

---

This workflow lets you repeat the same data cleaning and analysis process in Excel as you did in Python/Jupyter, using only built-in Excel tools.
