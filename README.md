# 💰 Sales Data Analysis using Python Pandas

## 📌 Project Introduction

This project is based on performing data analysis operations on a Sales Dataset using Python and the Pandas library inside Jupyter Notebook. The dataset contains information related to products, quantity sold, revenue, payment methods, cities, managers, and sales dates.

The main objective of this project is to understand how Python and Pandas are used in real-world sales data analysis for cleaning, filtering, grouping, statistical analysis, and extracting meaningful business insights from structured datasets efficiently.

In this project, different data analysis techniques were implemented such as:

- Data Cleaning
- Removing Duplicate Records
- Revenue Analysis
- Product-wise Analysis
- Payment Method Analysis
- Statistical Analysis
- Date-Time Analysis
- Data Visualization
- Exploratory Data Analysis (EDA)

This project provides practical exposure to working with business and sales datasets and understanding how data analysts use Python for extracting meaningful insights from sales performance data.

---

# 📂 Dataset Information

The dataset contains sales transaction records of products sold through different payment methods, cities, and managers.

### Dataset Features:

- Product
- Quantity Sold
- Revenue
- Payment Method
- City
- Manager
- Sales Date

Each record in the dataset represents a sales transaction.

---

# 🛠️ Tools & Technologies Used

## 🐍 Python
Python was used as the programming language for performing data analysis and dataframe operations.

## 📊 Pandas
Pandas library was used for:
- Data Cleaning
- Data Manipulation
- Revenue Analysis
- Filtering Data
- Statistical Analysis
- GroupBy Operations

## 📈 Matplotlib
Used for:
- Bar Graphs
- Revenue Visualization
- Sales Trend Analysis

## 📓 Jupyter Notebook
Jupyter Notebook was used to execute Python code interactively and visualize outputs step-by-step.

---

# 🔍 Pandas Functions Implemented

## 🔹 reset_index()
Converts the index into a dataframe column.

### Syntax:
```python
data.reset_index()
```

---

## 🔹 loc[]
Used to access rows and columns by labels.

### Syntax:
```python
data.loc[0]
```

---

## 🔹 info()
Displays complete dataset information.

### Syntax:
```python
data.info()
```

---

## 🔹 drop()
Removes columns or rows from the dataframe.

### Syntax:
```python
data.drop('Column_Name', axis=1)
```

---

## 🔹 str.strip().str.replace()
Removes extra spaces from text columns.

### Syntax:
```python
data['Product'] = data['Product'].str.strip().str.replace(r'\s+', ' ', regex=True)
```

---

## 🔹 duplicated()
Checks duplicate records.

### Syntax:
```python
data.duplicated()
```

---

## 🔹 drop_duplicates()
Removes duplicate records.

### Syntax:
```python
data.drop_duplicates(inplace=True)
```

---

## 🔹 round()
Rounds numerical values.

### Syntax:
```python
data['Revenue'].round(2)
```

---

## 🔹 pd.to_datetime()
Converts date column into datetime datatype.

### Syntax:
```python
data['Date'] = pd.to_datetime(data['Date'])
```

---

## 🔹 groupby()
Groups data based on specific columns.

### Syntax:
```python
data.groupby('Product')['Revenue'].sum()
```

---

## 🔹 std()
Calculates standard deviation.

### Syntax:
```python
data['Revenue'].std()
```

---

## 🔹 var()
Calculates variance.

### Syntax:
```python
data['Revenue'].var()
```

---

## 🔹 mean()
Calculates average values.

### Syntax:
```python
data['Revenue'].mean()
```

---

## 🔹 agg()
Applies multiple aggregate functions.

### Syntax:
```python
data.groupby('Product')[['Quantity', 'Revenue']].agg({
    'Quantity': 'mean',
    'Revenue': 'mean'
})
```

---

## 🔹 value_counts()
Displays unique values with their counts.

### Syntax:
```python
data['Payment_Method'].value_counts()
```

---

## 🔹 plot(kind='bar')
Creates bar graph visualization.

### Syntax:
```python
data['Product'].value_counts().plot(kind='bar')
```

---

## 🔹 dt.month
Extracts month values from date column.

