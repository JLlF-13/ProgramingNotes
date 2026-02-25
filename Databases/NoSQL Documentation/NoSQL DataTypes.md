NoSQL databases don’t use strict schemas, but data types still matter.

> Yes ther are identic or very similar to SQL Data Types
#### Data Types
- `String`: `"hello"`
- `Number`: `42`, `3.14`
- `Boolean`: `true`, `false`
- `Array`: `[1, 2, 3]`
- `Object`: `{ name: "Alice", age: 30 }`
- `Date`: `ISODate("2023-01-01")`
- `Null`: `null`
- `ObjectId`: Unique ID for documents

#### Notes
- You don’t need to declare types in advance
- MongoDB infers types from inserted data
- Arrays and nested objects are very common