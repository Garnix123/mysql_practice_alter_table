🛠 MySQL ALTER TABLE Practice – Little Lemon
📌 Project Overview

Practice altering and restructuring the FoodOrders table in the little_lemon database to enforce keys, constraints, and schema changes. 

Exercises covered:

Make OrderID the PRIMARY KEY. 

Enforce NOT NULL on Quantity and Cost. 

Add OrderDate (DATE) and CustomerID (INT) with a FOREIGN KEY to Customers(CustomerID). 

Drop OrderDate. 

Rename Order_status → DeliveryStatus (in OrderStatus). 

Rename table FoodOrders → OrderDeliveryStatus. 

🧑‍🍳 Industry Context

Little Lemon is a restaurant that needs accurate order records and valid customer references across tables. The schema changes above harden data integrity and prepare the orders table for reporting and analytics. 

🖼 Final Table Structure (after tasks)
Column Name	Data Type	Constraints
OrderID	INT	PRIMARY KEY, NOT NULL
Quantity	INT	NOT NULL
Cost	DECIMAL(4,2)	NOT NULL
CustomerID	INT	FOREIGN KEY → Customers(CustomerID) (added)

Derived from the ALTER steps and original table definition. 

🧩 Notes

The script uses ALTER TABLE FoodOrders, MODIFY ... (with a comma). In MySQL, drop the comma:
ALTER TABLE FoodOrders MODIFY OrderID INT PRIMARY KEY; 

💎 MySQL ALTER TABLE Practice – Mangata & Gallo
📌 Project Overview

Create and refine a Staff table for the Mangata_Gallo database: define keys, enforce nullability, add a role column, and remove an unneeded column. 

Exercises covered:

Create Staff_2 (StaffID, FullName, PhoneNumber), with StaffID as PRIMARY KEY. 

Apply constraints: StaffID INT PRIMARY KEY, FullName VARCHAR(...), PhoneNumber INT NOT NULL. 

Add Role VARCHAR(50) NOT NULL to Staff. 

Drop PhoneNumber from Staff. 

🏢 Industry Context

Mangata & Gallo is a luxury jewelry brand; clean staff data (IDs, names, roles) supports scheduling, payroll, and access control while preventing incomplete records. 

🖼 Final Table Structure (after tasks)
Column Name	Data Type	Constraints
StaffID	INT	PRIMARY KEY, NOT NULL
FullName	VARCHAR(100)	NOT NULL
Role	VARCHAR(50)	NOT NULL

Built from create + alter steps shown in the script. 

🧩 Notes

Your ALTER TABLE Staff_2 ... changes FullName to VARCHAR(255) in Task 2; the create step used VARCHAR(100). Keep whichever your rubric expects. 

Tasks 3–4 target table Staff, while the earlier steps use Staff_2. If you intended to keep working on the same table, use Staff_2 consistently (or rename). 

🎯 Key Learning Outcomes

Practiced ALTER TABLE to add, modify, and drop columns and constraints. 

Enforced primary, foreign, and nullability rules to improve data integrity. 

Identified small syntax gotchas (commas, table/column targets) common in schema-migration scripts. 
