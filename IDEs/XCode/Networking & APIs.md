Networking in iOS is typically handled using **URLSession**, **async/await**, or third‑party libraries like **Alamofire**.

---

### Core Concepts

#### **1. URLSession**

Foundation’s built‑in networking API:

```swift
let url = URL(string: "https://api.example.com/data")!
let (data, _) = try await URLSession.shared.data(from: url)
```

#### **2. Codable**

Easily decode JSON into Swift structs:

```swift
struct User: Codable {
    let id: Int
    let name: String
}
```

#### **3. Async/Await**

Modern concurrency for cleaner networking code:

```swift 
let user = try await fetchUser()
```

#### **4. Error Handling**

Use `do/catch` to manage failures:

```swift 
do {
    let result = try await fetchData()
} catch {
    print("Request failed:", error)
}
```

#### **5. Third‑Party Tools**

- **Alamofire** – Simplified networking
    
- **Moya** – API abstraction layer
    
- **Firebase** – Realtime DB, Auth, Analytics