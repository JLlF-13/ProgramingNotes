**MongoDB** is a document-based NoSQL database. It stores data in flexible, JSON-like documents inside collections. Each document can have its own structure, which makes MongoDB ideal for dynamic or nested data.

### Basic Document Structure

```json
{
  "_id": "u123",
  "name": "Alice",
  "age": 30,
  "email": "alice@example.com",
  "isActive": true,
  "tags": ["admin", "editor"],
  "profile": {
    "bio": "Developer",
    "joined": "2023-01-01"
  }
}
```

- Documents are stored in **collections** (similar to tables in SQL)
    
- Each document has a unique `_id` field (automatically generated if not provided)

### Common Operations

#### Insert

```Js
db.users.insertOne({ name: "Alice", age: 30 });
```

#### Find

```Js
db.users.find({ age: { $gt: 25 } });
```

#### Update

```Js
db.users.updateOne(
  { name: "Alice" },
  { $set: { age: 31 } }
);
```

#### Delete
```Js
db.users.deleteOne({ name: "Alice" });
```

---

### Query Operators

|Operator|Description|Example|
|---|---|---|
|`$gt`|Greater than|`{ age: { $gt: 18 } }`|
|`$lt`|Less than|`{ age: { $lt: 65 } }`|
|`$eq`|Equal to|`{ name: { $eq: "Alice" } }`|
|`$ne`|Not equal|`{ status: { $ne: "inactive" } }`|
|`$in`|Matches any in array|`{ role: { $in: ["admin", "user"] } }`|
|`$exists`|Checks if field exists|`{ email: { $exists: true } }`|