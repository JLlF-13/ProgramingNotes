Elements that collect user input.

### TextField

```swift
TextField("Name", text: $name)
```

### SecureField

```swift
SecureField("Password", text: $password)
```

### Toggle

```swift
Toggle("Enable feature", isOn: $enabled)
```

### Slider

```swift
Slider(value: $progress, in: 0...1)
```

### Stepper

```swift
Stepper("Age: \(age)", value: $age)
```

### Picker

```swift
Picker("Categoria", selection: $category) {
    Text("Històric").tag("historic")
    Text("Modern").tag("modern")
}
```

### DatePicker

```swift
DatePicker("Birthday", selection: $birthday)
```


