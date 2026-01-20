# 🆔 LeetCode 1378 – Replace Employee ID With The Unique Identifier

## 📌 Problem Statement

You are given two tables:

### **Employees**
| Column Name | Type |
|------------|------|
| id | int |
| name | varchar |

### **EmployeeUNI**
| Column Name | Type |
|------------|------|
| id | int |
| unique_id | int |

Each row in `Employees` contains the employee's name and ID.  
Each row in `EmployeeUNI` contains the employee's ID and their unique identifier.

---

## 🎯 Task

Write an SQL query to show the **unique_id** of each user and their **name**.

- If an employee does **not** have a unique identifier, return **NULL**.
- The result table can be returned in **any order**.

---

## 🧠 Approach

- Use **LEFT JOIN**
- Because we want **all employees**, even if they do not have a matching `unique_id`.

---

## ✅ SQL Solution (PostgreSQL / MySQL)

```sql
SELECT eu.unique_id, e.name
FROM Employees e
LEFT JOIN EmployeeUNI eu
ON e.id = eu.id;
