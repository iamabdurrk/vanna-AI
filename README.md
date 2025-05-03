# 🏢 IT Company Database (companyDB)

This project provides a normalized MySQL database schema for managing the data of an IT company. It covers core components such as companies, departments, employees, projects, clients, salaries, and more.

---

## 📂 Table of Contents

- [Overview](#overview)
- [Database Schema](#database-schema)
- [Table Relationships](#table-relationships)
- [Setup](#setup)
- [Dummy Data](#dummy-data)
- [Sample Queries](#sample-queries)
- [Using Vanna.AI](#using-vannaai)
- [License](#license)

---

## 📌 Overview

This MySQL database is designed to manage key operations of IT companies:
- Employee management
- Project tracking
- Client management
- Salary history
- Asset allocation

You can also connect this schema with **Vanna.AI** to allow natural language to SQL query generation.

---

## 🧱 Database Schema

The database contains the following 8 tables:

| Table             | Description                                         |
|------------------|-----------------------------------------------------|
| `companies`       | Stores company details (name, industry, location)   |
| `departments`     | Departments under each company                      |
| `employees`       | Employee personal and job information               |
| `projects`        | Projects managed by departments                     |
| `clients`         | Clients assigned to companies                       |
| `employee_projects` | Many-to-many relationship of employees to projects |
| `assets`          | Assets assigned to employees                        |
| `salaries`        | Salary and bonus history for employees              |

---

## 🔗 Table Relationships

- A `company` has many `departments`
- A `department` has many `employees` and `projects`
- An `employee` can work on many `projects` (via `employee_projects`)
- A `client` belongs to one `company`
- An `employee` has many `salaries` and may be assigned many `assets`

---

## ⚙️ Setup

1. Create the database:
   ```sql
   CREATE DATABASE companyDB;
   USE companyDB;
More Documentation: https://vanna.ai/docs/mysql-gemini-chromadb/#launch-the-user-interface   
