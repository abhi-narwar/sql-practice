# LeetCode 584 – Find Customer Referee (PostgreSQL)

## 🧩 Problem Statement
You are given a table named **Customer** with the following columns:

| Column Name | Type |
|------------|------|
| id         | int  |
| name       | varchar |
| referee_id | int (nullable) |

Each row represents a customer.  
`referee_id` shows which customer referred them.

### 🎯 Task
Find the **names of customers** whose:
- `referee_id` is **NOT equal to 2**
- OR `referee_id` is **NULL**

---

## ✅ SQL Solution (PostgreSQL)

```sql
SELECT name
FROM Customer
WHERE referee_id IS NULL
   OR referee_id <> 2;

### `<>` Operator in SQL

- `<>` means **NOT EQUAL TO**
- It is used to compare two values and check if they are different