### Joins Explained

Joins allow you to combine data from multiple tables:

|Type|Description|
|---|---|
|INNER JOIN|Only matching rows from both tables|
|LEFT JOIN|All rows from left + matches from right|
|RIGHT JOIN|All rows from right + matches from left|
|FULL JOIN|All rows from both tables|
Example:
```sql
SELECT users.name, orders.total
FROM users
INNER JOIN orders ON users.id = orders.user_id;
```
