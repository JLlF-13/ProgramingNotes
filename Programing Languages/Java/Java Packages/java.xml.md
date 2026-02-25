
## Write

#### Creating the file

```java
DocumentBuilderFactory Fabrica = DocumentBuilderFactory.newInstance();

DocumentBuilder construccion = Fabrica.newDocumentBuilder();

DOMImplementation implementacion = construccion.getDOMImplementation();

Document documento = implementacion.createDocument(null, "concesionario", null); 

documento.setXmlVersion("1.0");
```

#### Elements of th efile

#### Writing the file

```java
Source fuente = new DOMSource(documento);

Result result = new StreamResult(new File(file_xml)); 

Transformer tranformar = TransformerFactory.newInstance().newTransformer();

tranformar.setOutputProperty(javax.xml.transform.OutputKeys.INDENT, "yes");

tranformar.setOutputProperty("{http://xml.apache.org/xslt}indent-amount", "2");

tranformar.transform(fuente, result)
```

---
## Read

```java
DocumentBuilderFactory Fabrica = DocumentBuilderFactory.newInstance(); 

DocumentBuilder construccion = Fabrica.newDocumentBuilder(); 

Document document = construccion.parse(file_xml);
```

You can add this optionaly
```java
document.getDocumentElement().normalize();
```

We put the elements on a list
```java
NodeList llistaCoches = document.getElementsByTagName("coche");
```

We go trugh the list 

```java
for (int i = 0; i < llistaCoches.getLength(); i++) { 

	Node node = llistaCoches.item(i);
	
	if (node.getNodeType() == Node.ELEMENT_NODE) {
	
		Element e = (Element) node; 
		
		String identifier = e.getElementsByTagName("identifier").item(0).getTextContent(); 
		
		String marca = e.getElementsByTagName("marca").item(0).getTextContent();
		
		String price = e.getElementsByTagName("price").item(0).getTextContent();
		
		System.out.println("Cotxe #" + (i + 1)); 
		
		System.out.println(" Identifier: " + identifier);
		
		System.out.println(" Marca: " + marca);
		
		System.out.println(" Preu: " + price);
		
		System.out.println();
		
	}
}
```

Possible Output:

```
Cotxe #1

Identifier: 1111BBB

Marca: PORSCHE

Preu: 90000


Cotxe #2

Identifier: 2222BBB

Marca: SEAT

Preu: 10000
```