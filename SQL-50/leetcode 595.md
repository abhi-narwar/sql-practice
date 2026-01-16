# LeetCode 595 – Big Countries

## 🧩 Problem Statement
You are given a table named **World** that contains information about different countries.

### Table: World

| Column Name | Type |
|------------|------|
| name | varchar |
| continent | varchar |
| area | int |
| population | int |
| gdp | bigint |

---

## 🎯 Task
A country is considered **big** if:

- Its **area is greater than or equal to 3,000,000**, **OR**
- Its **population is greater than or equal to 25,000,000**

Return the following columns:
- `name`
- `population`
- `area`

---

## ✅ SQL Solution

```sql
SELECT name, population, area
FROM World
WHERE area >= 3000000
   OR population >= 25000000;
