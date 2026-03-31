SwiftUI is Apple’s modern declarative framework for building user interfaces across all platforms. Instead of manually updating views, you describe what the UI _should look like_, and SwiftUI automatically updates it when the underlying data changes.

---

#### **1. Declarative Syntax**

You describe the UI and its behavior in a simple, readable way:

```swift
var body: some View {
    Text("Hello, SwiftUI!")
        .font(.title)
        .padding()
} 
```

#### **2. Views**

Everything in SwiftUI is a `View`:

- `Text`
    
- `Image`
    
- `Button`
    
- `VStack`, `HStack`, `ZStack`
    
- Custom reusable views
    

Views are lightweight and composable.

#### **3. State Management**

SwiftUI updates the UI automatically when data changes.

Common property wrappers:

- `@State` – Local state
    
- `@Binding` – Pass state between views
    
- `@ObservedObject` – External data source
    
- `@StateObject` – Persistent observable object
    
- `@EnvironmentObject` – Shared global data

#### **4. Modifiers**

Modifiers transform or style views:

```swift
Text("Welcome")
    .font(.headline)
    .foregroundColor(.blue)
    .padding()
```

#### **5. Layout System**

SwiftUI uses stacks, grids, and frames to build layouts:

- `VStack` – Vertical layout
    
- `HStack` – Horizontal layout
    
- `ZStack` – Overlapping layers
    
- `LazyVGrid` / `LazyHGrid` – Efficient grids

#### **6. Navigation**

Modern navigation tools:

- `NavigationStack`
    
- `NavigationLink`
    
- `sheet`, `fullScreenCover`
    
- `tabView`

#### **7. Previews**

SwiftUI Previews let you see UI changes instantly:

```swift
#Preview {
    ContentView()
}
```

You can preview:

- Light/Dark mode
    
- Different devices
    
- Dynamic type sizes