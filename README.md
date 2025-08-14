 🧮 Task 7 - Sales Data Summary using MySQL & Python

This project demonstrates how to:
- Import a CSV file into a MySQL database
- Run SQL queries from Python using SQLAlchemy
- Perform data analysis and visualization using Pandas and Matplotlib

---

 📁 Dataset

The dataset used is `sales_data.csv`, which contains the following columns:

- `product` (Name of the product)
- `quantity` (Units sold)
- `price` (Price per unit)

---

 🧰 Tools & Technologies

- Python
- MySQL Server 
- Pandas
- Matplotlib
- SQLAlchemy
- Jupyter Notebook

---

 ⚙️ Steps Performed

🔹 Step 1: Created MySQL Database and Table

```sql
CREATE DATABASE sales_db;
USE sales_db;

CREATE TABLE sales (
    product VARCHAR(100),
    quantity INT,
    price FLOAT
);
🔹 Step 2: Loaded CSV into MySQL using Python
python
Copy
Edit
import pandas as pd
from sqlalchemy import create_engine

df = pd.read_csv("sales_data.csv")
engine = create_engine("mysql+mysqlconnector://root:your_password@localhost:3306/sales_db")
df.to_sql("sales", con=engine, if_exists='replace', index=False)
🔹 Step 3: Executed SQL Queries from Python
Examples:

Total revenue by product

Average price

Top-selling products

Sales count

Revenue vs quantity

📊 Visualizations Created
Bar chart: Revenue per product

Horizontal bar chart: Quantity sold

Pie chart: Revenue share for top products

Line chart: Sales count per product

Scatter plot: Revenue vs average price

All plots were created using Matplotlib and saved as PNGs.

📁 Files Included
File	Description
sales_data.csv	Input dataset
task7_analysis.ipynb	Jupyter notebook with code and plots
sales_chart.png	Sample output chart
README.md	This file

