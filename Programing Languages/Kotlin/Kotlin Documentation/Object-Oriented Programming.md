
### Standar class, Constructor and Accesing data:

Structure: 
```kotlin
class Objectname (var/val atributename: Type) {}
```

Example:
```kotlin
class Movie (val title: String, val duration: Int, val director: String, val year: Int, var isRented: Boolean ) { }
```

Overcharged contructors:

```kotlin
class Movie (val title: String, val duration: Int, val director: String, val year: Int, var isRented: Boolean ) { 
	constructor (): this ("",0,"",0,false)
	constructor (title: String, duration: Int, director:String, year: Int): this (title, duration, director, year, false) 
}
```

> Contructor is a reserves word

#### Accesing data

*Based on Movie contructor

```kotlin
var bladerunner = Movie ( "Blade Runner" , 117, "Ridley Scott" , 1982, false) 
var mononoke = Movie ( "Princess Mononoke" , 133, "Hayao Miyazaki" , 1996, false) 

println(bladerunner.director)
mononoke.year = 1997 
bladerunner.isRented=true 
```

Output:

```
Hayao Miyazaki
Error because year is val
Ok because isRented is var
```

> In kotlin you dont need to create setters and getters in public classes unlike java

### Init block

Used to check the creating objects like a movies older that 1888 can be created and assing values to atributes

Object creating checker:

```kotlin
class Movie (val title: String, val duration: Int, val director: String, val year: Int, var isRented: Boolean ) {
	init {
		println("Creada la pel·lícula ' $title' dirigida per $director en $year")
		if (year < 1888) {
			throw IllegalArgumentException( "L'any ha de ser vàlid, major o igual a 1888" )
		}
	}
}
```

```kotlin
var mononoke = Movie ( "Random name" , 120, "Anonymus" , 1800, false )
```

```cmd
Error The movie year haas to be valid, higher or equal to 1888
```

### Methods

Are actions in the class, like editing the object showing the object interacting with other objects

```kotlin
class Movie (val title: String, val duration: Int, val director: String, val year: Int, var isRented: Boolean ) {
	fun rentMovie() { ... }
	fun returnMovie () { ... }
	fun movieDescript() { ... }
}

var bladerunner = Movie ( "Blade Runner" , 117, "Ridley Scott" , 1982, false) 

bladerunner.rentMovie()
bladerunner.returnMovie()
bladerunner.movieDescript()
```

Explanation:

- Object is created
- isRented is set to true
- isRented is set to false
- Describes the object

### Modifing acces

Key differences with java:
- Withou explicit modificator = public
- Internat (does not exist in java): VIsible inside the same module
- Protected: Visibility inside the class and subclasses but not inside the same packet x classs that are not subclasses
Public i private like java
The syntax is the same modificator className(){ ... }

```kotlin
private class Movie (val title: String, val duration: Int, val director: String, val year:Int, var isRented: Boolean ) {}
```

#### Acces private attributes

We said before that we not create getters and setters, but if you want to make private attributes accesible we have to do this:

Only read:

```kotlin
class Persona {
	private var nomPrivat: String = ""
	val nom: String
	get() = nomPrivat
}
```

Read and Write:

```kotlin
class Persona {
	private var nomPrivat: String = ""
	var nom: String
	get() = nomPrivat
	set(value){ nomPrivat = value}
}
```

Acces:

```kotlin
var person = Persona()
person.nom = "Mike" // Error if the set is not definded
println(person.nom)
```

### Nested & Inner

#### Nested

A class inside another class. To create and instance of a class we have to do this: `Outer.Nested()`

```kotlin
class City(val name: String) { //Outer
	class Ghost(val name: String) { //Nested
		fun scare() = "¡Buuu! I am the gosth $name."
	}
}
fun main() {
	val ghost = City.Ghost( "Slimer")
	println(ghost.scare())
}
```

Output:

```
¡Buuu! I am the gosth Slimer.
```

#### Inner

To acces the atributes or functions of the outer class we need to use and inner class

```kotlin
class City(val name: String) {
	class Ghost(val name: String) {}
	inner class GhostBuster( val nameGhostBuster : String, ghost: Ghost) {
		val ghost = ghost
		fun bust() = "$nameGhostBuster atraparà a ${ghost.name} en $name." 
	}
}
fun main() {
	val slimer = City.Ghost("Slimer")
	val newyork = City("Nova York")
	val venkman = newyork.GhostBuster("Venkman", slimer)
	println(venkman.bust()) 
}
```

Output:

```
Venkman atraparà a Slimer en Nova York
```

