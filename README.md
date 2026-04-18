# Task8-dashboard-
# 📦 Parcel Management System (SQL Project)

## 📌 Project Overview
This project is a **Parcel Management System** designed to manage parcel delivery operations efficiently. It includes database design, SQL queries, and basic reporting features.

---

## 🎯 Features
- Manage parcel details 📦
- Track sender and receiver 👤
- Branch-wise parcel management 🏢
- Parcel status tracking 🚚
- Generate reports using SQL queries 📊

---

## 🗂️ Database Tables
- **customers** – Stores customer details
- **parcel** – Stores parcel information
- **branch** – Stores branch details

---

## 🧠 SQL Queries Included

### 1. Sender & Receiver Details
```sql
SELECT 
    p.parcel_id,
    c1.name AS sender,
    c2.name AS receiver,
    p.status
FROM parcel p
JOIN customers c1 ON p.sender_id = c1.customer_id
JOIN customers c2 ON p.receiver_id = c2.customer_id;
