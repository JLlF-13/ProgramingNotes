Views that organize layout and structure.

### VStack

```swift
VStack {
    Text("Top")
    Text("Bottom")
}
```

### HStack

```swift
HStack {
    Image(systemName: "person")
    Text("Username")
}
```

### ZStack

```swift
ZStack {
    Color.blue
    Text("Overlay")
}
```

### ScrollView

```swift
ScrollView {
    Text("Scrollable content")
}
```

### List

```swift
List(items) { item in
    Text(item.title)
}
```

### Form

```swift
Form {
    Section(header: Text("Tipus de Castell")) {
        // Components here
    }
}
```

### Section

```swift
Section(header: Text("Settings")) {
    Toggle("Dark Mode", isOn: $darkMode)
}
```

### Group / GroupBox

```swift
GroupBox("Info") {
    Text("Details here")
}
```

### NavigationStack

```swift
NavigationStack {
    Text("Home")
}
```

### TabView

```swift
TabView {
    HomeView().tabItem { Label("Home", systemImage: "house") }
    SettingsView().tabItem { Label("Settings", systemImage: "gear") }
}
```



