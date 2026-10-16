# 📊 E-Commerce Sales Analysis – Power BI

## 📌 Project Overview

This project is part of my **Data Analytics learning journey**, where I use **Microsoft Power BI and Power Query** to prepare, clean, transform, model, and analyse an E-Commerce sales dataset.

The main objective of this project is to demonstrate practical skills in **data preparation, data cleansing, data transformation, data modelling, and business-oriented analysis** using Power BI.

---

## 🎯 Problem Statement

As a Data Analyst, I worked with an E-Commerce sales dataset containing multiple related tables representing orders, order details, and sales targets.

The project focuses on:

- Data import
- Data cleaning
- Data transformation
- Missing-value handling
- Duplicate-value handling
- Data aggregation
- Table merging
- Relationship modelling
- Data validation
- Business-focused analysis

The final prepared data model can be used to create meaningful Power BI reports and dashboards.

---

## 📂 Dataset Description

The project uses three datasets.

### 1. List of Orders

Contains order-level information.

| Column | Description |
|---|---|
| Order ID | Unique order identifier |
| Order Date | Date of the order |
| Customer Name | Customer name |
| City | Customer city |
| State | Customer state |
| Category | Product category |
| Amount | Order amount |
| Profit | Order profit |

### 2. Order Details

Contains detailed information about each order.

| Column | Description |
|---|---|
| Order ID | Order identifier |
| Category | Product category |
| Sub-Category | Product sub-category |
| Quantity | Quantity ordered |
| Amount | Sales amount |
| Profit | Profit generated |

### 3. Sales Target

Contains monthly sales targets.

| Column | Description |
|---|---|
| Category | Product category |
| Month of Order Date | Order month |
| Target | Sales target |

---

# 🛠️ Tools & Technologies

- **Microsoft Power BI**
- **Power Query Editor**
- **Power BI Data Model**
- **Power BI Relationships**
- **GitHub**
- CSV datasets

---

# 🔄 Data Preparation & Transformation

## 1. Data Import

Imported the following datasets into Power BI:

- `List of Orders.csv`
- `Order Details.csv`
- `Sales Target.csv`

The data was opened in **Power Query Editor** using the **Transform Data** option.

---

## 2. Row Limiting & Data Types

The following transformations were performed:

- Restricted the **List of Orders** table to the first **500 rows**.
- Changed **Order Date** to the **Date** data type.
- Changed **Amount** to **Fixed Decimal Number**.
- Changed **Target** to **Fixed Decimal Number**.

These transformations help maintain data consistency and accuracy.

---

## 3. Text Formatting

The **Customer Name** column was converted to **Proper Case** to maintain consistent customer-name formatting.

Example:

```text
john smith → John Smith
```

---

## 4. Created Columns

### Location

Merged the **City** and **State** columns into a new column:

```text
Location = City, State
```

Example:

```text
Chennai, Tamil Nadu
```

### Profit Margin

Created a custom column using:

```text
Profit Margin = Profit / Amount
```

The resulting column was formatted as a percentage.

---

## 5. Profit Status

Created a conditional column called **Profit Status**.

| Condition | Profit Status |
|---|---|
| Profit < 0 | Loss |
| Profit = 0 | Break-Even |
| Profit > 0 | Profit |

This classification helps identify whether each order generated a profit or loss.

---

# 🔗 6. Data Merging

The **List of Orders** and **Order Details** tables were merged using:

```text
Order ID
```

The merged output was named:

```text
Orders Data
```

This merge combines order-level and order-detail information for further analysis.

---

# 🧹 7. Missing & Duplicate Data Handling

Missing values were checked across all three datasets.

The following strategies were considered based on business relevance:

- Replace missing values where an appropriate value can be determined.
- Remove records when missing information makes the record unusable.
- Retain null values when the missing information is meaningful or cannot be safely replaced.

Duplicate records were also identified.