### Syntax:
```python
data['Month'] = data['Date'].dt.month
```

---

# 📊 Tasks Performed in the Project

## ✅ Q1) Preferred Payment Method Analysis

### Task:
Find the most preferred payment method.

### Code Used:
```python
data['Payment_Method'].value_counts()
```

### Explanation:
- Counts occurrences of payment methods
- Helps identify most used payment option

---

# 📊 Q2) Most Selling Product Analysis

### Task:
Find the most selling product by quantity and revenue.

### Code Used:
```python
data.groupby('Product')['Quantity'].sum()

data.groupby('Product')['Revenue'].sum()
```

### Explanation:
- Groups sales by product
- Calculates total quantity and revenue

---

# 📊 Q3) City & Manager Revenue Analysis

### Task:
Find city and manager with highest revenue.

### Code Used:
```python
data.groupby('City')['Revenue'].sum().sort_values(ascending=False)

data.groupby('Manager')['Revenue'].sum().sort_values(ascending=False)
```

### Explanation:
- Groups revenue by city and manager
- Helps identify best-performing locations and managers

---

# 📊 Q4) Date-wise Revenue Analysis

### Task:
Show date-wise revenue.

### Code Used:
```python
data.groupby('Date')['Revenue'].sum()
```

### Explanation:
- Groups revenue by date
- Useful for sales trend analysis

---

# 📊 Q5) Average Revenue Analysis

### Task:
Find average revenue.

### Code Used:
```python
data['Revenue'].mean()
```

### Explanation:
- Calculates overall average revenue
- Helps analyze business performance

---

# 📊 Q6) November & December Revenue Analysis

### Task:
Find average revenue for November and December.

### Code Used:
```python
data.groupby('Month')['Revenue'].mean()
```

### Explanation:
- Groups revenue by month
- Helps analyze seasonal sales trends

---

# 📊 Q7) Standard Deviation Analysis

### Task:
Find standard deviation of Revenue and Quantity.

### Code Used:
```python
data['Revenue'].std()

data['Quantity'].std()
```

### Explanation:
- Measures data spread and variability
- Useful for statistical analysis

---

# 📊 Q8) Variance Analysis

### Task:
Find variance of Revenue and Quantity.

### Code Used:
```python
data['Revenue'].var()

data['Quantity'].var()
```

### Explanation:
- Measures variation in sales data
- Helps understand sales fluctuations

---

# 📊 Q9) Revenue Trend Analysis

### Task:
Analyze whether revenue was increasing or decreasing over time.

### Code Used:
```python
data.groupby('Date')['Revenue'].sum().plot()
```

### Explanation:
- Visualizes sales trends over time
- Helps identify business growth patterns

---

# 📊 Q10) Product-wise Average Analysis

### Task:
Find average Quantity Sold and Revenue for each product.

### Code Used:
```python
data.groupby('Product')[['Quantity', 'Revenue']].agg({
    'Quantity': 'mean',
    'Revenue': 'mean'
})
```

### Explanation:
- Groups data product-wise
- Calculates average quantity and revenue

---

# 📌 Important Insights

✔️ Pandas makes sales data analysis simple and efficient.

✔️ GroupBy operations help analyze product and revenue trends.

✔️ Statistical analysis helps understand business performance.

✔️ Date-Time analysis helps identify monthly and daily sales trends.

✔️ Visualization techniques improve understanding of sales patterns.

✔️ Real-world business datasets can be analyzed efficiently using Python.

---

# 📁 Project Structure

```text
├── Sales_Data_Analysis.ipynb
├── Sales_Data.csv
├── README.md
```

---

# 🎯 Final Conclusion

This project demonstrates how Python and Pandas can be used for real-world sales data analysis tasks. Different operations such as data cleaning, removing duplicate records, grouping data, statistical analysis, visualization, and extracting meaningful business insights were successfully implemented.

Through this project, practical understanding was gained in:

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Data Manipulation using Pandas
- Statistical Analysis
- GroupBy Operations
- Revenue Analysis
- Data Visualization
- Python-based Data Analytics

Overall, this project serves as a strong beginner-friendly foundation for learning Data Analysis and Data Science using Python.
