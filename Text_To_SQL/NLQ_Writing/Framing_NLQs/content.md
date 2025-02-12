# Frame the Right Questions

Now that you have a clear idea of the business metrics and data, it’s time to start writing questions for each metric. When training a model to generate SQL queries from natural language, the goal is to create NLQs that challenge the model and push it to learn and improve with each interaction.

To enhance the quality of your queries, incorporate the following strategies:

---

## 1. Relevance and Business Value

Ensure that your query addresses a real business problem or insight. It should be actionable and support decision-making. Additionally, verify that the query can be answered using the available data and schema.

**Example:**

- ❌ *Bad:* "List all products and their sales."
- ✅ *Good:* "What was the total revenue from our top 5 selling products last quarter?"

---

## 2. Clarity and Specificity

Be clear and precise to avoid multiple interpretations. Replace vague terms like *"compare"* or *"analyze"* with specific operations, such as *"calculate the difference between"* or *"determine which is greater."* Your question should be straightforward and easy to understand.

**Example:**

- ❌ *Bad:* "Compare order values in different cities."
- ✅ *Good:* "Calculate the difference in average order amount between customers in New York and Los Angeles."

---

## 3. Avoid Technical References

Use business language instead of technical jargon. Refrain from mentioning specific column names or table structures, unless it involves widely known personal information like email addresses.

**Example:**

- ❌ *Bad:* "Count the orders in the 'orders' table where cust_email = 'john.doe@example.com'."
- ✅ *Good:* "What is the total number of orders placed by the customer with email address john.doe@example.com?"

---

## 4. Eliminate Ambiguity

Make sure each term in your query has a clear and singular meaning. Avoid expressions that require human interpretation and be specific about time periods, categories, or other relevant parameters.

**Example:**

- ❌ *Bad:* "Which sales reps performed well recently?"
- ✅ *Good:* "Which sales representatives exceeded their quarterly targets by more than 10% in Q2 2022?"

---

## 5. Use Proper Language

Grammatical accuracy and clear sentence structure are crucial for a good NLQ. Ensure your queries are written in complete sentences with clear subjects and actions.

**Example:**

- ❌ *Bad:* "Whats the avg time btw 1st n 2nd purchase of customer?"
- ✅ *Good:* "What is the average duration between a customer's first and second purchase?"

---

## 6. Ensure Queryability

Your NLQ should translate into a SQL query that can be executed. Avoid pseudocode or overly technical terms and ensure the language is intuitive.

**Example:**

- ❌ *Bad:* "SELECT TOP 10 customers ORDER BY purchase_amount DESC LIMIT 6 months."
- ✅ *Good:* "List the top 10 customers by total purchase amount in the last 6 months."

---

## 7. Data Exploration

Familiarize yourself with the data tables before writing queries. Ensure the data you need to answer the query is available and accessible.

**Example:**

- ❌ *Bad:* "How many customers bought stuff from different categories?"
- ✅ *Good:* "What percentage of our active customers have made a purchase in each product category?"

---

## 8. Conciseness

Keep your query concise while still ensuring clarity and completeness. Avoid unnecessary details that don’t add value.

**Example:**

- ❌ *Bad:* "Calculate the growth rate of new user signups for each month in the year 2023 compared to the previous month, showing the percentage increase or decrease."
- ✅ *Good:* "What is the month-over-month growth rate of new user signups in 2023?"

---

## 9. Quantifiable Metrics

Be specific when comparing or analyzing data. Always state the exact metrics to be used and use clear terms for calculations such as *"average,"* *"total,"* or *"percentage."*

**Example:**

- ❌ *Bad:* "How loyal are our new users?"
- ✅ *Good:* "What is the 90-day retention rate for users who signed up in January 2023?"

---

## 10. Review and Refine

After writing your query, review it from both a non-technical user and a SQL writer’s perspective. Revise any parts that could be ambiguous or unclear.

**Example:**

- ❌ *Original:* "Which products are popular among young customers?"
- ✅ *Refined:* "Which 5 products have the highest sales volume among customers aged 18-25 in the last 3 months?"

---

This structured guide will help you create high-quality NLQs that are clear, actionable, and effective for SQL generation.
