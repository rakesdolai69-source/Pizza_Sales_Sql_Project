# 🍕 SQL Pizza Sales Analysis

This project involves designing and implementing a SQL-based system to analyze pizza sales data. The goal was to extract actionable insights from raw data using advanced SQL queries and data analysis techniques.

## 🔍 Key Insights

- **Comprehensive Sales Tracking:** Designed and implemented a SQL system to track pizza orders and revenue.
- **Metrics Retrieval:** Retrieved key business metrics such as:
  - Total Orders
  - Total Revenue
  - Top-Selling Pizzas
- **Trend Analysis:** Analyzed sales trends over time to uncover peak hours and sales distributions.
- **Customer Preference Insights:** Performed category-wise analysis to understand customer preferences.
- **Performance Metrics:** Evaluated cumulative revenue and performance using window functions and aggregations.

## 🛠 Tech Stack

- **SQL**
- **Data Analysis**
- **Database Design**
- **Query Optimization**

## 📁 Project Structure

├── questions.txt # List of questions and queries used for analysis
├── orders.csv # Contains order timestamps and IDs
├── orderdetails.csv # Order-level details including quantities and pizza types
├── pizza_types.csv # Metadata about each pizza (category, ingredients, etc.)
├── sql_pizza.pdf # Presentation of the pizza sales analysis (PDF format)


## 🧠 Learnings

- Writing efficient and optimized SQL queries for large datasets
- Leveraging JOINs, GROUP BY, CTEs, and window functions for deep data exploration
- Applying data analysis techniques to drive business insights

📬 Contact
Feel free to reach out if you have any questions or feedback!

## 📊 Sample Queries

```sql
-- Top 5 best-selling pizzas
SELECT pizza_name, SUM(quantity) AS total_sold
FROM order_details
JOIN pizzas ON order_details.pizza_id = pizzas.pizza_id
GROUP BY pizza_name
ORDER BY total_sold DESC
LIMIT 5;
