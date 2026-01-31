# 🍔 Food Delivery Data Integration & Analysis

## 📌 Overview
This project demonstrates how to integrate and clean data from **multiple file formats (CSV, JSON, SQL)** using **Microsoft Excel Power Query**, and generate a **single final dataset** for analysis.

The final dataset is used to analyze:
- User behavior
- Restaurant performance
- Revenue trends
- Membership impact (Gold vs Regular)

---

## 📁 Dataset Files
| File | Format | Description |
|-----|--------|-------------|
| orders.csv | CSV | Transactional order data |
| users.json | JSON | User master data |
| restaurants.sql | SQL | Restaurant master data |
| final_food_delivery_dataset.csv | CSV | Final merged dataset |

---

## 🛠 Tools & Technologies
- Microsoft Excel
- Power Query Editor

---

## 🔄 Data Processing Steps

### 1. Load Orders Data
- Import `orders.csv` using **Data → Get Data → From Text/CSV**

### 2. Load Users Data
- Import `users.json` using **Data → Get Data → From JSON**
- Convert JSON to table and expand columns

### 3. Load Restaurants Data
- Paste SQL `INSERT` statements from `restaurants.sql` into Excel
- Use Power Query to:
  - Split columns by delimiter
  - Remove SQL keywords using Replace Values
  - Clean and format columns

---

## 🔗 Data Integration

### Join Conditions
- `orders.user_id` → `users.user_id`
- `orders.restaurant_id` → `restaurants.restaurant_id`

### Join Type
- **Left Outer Join** (to retain all orders)

---

## 📊 Final Dataset
The final dataset includes:
- Order details
- User information
- Restaurant information

**Output File**
