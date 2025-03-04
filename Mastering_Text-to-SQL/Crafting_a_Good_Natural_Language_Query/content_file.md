# Crafting Effective NLQs

Crafting effective NLQs is an art where creativity meets precision. Your goal is to simulate the types of questions real-world users would ask a model. Let’s break down the process step by step to help you write strong, business-focused queries.

<img height="329" width="602" src="${PRIVATE_IMAGE_INTRO_3}" />

## 1. Understand the Database

The foundation of any good NLQ is a deep understanding of the database you're working with. Take time to explore all the tables and columns, running small queries to grasp how the data is structured and how it reflects the business's core functions. This will help you understand the nuances of the data, enabling you to craft more accurate and relevant questions.

## 2. Identify Key Business Metrics

Once you’ve familiarized yourself with the database, the next step is to list the business metrics that someone might be interested in. These metrics should align with the company’s goals. For example, if the business is an e-commerce seller, focus on key metrics like:

* Order delays
* Maximum returns
* Customer retention rates

*Avoid focusing on metrics that don't directly contribute to business insights, such as "customer names" or "maximum orders" without context.*

## 3. Frame the Right Questions

Now that you have a clear idea of the business metrics and data, it’s time to start writing questions for each metric. Here’s how you should approach framing your questions. When training a model to generate SQL queries from natural language, the goal is to create NLQs that challenge the model and push it to learn and improve with each interaction.

To enhance the quality of your queries, incorporate the following strategies:

### 3.1 Relevance and Business Value

Ensure that your query addresses a real business problem or insight. It should be actionable and support decision-making. Additionally, verify that the query can be answered using the available data and schema.

**Example:**

:::danger
❌ **Bad:** "List all products and their sales."
:::

:::info
✅ **Good:** "What was the total revenue from our top 5 selling products last quarter?"
:::

### 3.2 Clarity and Specificity

Be clear and precise to avoid multiple interpretations. Replace vague terms like "compare" or "analyze" with specific operations, such as "calculate the difference between" or "determine which is greater." Your question should be straightforward and easy to understand.

**Example:**

:::danger
❌ **Bad:** "Compare order values in different cities."
:::

:::info
✅ **Good:** "Calculate the difference in average order amount between customers in New York and Los Angeles."
:::

### 3.3 Avoid Technical References

Use business language instead of technical jargon. Refrain from mentioning specific column names or table structures, unless it involves widely known personal information like email addresses.

**Example:**

:::danger
❌ **Bad:** "Count the orders in the 'orders' table where cust\_email = 'john.doe@example.com'."
:::

:::info
✅ **Good:** "What is the total number of orders placed by the customer with email address john.doe@example.com?"
:::

### 3.4 Eliminate Ambiguity

Make sure each term in your query has a clear and singular meaning. Avoid expressions that require human interpretation and be specific about time periods, categories, or other relevant parameters.

**Example:**

:::danger
❌ **Bad:** "Which sales reps performed well recently?"
:::

:::info
✅ **Good:** "Which sales representatives exceeded their quarterly targets by more than 10% in Q2 2022?"
:::

### 3.5 Use Proper Language

Grammatical accuracy and clear sentence structure are crucial for a good NLQ. Ensure your queries are written in complete sentences with clear subjects and actions.

**Example:**

:::danger
❌ **Bad:** "Whats the avg time btw 1st n 2nd purchase of customer?"
:::

:::info
✅ **Good:** "What is the average duration between a customer's first and second purchase?"
:::

### 3.6 Ensure Queryability

Your NLQ should translate into a SQL query that can be executed. Avoid pseudocode or overly technical terms and ensure the language is intuitive.

**Example:**

:::danger
❌ **Bad:** "SELECT TOP 10 customers ORDER BY purchase\_amount DESC LIMIT 6 months."
:::

:::info
✅ **Good:** "List the top 10 customers by total purchase amount in the last 6 months."
:::

### 3.7 Data Exploration

Familiarize yourself with the data tables before writing queries. Ensure the data you need to answer the query is available and accessible.

**Example:**

:::danger
❌ **Bad:** "How many customers bought stuff from different categories?"
:::

:::info
✅ **Good:** "What percentage of our active customers have made a purchase in each product category?"
:::

### 3.8 Conciseness

Keep your query concise while still ensuring clarity and completeness. Avoid unnecessary details that don’t add value.

**Example:**

:::danger
❌ **Bad:** "Calculate the growth rate of new user signups for each month in the year 2023 compared to the previous month, showing the percentage increase or decrease."
:::

:::info
✅ **Good:** "What is the month-over-month growth rate of new user signups in 2023?"
:::

### 3.9 Quantifiable Metrics

Be specific when comparing or analyzing data. Always state the exact metrics to be used and use clear terms for calculations such as "average," "total," or "percentage."

**Example:**

:::danger
❌ **Bad:** "How loyal are our new users?"
:::

:::info
✅ **Good:** "What is the 90-day retention rate for users who signed up in January 2023?"
:::

### 3.10 Review and Refine

After writing your query, review it from both a non-technical user and a SQL writer’s perspective. Revise any parts that could be ambiguous or unclear.

**Example:**

:::danger
❌ **Original:** "Which products are popular among young customers?"
:::

:::info
✅ **Refined:** "Which 5 products have the highest sales volume among customers aged 18-25 in the last 3 months?"
:::