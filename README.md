# 🛠 MySQL ALTER TABLE Practice – Little Lemon

## 📌 Project Overview
This project focuses on altering and restructuring the **FoodOrders** table in the `little_lemon` database.  
It demonstrates how to use `ALTER TABLE` to enforce constraints, add relationships, and rename columns/tables.

The exercises cover:
- **Primary keys** – enforce unique identifiers
- **Domain constraints** – apply `NOT NULL`
- **Referential integrity** – use `FOREIGN KEY`
- **Schema changes** – drop and rename columns and tables

---

## 🧑‍🍳 Industry Context
**Little Lemon** is a Mediterranean restaurant that requires accurate order records.  
The database ensures that:
- Every order is uniquely identifiable.  
- No record can contain missing or invalid values.  
- Orders are properly linked to customers.

---

## 🖼 Tables Created & Constraints Applied

### **1. FoodOrders Table**
**Purpose:** Manage customer orders with enforced constraints.  

| Column Name | Data Type     | Constraints                          |
|-------------|---------------|--------------------------------------|
| OrderID     | INT           | PRIMARY KEY, NOT NULL                |
| Quantity    | INT           | NOT NULL                             |
| Cost        | DECIMAL(4,2)  | NOT NULL                             |
| CustomerID  | INT           | FOREIGN KEY → Customers(CustomerID)  |

---

### **2. OrderStatus → OrderDeliveryStatus Table**
**Purpose:** Track delivery status of orders.  

| Column Name    | Data Type    | Constraints |
|----------------|-------------|-------------|
| DeliveryStatus | VARCHAR(15) | NOT NULL    |

---

## 🎯 Key Learning Outcomes
- Declared **primary keys** and enforced **NOT NULL**.  
- Used `ALTER TABLE` to add, modify, and drop columns.  
- Applied **foreign keys** for relational integrity.  
- Renamed columns and tables for clarity.  

---

# 💎 MySQL ALTER TABLE Practice – Mangata & Gallo

## 📌 Project Overview
This project involves creating and modifying the **Staff** table in the `Mangata_Gallo` database.  
The exercises apply constraints, add new attributes, and remove unnecessary ones.

The exercises cover:
- **Primary keys** – uniquely identify staff members
- **Domain constraints** – apply `NOT NULL`
- **Schema updates** – add a role column, drop unused fields

---

## 🏢 Industry Context
**Mangata & Gallo** is a luxury jewelry company requiring reliable staff records.  
The database ensures that:
- Every staff member is uniquely identifiable.  
- Roles are clearly defined.  
- Redundant columns are removed.

---

## 🖼 Tables Created & Constraints Applied

### **1. Staff Table**
**Purpose:** Maintain accurate staff records.  

| Column Name | Data Type     | Constraints          |
|-------------|--------------|----------------------|
| StaffID     | INT          | PRIMARY KEY, NOT NULL|
| FullName    | VARCHAR(100) | NOT NULL             |
| Role        | VARCHAR(50)  | NOT NULL             |

---

## 🎯 Key Learning Outcomes
- Practiced `ALTER TABLE` with `MODIFY`, `ADD`, and `DROP`.  
- Enforced essential constraints for data accuracy.  
- Learned how to evolve schema design as business requirements change.
