# LeetCode 1148 – Article Views I

## 🧩 Problem Statement
You are given a table named **Views** that stores information about article views.

### Table: Views

| Column Name | Type |
|------------|------|
| article_id | int |
| author_id | int |
| viewer_id | int |
| view_date | date |

Each row means:
- An article (`article_id`)
- Written by an author (`author_id`)
- Viewed by a user (`viewer_id`)

---

## 🎯 Task
Find the **authors who viewed their own articles**.

### Output Requirements:
- Return only the **author_id**
- Rename the column as **id**
- Result must be **sorted in ascending order**
- Duplicate values should be removed

---

## ✅ SQL Solution

```sql
SELECT DISTINCT author_id AS id
FROM Views
WHERE author_id = viewer_id
ORDER BY author_id;
