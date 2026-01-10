# 🟢 LeetCode 1757 – Recyclable and Low Fat Products

## 📌 Problem Overview
We are given a table **Products** that stores information about products and whether they are:
- Low fat
- Recyclable

Our task is to **find the product IDs** of products that are **both low fat AND recyclable**.

---

## 🗂 Table Structure

**Table: Products**

| Column Name | Type | Description |
|------------|------|-------------|
| product_id | INT | Unique product identifier |
| low_fats | ENUM('Y','N') | 'Y' → Low fat, 'N' → Not low fat |
| recyclable | ENUM('Y','N') | 'Y' → Recyclable, 'N' → Not recyclable |

---

## 🎯 Requirement
Return the `product_id` of products where:
- `low_fats = 'Y'`
- `recyclable = 'Y'`

Order of result **does not matter**.

---

## 🧪 Example

### Input:
| product_id | low_fats | recyclable |
|-----------|----------|------------|
| 0 | Y | N |
| 1 | Y | Y |
| 2 | N | Y |
| 3 | Y | Y |
| 4 | N | N |

### Output:
| product_id |
|-----------|
| 1 |
| 3 |

### Explanation:
Only products **1** and **3** satisfy both conditions.

---

## ✅ SQL Solution

```sql
SELECT product_id
FROM Products
WHERE low_fats = 'Y'
  AND recyclable = 'Y';


## 📘 ENUM in SQL (Easy Explanation)

**ENUM** SQL ka ek **data type** hota hai jo kisi column ko **sirf fixed (predefined) values** store karne deta hai.

Matlab:
> Column me sirf wahi values aa sakti hain jo pehle se define ki gayi ho.

---

### 🔹 Syntax
```sql
ENUM('value1', 'value2', 'value3')

low_fats ENUM('Y', 'N')

Iska matlab:

'Y' → Yes / True

'N' → No / False

Iske alawa koi value allowed nahi hogi