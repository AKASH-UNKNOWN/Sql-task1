
🛒 E-commerce SQL Database Project

📋 Overview
This project represents a simplified e-commerce database system built using PostgreSQL. It demonstrates core SQL concepts like database creation, table design, data relationships, normalization, and ER modeling.

🧱 Entities and Their Descriptions

| Table       | Description                              |
|-------------|------------------------------------------|
| Customer    | Stores customer details                  |
| Category    | Organizes products into categories       |
| Product     | Stores product information               |
| Orders      | Records customer orders                  |
| OrderItem   | Junction table for orders and products   |
| Payment     | Stores payment details for orders        |
| Shipping    | Records shipping information per order   |

🔑 Relationships
- Customer - Orders: One-to-many
- Order - OrderItem: One-to-many
- Product - OrderItem: One-to-many
- Category - Product: One-to-many
- Order - Payment: One-to-one
- Order - Shipping: One-to-one

🧾 SQL Features Used
- CREATE TABLE, PRIMARY KEY, FOREIGN KEY
- SERIAL (for auto-incremented IDs)
- REFERENCES (to define relationships)
- Normalized schema design (3NF)

💾 Sample SQL Queries

-- Select all products
SELECT * FROM Product;

-- Get all orders by a customer
SELECT * FROM Orders WHERE CustomerID = 1;

-- Join orders with products and quantities
SELECT o.OrderID, p.Name, oi.Quantity
FROM Orders o
JOIN OrderItem oi ON o.OrderID = oi.OrderID
JOIN Product p ON p.ProductID = oi.ProductID;

🗂️ Files Included

| File              | Description                            |
|-------------------|----------------------------------------|
| ecommerce_schema.sql | SQL script to create full database schema |
| ER_diagram.png       | Entity Relationship Diagram image     |
| README.md            | Project description and documentation  |

📌 Tools Used
- PostgreSQL
- pgAdmin / psql CLI
- ER diagram created using dbdiagram.io / Lucidchart

🚀 How to Run

1. Open your PostgreSQL environment
2. Run ecommerce_schema.sql to create the schema
3. Insert sample data if needed
4. Use SELECT, JOIN, INSERT, UPDATE queries to interact with the data

📷 ER Diagram
(Refer to ER_diagram.png in the repo)

📬 Contact
Created by Akash Kumar  
For SQL Developer Internship Task 1
