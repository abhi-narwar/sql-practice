# LeetCode 1683 – Invalid Tweets

## 🧩 Problem Statement
You are given a table named **Tweets** that stores tweet information.

### Table: Tweets

| Column Name | Type |
|------------|------|
| tweet_id | int |
| content | varchar |

Each row represents a tweet with its text content.

---

## 🎯 Task
Find the **tweet_id** of tweets where:
- The length of `content` is **strictly greater than 15 characters**

Return the result in **any order**.

---

## ✅ SQL Solution (PostgreSQL)

```sql
SELECT tweet_id
FROM Tweets
WHERE LENGTH(content) > 15;
