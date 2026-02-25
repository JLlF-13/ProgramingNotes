
### File & FileWriter

`File`:  Represents a path to a file or directory. It doesn’t read or write data—it just points to the location.

```java
 File file = new File("document.txt");
```

> If you provide a path like `C:\Users`, you can iterate through its contents. For each item, check with `.isDirectory()` or `.isFile()` to know if it's a folder or a file, and more...

`FileWriter`: Writes character data to a file. Ideal for writing plain text.

```java
FileWriter writer = new FileWriter("document.txt"); 
writer.write("Hello world");
```

---
### Delete & Exist

`Delete`: Deletes the file or directory

```java
File file = new File("document.txt");
file.delete();
```

`Exist`: Checks if file or directory exist

```java
File file = new File("document.txt");

if(file.exists()) {
	System.out.print("File exist");
}
else {
	System.out.print("The file does not exist");
}
```

---
### IOEExepction

`IOException`: A checked exception that signals problems during input/output operations, such as:

- File not found

- Permission denied

- Disk or network errors

You must handle it using `try-catch` or declare it with `throws`.

---
### BufferedWriter & BufferedReader

`BufferedWriter`: Writes text to a file using a buffer, which improves performance.

- It stores data in memory before writing it all at once, reducing disk access.

```java
BufferedWriter bw = new BufferedWriter(new FileWriter("document.txt"));
bw.write("Hello world");
bw.close();
```

`BufferedReader`:

Read 1 line:
```java
BufferedReader br = new BufferedReader(new FileReader("document.txt"));
String line_1 = br.readLine();
br.close();
System.out.println(line_1);
```

Read Multiple Lines:
```java
BufferedReader br = new BufferedReader(new FileReader("document.txt"));
String line;
while ((line = br.readLine()) != null){
	System.out.println(line)
}
br.close()
```

---
### FileOutputStream & FileInputStream

`FileOutputStream`: Writes raw bytes to a file. Best for binary data like images or audio.

`FileInputStream`: Reads raw bytes from a file.

```java
FileOutputStream fos = new FileOutputStream("image.jpg");
FileInputStream fis = new FileInputStream("image.jpg");
```

---
### ObjectOutputStream & ObjectInputStream

`ObjectOutputStream`: Serializes Java objects and writes them to a file.

`ObjectInputStream`: Deserializes objects from a file and reconstructs them in memory.

The object’s class must implement `Serializable`.

```java
ObjectOutputStream oos = new ObjectOutputStream(new FileOutputStream("data.obj"));
oos.writeObject(myObject);
oos.close();

ObjectInputStream ois = new ObjectInputStream(new FileInputStream("data.obj"));
Object obj = ois.readObject();
ois.close();
```

#### Casting when reading objects

Since `readObject()` returns a generic `Object`, you must **cast** it to the expected class:

```java
Person p = (Person) ois.readObject();
```

> This tells Java: “Treat this object as a `Person`.”