This are some of the diferent data containers in Kotlin

## Arrays

Values separeted by `,`, values of the same type, limited, more values can't be added


```kotlin
var citiesArray = arrayOf("Ciutadella", "Es Castell", "Es Mercadal")
```
> Function size() to get the length

---

## List

There are 2 types of list

Similar to arrays but with more functions

| Function   | What it does              | Example                                                                             |
| ---------- | ------------------------- | ----------------------------------------------------------------------------------- |
| indexOf()  | Return index of a value   | mastersOfTheUniverse.indexOf(1) //Teela                                             |
| last()     | Returns last item         | mastersOfTheUniverse.last()                                                         |
| first()    | Return first item         | mastersOfTheUniverse.first()                                                        |
| contains() | Return values if it exist | mastersOfTheUniverse.contains(Skeletor)                                             |
| filter()   |                           | val test = mastersOfTheUniverse. filter { it == "He-Man"<br>\|\| it == "Skeletor" } |
| add()      | Add value                 | mastersOfTheUniverse.add ("Roboto")                                                 |
| remove()   | Delete value              | mastersOfTheUniverse.add ("Roboto")                                                 |
| size()     | Get length of a list      | mastersOfTheUniverse.size()                                                         |
### Mutable List

You can make a empty list and add thing or in short terms it can be edited

```kotlin
var mastersOfTheUniverse: MutableList<String> = mutableListOf()

mastersOfTheUniverse.add("He-Man")
mastersOfTheUniverse.add("Teela")
mastersOfTheUniverse.add("Skeletor")

print(mastersOfTheUniverse)
```

Here how you can add items
```kotlin
mastersOfTheUniverse.add ("Roboto") //mastersOfTheUniverse.add ( 0, "Roboto")

print(mastersOfTheUniverse)
```

> You can add the index of where you want to put the value

### Inmutable list

Can't be edited

```kotlin
var citiesList: List<String> = listOf("Ciutadella", "Es Castell", "Es Mercadal")

print(citiesList)
```

To "edit" the inmuatable list we can use the `filter()` function

```kotlin
val test = citiesList. filter { it == "Es Mercadal" || it == "Alaior" }
```