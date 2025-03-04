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

<img height="329" width="602" src="${PRIVATE_IMAGE_INTRO_4}" />



:::tip
&#x20;  ✅**SQL follows NLQ accurately:**
&#x20;         The query should correctly reflect the natural language question, addressing all its requirements.
&#x20;  ✅**Logical correctness:**
&#x20;         Ensure the SQL is logically sound and flows in a structured manner that makes sense.
&#x20;  ✅**Avoid unnecessary columns:**
&#x20;        Only include the columns needed for the specific question. Extra columns can clutter results and slow down execution.
&#x20;  ✅**Include all necessary columns:**
&#x20;         Make sure every column needed by the NLQ is present in the SELECT statement.
&#x20;  ✅**Use relevant aliases:**
&#x20;         All columns in the final SELECT statement should have clear and meaningful aliases to improve readability.
&#x20;  ✅**Correct use of aggregate functions:**
&#x20;         Ensure that aggregate functions such as SUM(), AVG(), COUNT(), etc., are used correctly according to the NLQ's requirements.
&#x20;  ✅**Joins are accurate:**
&#x20;         Verify that the joins are based on the correct keys and match the corresponding tables. Avoid using joins that are not required.
&#x20;  ✅**Group by keys, not names:**
&#x20;         When using GROUP BY, make sure to group by key columns, not names, unless specifically required by the NLQ.
&#x20;  ✅**Use ORDER BY sparingly:**
&#x20;         Only use ORDER BY when explicitly requested by the NLQ or if needed to filter top results.
&#x20;  ✅**Correct sorting order:**
&#x20;         Ensure the ASC (ascending) or DESC (descending) order aligns with the requirements of the NLQ.

&#x20;   ✅**SQL follows NLQ accurately:**
&#x20;          The query should correctly reflect the natural language question, addressing all its requirements.
&#x20;   ✅**Logical correctness:**
&#x20;          Ensure the SQL is logically sound and flows in a structured manner that makes sense.
&#x20;   ✅**Avoid unnecessary columns:**
&#x20;          Only include the columns needed for the specific question. Extra columns can clutter results and slow down execution.
&#x20;   ✅**Include all necessary columns:**
&#x20;          Make sure every column needed by the NLQ is present in the SELECT statement.
&#x20;   ✅**Use relevant aliases:**
&#x20;          All columns in the final SELECT statement should have clear and meaningful aliases to improve readability.
&#x20;   ✅**Correct use of aggregate functions:**
&#x20;          Ensure that aggregate functions such as SUM(), AVG(), COUNT(), etc., are used correctly according to the NLQ's requirements.
&#x20;   ✅**Joins are accurate:**
&#x20;          Verify that the joins are based on the correct keys and match the corresponding tables. Avoid using joins that are not required.
&#x20;   ✅**Group by keys, not names:**
&#x20;          When using GROUP BY, make sure to group by key columns, not names, unless specifically required by the NLQ.
&#x20;   ✅**Use ORDER BY sparingly:**
&#x20;          Only use ORDER BY when explicitly requested by the NLQ or if needed to filter top results.
&#x20;   ✅**Correct sorting order:**
&#x20;          Ensure the ASC (ascending) or DESC (descending) order aligns with the requirements of the NLQ.
:::