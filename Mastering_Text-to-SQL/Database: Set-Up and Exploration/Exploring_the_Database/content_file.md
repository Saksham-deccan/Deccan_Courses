# Database Exploration

## Step 1: Understanding Database Schema

A database schema defines how data is organized, including tables, columns, data types, relationships, and constraints. The first step in database exploration is schema discovery.

### 1.1 Listing Tables in the Database

```txt
SHOW TABLES; 
```

### 1.2 Inspecting Table Structure

```txt
DESCRIBE table_name;
```

This reveals:

 ✅ Column names
 ✅ Data types (e.g., VARCHAR, INTEGER, DATE)
 ✅ Constraints (e.g., NOT NULL, PRIMARY KEY, FOREIGN KEY)
 ✅ Default values

## Step 2: Identifying Primary and Foreign Keys

You can check all Foreign Keys using:

```txt
SELECT TABLE_NAME, COLUMN_NAME, REFERENCED_TABLE_NAME, REFERENCED_COLUMN_NAME
FROM INFORMATION_SCHEMA.KEY_COLUMN_USAGE
WHERE TABLE_SCHEMA = 'tpch' AND REFERENCED_TABLE_NAME IS NOT NULL;
```

This helps identify **how tables are linked,** which is crucial for writing JOIN queries.

## Step 3: Exploring Table Contents

**3.1** Checking sample data

```txt
SELECT * FROM table_name LIMIT 10;
```

**3.2** Counting Records in a Table

```txt
SELECT COUNT(*) FROM table_name; 
```

**3.3** Finding Unique Values

```txt
SELECT DISTINCT column_name FROM table_name; 
```

This helps understand **categorical data** like product categories, user roles, or regions.

**3.4** Checking for NULL Values

```txt
SELECT column_name, COUNT(*) FROM table_name WHERE column_name IS NULL;
```

## Step 4: Data Distribution and Statistical Insights

**4.1** Finding Minimum and Maximum Values

```txt
SELECT MIN(column_name), MAX(column_name) FROM table_name;
```

**4.2** Calculating Averages and Medians

```txt
SELECT AVG(column_name) FROM table_name;
```

For a **true median**:

```txt
SELECT column_name FROM table_name ORDER BY column_name LIMIT 1 OFFSET (SELECT COUNT(*)/2 FROM table_name); 
```

**4.3** Detecting Outliers
Outliers can distort analysis. Use standard deviation:

```txt
SELECT column_name, AVG(column_name), STDDEV(column_name) 
FROM table_name;
```

## Step 5: Writing Small Queries to Understand Data

For Example:

```txt
SELECT O_ORDERKEY, O_TOTALPRICE 
FROM ORDERS 
ORDER BY O_TOTALPRICE DESC 
LIMIT 5;
```

Helps understand order values before writing revenue-based NLQs.

or

```txt
SELECT P.P_NAME, SUM(L.L_QUANTITY) AS TotalSold
FROM LINEITEM L
JOIN PART P ON L.L_PARTKEY = P.P_PARTKEY
GROUP BY P.P_NAME
ORDER BY TotalSold DESC
LIMIT 5;
```

Ensures that popular products are identified before writing product sales NLQs.

:::tip
**Why is thorough database exploration important?**
Effective database exploration is fundamental to writing high-quality SQL queries and generating meaningful insights. By systematically examining schema structures, relationships, and data distributions, you can craft precise, efficient business analysis queries.
:::