Duplicate handling was based on the business meaning of each table rather than simply deleting every repeated value.

For example, multiple records with the same **Order ID** in the Order Details table may be valid because one order can contain multiple products or sub-categories.

---

# 🔽 8. Sorting & Filtering

The **Orders Data** table was sorted by:

```text
Order Date → Descending
```

A state filter was also applied to analyse orders from a specific state, such as:

```text
Tamil Nadu
```

This allows regional sales information to be analysed separately.

---

# 📊 9. Grouping & Aggregation

### Order Details Analysis

A duplicate of the **Order Details** table was created to perform aggregation.

The following analyses were performed:

### Count of Order ID

Calculated the number of order records.

### Average Profit by Category

Calculated the average profit for each product category.

### Total Amount by Sub-Category

Calculated the total sales amount for each sub-category.

---

## Sales Target Analysis

A duplicate of the **Sales Target** table was created.

The data was grouped by:

```text
Month of Order Date
```

The **Target** values were aggregated to calculate the total monthly sales target.

---

# 🧩 10. Data Modelling

Relationships were established between the tables.

### Relationship 1

```text
List of Orders
       │
       │ Order ID
       ▼
Order Details
```

### Relationship 2

```text
Order Details
       │
       │ Category
       ▼
Sales Target
```

The relationships were checked using **Manage Relationships** in Power BI.

The relationships were verified to ensure that they were:

- Active
- Correctly defined
- Based on the appropriate columns

---

# 📈 Key Skills Demonstrated

Through this project, I practised the following Data Analyst skills:

- Data Import
- Data Cleaning
- Data Transformation
- Power Query
- Data Type Conversion
- Text Formatting
- Custom Columns
- Conditional Columns
- Data Merging
- Missing-Value Handling
- Duplicate Handling
- Sorting & Filtering
- Grouping & Aggregation
- Data Modelling
- Relationship Management
- Power BI

---

# 💡 Business Analysis Opportunities

The prepared dataset can be used to answer business questions such as:

- Which product categories generate the highest profit?
- Which sub-categories generate the highest sales?
- Which states generate the most orders?
- Which orders result in losses?
- What is the average profit by category?
- How does actual sales performance compare with monthly targets?
- Which months have the highest sales targets?
- Which regions have stronger sales performance?

---

# 📁 Project Structure

```text
POEWR-BI-ASS-MENT/
│
├── README.md
│
├── List of Orders.csv
├── Order Details.csv
├── Sales Target.csv
│
├── Power BI/
│   └── E-Commerce-Sales-Analysis.pbix
│
└── Screenshots/
    ├── Power Query.png
    ├── Data Model.png
    └── Power BI Dashboard.png
```

---

# 🎓 Learning Outcome

This project helped me develop practical knowledge of **Power BI data preparation and modelling**.

I learned how to take raw datasets, clean and transform them using Power Query, combine related datasets, create calculated columns, perform aggregations, and establish relationships between tables.

This project is part of my journey towards becoming a **Data Analyst** and will be included in my Data Analytics portfolio.

---

# 🚀 Future Improvements

I plan to extend this project by creating an interactive Power BI dashboard containing:

- KPI Cards
- Sales Analysis
- Profit Analysis
- Category Analysis
- Sub-Category Analysis
- State/Regional Analysis
- Monthly Sales Trends
- Sales Target vs Actual Analysis
- Interactive filters and slicers

---

## 👨‍💻 Author

**Karthick Raja**

Aspiring Data Analyst

### Skills Currently Developing

- Microsoft Excel
- Power BI
- Power Query
- Data Cleaning
- Data Analysis
- Data Visualization
- SQL
- Python

---

## ⭐ Portfolio

This repository is part of my **Data Analytics Portfolio**, where I document my projects and practical learning in data analysis.

If you find this project useful, feel free to explore the repository and follow my Data Analytics journey.
# POEWR-BI-ASS-MENT
