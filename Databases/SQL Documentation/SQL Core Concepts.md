## Core Concepts

#### Tables
Represent entities (e.g. `users`, `products`, `orders`)  
Each row = one record  
Each column = one attribute

#### Primary Key
Uniquely identifies each row in a table  
Example: `user_id` in a `users` table

#### Foreign Key
Connects rows between tables  
Example: `user_id` in an `orders` table refers to `user_id` in `users`

#### Relationships
- **One-to-One**: each user has one profile  (1-1)
- **One-to-Many**: one user can place many orders  (1-m)
- **Many-to-Many**: products in multiple categories (requires join table) (m-m)