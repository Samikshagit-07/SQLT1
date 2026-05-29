# SQLT1# SQL Developer Internship - Task 1: Database Setup and Schema Design

## 📌 Project Overview
This repository contains the deliverables for **Task 1: Database Setup and Schema Design** as part of the SQL Developer Internship at Elevate Labs[cite: 1]. The objective of this task is to design a well-structured, normalized database schema, implement it using standard Data Definition Language (DDL), establish relational constraints, and visually map the architecture using an Entity-Relationship (ER) Diagram[cite: 1].

For this assignment, an **E-Commerce Platform** domain was chosen to demonstrate concepts of data integrity, normalization, and relational structuring.

---

## 🛠️ Tools Used
* **Database Engine & GUI:** MySQL Server (v8.0.46) & MySQL Workbench (v8.0.47)
* **Design Methodology:** Enhanced Entity-Relationship (EER) Reverse Engineering
* **Documentation:** Markdown (`README.md`)

---

## 📂 Repository Structure
* `SQLT1.sql` - The production-ready SQL script containing the database and table creation queries[cite: 1].
* `sqlt1.png` - The auto-generated Entity-Relationship Diagram showing table connections[cite: 1].
* `README.md` - Documentation detailing the database architecture and conceptual assignment questions.

---

## 📐 Database Architecture & Design
The schema is designed around 4 primary entities, fully normalized to remove data redundancy and ensure transactional integrity:

1. **`users`**: Stores client profile information with strict unique email constraints.
2. **`products`**: Maintains inventory data with numerical validation checks on pricing and stock levels.
3. **`orders`**: Tracks individual customer transactions, mapping a **One-to-Many (1:N)** relationship with the `users` table via foreign keys.
4. **`order_items`**: Functions as a **Bridge Table** to resolve the **Many-to-Many (M:N)** relationship between orders and products. It utilizes cascading deletes (`ON DELETE CASCADE`) to keep dependent records clean.

