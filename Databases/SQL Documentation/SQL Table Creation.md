#### Creating Tables

```sql
CREATE TABLE users (
  id INT PRIMARY KEY,
  name VARCHAR(100) NOT NULL,
  email VARCHAR(255) UNIQUE,
  age INT DEFAULT 18
);
```

**NOT NULL** → the column must have a value (default NULL)
**UNIQUE** → no duplicate values allowed
**DEFAULT** → sets a default value if none is provided 
**AUTO_INCREMENT** (MySQL) or `SERIAL` (PostgreSQL) → for automatic ID generation