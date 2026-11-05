# Analyzing Customer Orders Using Python

**Course-End Project**

A Python project demonstrating how to use core data structures to store, process, and analyze retail customer orders, uncovering spending habits, category revenue, and customer segments without the need for external libraries.

## Business Problem

Retail businesses need to understand who their top spenders are, which product categories drive the most revenue, and how to classify customers based on their buying behavior. This project shows how built-in Python data structures can be used to organize raw order data and surface actionable business insights.

## Dataset

The project uses a hardcoded dataset of customer orders. Each order is stored as a tuple containing the customer's name, the product purchased, the price, and the product category.

**Example Order:**
```python
("Alice", "Television", 120.00, "Electronics")
```

## Tools & Concepts Used

* **Language:** Python 3
* **External Libraries:** None (Pure Python only)
* **Core Data Structures:**
  * **Lists:** Used to store the master list of customer names, order records, and filtered subsets (e.g., electronics customers).
  * **Tuples:** Used to represent each individual order as an immutable record `(name, product, price, category)`.
  * **Dictionaries:** Used for fast lookups and aggregations, such as mapping customers to their orders, mapping products to categories, tracking total spending per customer, and summing revenue by category.
  * **Sets:** Used to automatically deduplicate data (finding unique product categories/products) and to perform operations like finding customers who bought from multiple categories (intersections, unions, differences).

## Project Tasks & Steps

1. **Store Customer Orders:** 
   Created the base list of tuples and converted it into a dictionary grouping all purchases by customer. Practiced safely retrieving, adding, updating, and removing dictionary records.
2. **Classify Products by Category:** 
   Mapped individual products to their broader categories using dictionaries and extracted unique categories using sets.
3. **Analyze Customer Orders:** 
   Calculated the total amount spent by each customer and segmented them into tiers:
   * **High-value buyer:** Spent > $100
   * **Moderate buyer:** Spent $50 - $100
   * **Low-value buyer:** Spent < $50
4. **Generate Business Insights:** 
   Calculated total revenue per product category, identified all unique products sold, filtered for customers who specifically bought electronics, and used sorting to rank the top 3 highest-spending customers.
5. **Organize and Display Data:** 
   Generated a cleanly formatted summary table of customer spending and classifications. Used advanced set operations (intersection `&`, union `|`, difference `-`) to analyze cross-category purchasing behavior.

## Key Insights

* **Top Spenders:** Julia (\$150.00), Alice (\$135.00), and Fiona (\$110.00) were identified as the high-value buyers.
* **Top Category:** Electronics drove the majority of the revenue (\$410.00 out of \$790.00 total).
* **Cross-Selling:** Set intersections revealed that zero customers purchased across multiple categories in this dataset (e.g., no one bought both Electronics and Clothing), highlighting an area where cross-promotional marketing could be introduced.