A **view** is a virtual table based on the result of a SQL query. It doesn’t store data itself, but allows you to reuse complex queries as if they were regular tables.

Why Use Views?
- To simplify complex queries
    
- To hide sensitive columns or logic
    
- To create reusable data layers for applications
    
- To improve readability and maintainability

---

### Creating a View

```sql
CREATE VIEW active_users AS
SELECT id, name, email
FROM users
WHERE status = 'active';
```

Now you can query it like a table:

```sql
SELECT * FROM active_users; 
```

---

### Updating Views

Some views can be **updatable**, meaning you can `INSERT`, `UPDATE`, or `DELETE` data through them — but only if:

- The view is based on a single table
    
- It doesn’t use `GROUP BY`, `DISTINCT`, `JOIN`, or aggregate functions
    

Example of an updatable view:

```sql
CREATE VIEW user_emails AS
SELECT id, email FROM users;
```

You can then update like this:

```sql
UPDATE user_emails SET email = 'new@example.com' WHERE id = 1;
```

---

### Dropping a View

To delete a view you doit like this:

```sql
DROP VIEW active_users;
```

--- 

### Limitations

- Views don’t improve performance by themselves
    
- Complex views can slow down queries if not indexed properly
    
- Not all views are updatable