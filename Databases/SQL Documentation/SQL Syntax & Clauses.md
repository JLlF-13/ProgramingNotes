### Basic SQL Syntax

```sql
-- Select all users
SELECT * FROM users;

-- Insert a new product
INSERT INTO products (name, price) VALUES ('Laptop', 999);

-- Update an order status
UPDATE orders SET status = 'shipped' WHERE id = 42;

-- Delete a customer
DELETE FROM customers WHERE id = 10;
```


---

### Basic SQL Clauses

#### `WHERE`

Filters rows based on a condition.

```sql
SELECT * FROM users WHERE age > 18;
```

#### `ORDER BY`

Sorts results by one or more columns.

```sql
SELECT * FROM products ORDER BY price DESC;
```

#### `LIMIT`

Restricts the number of rows returned.

```sql
SELECT * FROM orders LIMIT 10;
```

#### `GROUP BY`

Groups rows that share a value in a column — often used with aggregate functions.

```sql
SELECT country, COUNT(*) FROM users GROUP BY country;
```

#### `HAVING`

Filters grouped results (used with `GROUP BY`).

```sql
SELECT country, COUNT(*) FROM users GROUP BY country HAVING COUNT(*) > 100;
```

Tips:
- Use `UPDATE` with caution — always include a `WHERE` clause
    
- Use `DELETE` carefully — without `WHERE`, it removes all rows
    
- Use `TRUNCATE` to quickly empty a table (no rollback)