A **database** is a structured system used to store and manage data efficiently. Instead of saving information in random files or spreadsheets, a database organizes data into **tables** that are easy to query, update, and relate to each other.

Each **table** contains **rows** (also called records) and **columns** (fields). For example, a `users` table might have columns like `id`, `name`, and `email`, and each row would represent one user.

Databases are especially useful when:

- You need to store large amounts of data (e.g. thousands of users or products)
    
- You want to search or filter data quickly (e.g. find all users from Spain)
    
- You need to maintain relationships between data (e.g. users and their orders)
    

Most modern applications use databases behind the scenes — websites, mobile apps, business software, etc.

---
## DDL & DML

#### DDL
DDL or Data Definition Language, refers to SQL commands usd to create, modify and delete database structures such as tables, indexes and views

#### DML
DML or Data Manipulation Language, refers to SQL commands used to insert, update, delete data wthitin the database

---
## Types of Databases

There are many kinds of databases, but the two most common types you'll encounter when learning programming are:

#### [[Relational Databases (SQL)]]

Relational databases store data in **tables** with predefined **schemas**. Each table has rows and columns, and tables can be linked together using **keys** (like `user_id` or `product_id`). This structure is ideal for data that fits into a consistent format.

- Uses **Structured Query Language (SQL)** to interact with data
    
- Good for structured, predictable data
    
- Supports relationships between tables (e.g. users and their orders)
    
- Examples: **MySQL**, **PostgreSQL**, **SQLite**, **SQL Server**

---

#### [[NoSQL Databases]]

NoSQL databases are designed for **flexibility** and **scalability**. They don’t require a fixed schema and can store data in formats like **JSON**, **key-value pairs**, or **documents**. They’re great for handling large volumes of unstructured or semi-structured data.

- Doesn’t use SQL (though some support SQL-like queries)
    
- Ideal for dynamic or hierarchical data
    
- Scales easily across multiple servers
    
- Examples: **MongoDB**, **Cassandra**, **Redis**, **Firebase**

--- 

## SQL vs NoSQL

Relational (SQL) and non-relational (NoSQL) databases serve different purposes and are optimized for different types of data and workloads. Here's a comparison to help you understand their strengths and differences.
#### General Comparison

| Feature        | SQL (Relational) | NoSQL (Non-relational)     |
| -------------- | ---------------- | -------------------------- |
| Schema         | Fixed            | Flexible or none           |
| Relationships  | Strong (joins)   | Limited or manual          |
| Scalability    | Vertical         | Horizontal                 |
| Query Language | SQL              | Varies (MongoQL, etc.)     |
| Best For       | Structured data  | Unstructured, dynamic data |
#### Practical Concepts

|Concept|MongoDB (NoSQL)|SQL (Relational)|
|---|---|---|
|Data unit|Document|Row|
|Container|Collection|Table|
|Structure|Flexible|Fixed schema|
|Relationships|Embedded or manual|Foreign keys|
### Summary

- **SQL** is ideal when your data is highly structured and relationships are complex.
    
- **NoSQL** is better when your data changes often, is nested, or needs to scale horizontally.
    
- MongoDB allows embedding related data directly inside documents, while SQL uses foreign keys and joins to link tables.