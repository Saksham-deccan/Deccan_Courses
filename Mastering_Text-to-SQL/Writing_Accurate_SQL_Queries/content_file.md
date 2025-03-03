# Writing Accurate SQL Queries

Now that you’ve crafted your questions, it's time to generate the SQL queries that will extract the relevant information. Writing good SQL queries involves more than just translating the question into SQL—it requires attention to detail and a methodical approach. Let’s break down the key steps to writing quality queries.

## 1. Extract Key Instructions from the NLQ

The first and most important step in writing a SQL query is identifying the critical details from the natural language question (NLQ). This is where many people struggle—they miss important elements that lead to irrelevant or incomplete queries. Make sure to mark all the essential instructions that the NLQ is asking for, so nothing is overlooked.

## 2. Use Meaningful Aliases and CTEs

To improve query readability and maintainability, it’s advisable to use meaningful aliases for tables and columns. Additionally, use Common Table Expressions (CTEs) wherever needed to break down complex logic into simpler, reusable steps.

## 3. Return at Least One Row

An effective query should return at least one row in its output. If your query returns no data, check your logic and ensure that all conditions are correct and aligned with the NLQ.

## 4. SQL Quality Checklist

To ensure the query meets quality standards, follow this checklist:

* **SQL follows NLQ accurately:**
  The query should correctly reflect the natural language question, addressing all its requirements.
* **Logical correctness:**
  Ensure the SQL is logically sound and flows in a structured manner that makes sense.
* **Avoid unnecessary columns:**
  Only include the columns needed for the specific question. Extra columns can clutter results and slow down execution.
* **Include all necessary columns:**
  Make sure every column needed by the NLQ is present in the SELECT statement.
* **Use relevant aliases:**
  All columns in the final SELECT statement should have clear and meaningful aliases to improve readability.
* **Correct use of aggregate functions:**
  Ensure that aggregate functions such as SUM(), AVG(), COUNT(), etc., are used correctly according to the NLQ's requirements.
* **Joins are accurate:**
  Verify that the joins are based on the correct keys and match the corresponding tables. Avoid using joins that are not required.
* **Group by keys, not names:**
  When using GROUP BY, make sure to group by key columns, not names, unless specifically required by the NLQ.
* **Use ORDER BY sparingly:**
  Only use ORDER BY when explicitly requested by the NLQ or if needed to filter top results.
* **Correct sorting order:**
  Ensure the ASC (ascending) or DESC (descending) order aligns with the requirements of the NLQ.