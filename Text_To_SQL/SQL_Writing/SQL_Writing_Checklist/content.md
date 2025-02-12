# SQL Quality Checklist ✅

To ensure the query meets quality standards, follow this checklist:

---

## 1. SQL Follows NLQ Accurately 🎯
- The query should **correctly reflect the natural language question** (NLQ), addressing all its requirements.

---

## 2. Logical Correctness ✅
- Ensure the SQL is **logically sound** and flows in a structured manner that makes sense.

---

## 3. Avoid Unnecessary Columns 🗑️
- Only include the **columns needed** for the specific question.
- Extra columns can clutter results and **slow down execution**.

---

## 4. Include All Necessary Columns 📌
- Make sure **every required column** from the NLQ is present in the `SELECT` statement.

---

## 5. Use Relevant Aliases 🏷️
- All columns in the final `SELECT` statement should have **clear and meaningful aliases** to improve readability.

---

## 6. Correct Use of Aggregate Functions 📊
- Ensure aggregate functions like `SUM()`, `AVG()`, `COUNT()`, etc., are **used correctly** according to the NLQ's requirements.

---

## 7. Joins Are Accurate 🔗
- Verify that joins are **based on the correct keys** and match the corresponding tables.
- **Avoid unnecessary joins** that are not required.

---

## 8. Group by Keys, Not Names 🔑
- When using `GROUP BY`, make sure to **group by key columns**, not names, unless specifically required by the NLQ.

---

## 9. Use ORDER BY Sparingly 📉
- Only use `ORDER BY` when explicitly requested by the NLQ or **if needed to filter top results**.

---

## 10. Correct Sorting Order ⬆️⬇️
- Ensure `ASC` (ascending) or `DESC` (descending) **aligns with the NLQ's requirements**.

---

Following these best practices will help you write **efficient, accurate, and maintainable SQL queries**. 🚀
