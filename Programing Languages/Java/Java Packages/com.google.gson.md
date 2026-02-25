
### Writing to File

> To write JSON data to a file, you first need a class that represents your data — for example, a `Project` or `Exercise` class.

```java
String json_write = gson.toJson(exercisis);
BufferedWriter writer = new BufferedWriter(new FileWriter(file_json)); 
writer.write(json_write);
writer.close();
```

Explanation:
- `gson.toJson(exercisis)`: Converts your Java object (like a list or a class instance) into a JSON-formatted string.
    
- `BufferedWriter` with `FileWriter`: Used to write text (in this case, JSON) to a file.
    
- `writer.write(json_write)`: Writes the JSON content to the file.
    
- `writer.close()`: Closes the writer to ensure all data is properly saved and resources are released.

---
### Reading from File

> To read JSON data to a file, you first need a class that represents your data — for example, a `Project` or `Exercise` class.

```java
List<WriteJson> exercisisDeserialitzats = new ArrayList<>(); 
BufferedReader reader = new BufferedReader(new FileReader(file_json));
JsonParser parser = new JsonParser(); 
JsonArray gsonArr = parser.parse(reader).getAsJsonArray();

for (JsonElement obj : gsonArr) { 
	JsonObject gsonObj = obj.getAsJsonObject();
	
	String name = gsonObj.get("name").getAsString();
	String descripcio = gsonObj.get("descripcio").getAsString();
	Double pressupost = gsonObj.get("pressupost").getAsDouble();
	
	JsonArray tags = gsonObj.get("tags").getAsJsonArray(); 
	List<String> listtags = new ArrayList<String>();
	for (JsonElement tag : tags) {
		listtags.add(tag.getAsString());
	}
	
	JsonArray deadlines = gsonObj.get("deadlines").getAsJsonArray(); 
	List<Date> listdeadlines = new ArrayList<>();
	for (JsonElement deadline : deadlines) {
		try {
			Date date = sdf.parse(deadline.getAsString());
			listdeadlines.add(date);
		} catch (Exception e) {
			e.printStackTrace();
		}
	}
	
	WriteJson project = new WriteJson(name, descripcio, pressupost, listtags, listdeadlines); 
	exercisisDeserialitzats.add(project); 
}
System.out.println("El JSON ha sigut desrialitzat");
System.out.println(exercisisDeserialitzats);
```

Explanation:
- `List<Writerjson>`: Create a array with the type of the class created
- `BufferedReader`: We get to read the file
- `JsonParser()`: We parse the buffered data
- `getAsJsonArray()`: The parsed buffere is converted to a json array for correct reading 
- `for (JsonElement obj : gsonArr)`: We ran through the file
- `JsonObject gsonObj = obj.getAsJsonObject()`: 
- `DataType variable = gsonObj("attribute_name").getDataType()`: 
- `Object name = new Object(attributes)`: We set the value to the attribute of the object we that we are creating
- `List.add(name)`: We add the created object to the list
- `System.out.println(List)`: We print the list with the memory name of the object
