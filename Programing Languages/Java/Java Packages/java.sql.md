Used to work with databases with java

## Connect to a database

```java
private static final String URL = "jdbc:mysql://127.0.0.1:3306/concecionario?useSSL=false&serverTimezone=UTC";
private static final String USER = "root";
private static final String PASSWORD = "";

public static void main(String[] args) {

try (Connection conn = DriverManager.getConnection(URL, USER, PASSWORD)) {
	// Database Sentaces
}catch (SQLException e) {
	e.printStackTrace();
}
```

---
## Database Sentaces

```java
try (Statement stmt = conn.createStatement()) {
	//
}
```

Create table example:
```java
try (Statement stmt = conn.createStatement()) {
	String sqlDDL = "CREATE TABLE IF NOT EXISTS profesores (" +
	"id INT AUTO_INCREMENT PRIMARY KEY," +
	"nombre VARCHAR(50) NOT NULL)";
	stmt.executeUpdate(sqlDDL);
	System.out.println("Tabla profesores creada (si no existía)");
}
```

Insert in a table:
```java
String insertAlumno = "INSERT INTO alumnos(nombre, edad) VALUES(?, ?)";
try (PreparedStatement ps = conn.prepareStatement(insertAlumno, Statement.RETURN_GENERATED_KEYS)) {
	ps.setString(1, "Juan");
	ps.setInt(2, 20);
	ps.executeUpdate();
	ps.setString(1, "Ana");
	ps.setInt(2, 22);
	ps.executeUpdate();
	ps.setString(1, "Luis");
	ps.setInt(2, 19);
	ps.executeUpdate();
}
```

Update table:
```java
String updateAlumno = "UPDATE alumnos SET edad = ? WHERE nombre = ?";
try (PreparedStatement ps = conn.prepareStatement(updateAlumno)) {
	ps.setInt(1, 21);
	ps.setString(2, "Juan");
	ps.executeUpdate();
}
```

Select from a table:
```java
String selectAlumnos = "SELECT * FROM alumnos WHERE edad > ?";
try (PreparedStatement ps = conn.prepareStatement(selectAlumnos)) {
	ps.setInt(1, 20);
	ResultSet rs = ps.executeQuery();
	while (rs.next()) {
		System.out.println("Alumno: " + rs.getString("nombre") + ", Edad: " + rs.getInt("edad"));
	}
}
```