# Task1
Database Setup and Schema Design

# 📚 Library Management System – Database Schema Design

## 📌 Task 1: Database Setup and Schema Design

### 🎯 Objective
The goal of this task is to design a well-structured relational database by:
- Creating a database and tables
- Defining primary and foreign keys
- Establishing entity relationships
- Generating an Entity-Relationship (ER) Diagram

### 🛠️ Tools Used
- [MySQL Workbench]
- - SQL (MySQL Syntax)
- Git & GitHub for version control

---

## 🧠 Domain: Library Management System

A Library Management System keeps track of books, members, staff, and book loans.

---

## 🔍 Step-by-Step Breakdown

### 1. **Entities Identified**
- **Authors**
- **Categories**
- **Books**
- **Members**
- **Staff**
- **Loans**

### 2. **Relationships**
- One author can write many books (1:N)
- One book belongs to one category (1:1)
- One member can borrow many books (1:N via Loans)
- Each loan is handled by a staff member

---

## 🗃️ Database Schema – SQL Script

sql:
CREATE TABLE members (
    member_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100) NOT NULL
);


Here, member_id is the primary key.

CREATE TABLE loans (
    loan_id INT AUTO_INCREMENT PRIMARY KEY,
    member_id INT,
    FOREIGN KEY (member_id) REFERENCES members(member_id)
);

member_id in loans is a foreign key.

It must match a value in members.member_id






