# SQL Quality Checklist

To ensure the query meets quality standards, follow the checklist as discussed in the video below:

<iframe src="${PRIVATE_SQL_CHECKLIST}"
        width="800"
        height="450"
        frameborder="0"
        allowfullscreen>
</iframe>



## <span style="color:#364BC9"> 1. SQL Follows NLQ Accurately </span>
- The query should **correctly reflect the natural language question** (NLQ), addressing all its requirements.


## <span style="color:#364BC9"> 2. Logical Correctness </span>
- Ensure the SQL is **logically sound** and flows in a structured manner that makes sense.


## <span style="color:#364BC9"> 3. Avoid Unnecessary Columns </span>
- Only include the **columns needed** for the specific question.
- Extra columns can clutter results and **slow down execution**.


## <span style="color:#364BC9"> 4. Include All Necessary Columns </span>
- Make sure **every required column** from the NLQ is present in the `SELECT` statement.


## <span style="color:#364BC9"> 5. Use Relevant Aliases </span>
- All columns in the final `SELECT` statement should have **clear and meaningful aliases** to improve readability.


## <span style="color:#364BC9"> 6. Correct Use of Aggregate Functions </span>
- Ensure aggregate functions like `SUM()`, `AVG()`, `COUNT()`, etc., are **used correctly** according to the NLQ's requirements.


## <span style="color:#364BC9"> 7. Joins Are Accurate </span>
- Verify that joins are **based on the correct keys** and match the corresponding tables.
- **Avoid unnecessary joins** that are not required.


## <span style="color:#364BC9"> 8. Group by Keys, Not Names </span>
- When using `GROUP BY`, make sure to **group by key columns**, not names, unless specifically required by the NLQ.


## <span style="color:#364BC9"> 9. Use ORDER BY Sparingly </span>
- Only use `ORDER BY` when explicitly requested by the NLQ or **if needed to filter top results**.


## <span style="color:#364BC9"> 10. Correct Sorting Order </span>
- Ensure `ASC` (ascending) or `DESC` (descending) **aligns with the NLQ's requirements**.
