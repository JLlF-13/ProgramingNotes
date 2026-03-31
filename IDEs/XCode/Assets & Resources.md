Xcode organizes all visual and data resources inside **Asset Catalogs**, ensuring they are optimized for every Apple device.

---

### Types of Assets

#### **1. Images**

- Automatically handles @1x, @2x, @3x
    
- Supports vector PDFs
    
- Named access via `Image("iconName")` or `UIImage(named:)`
    

#### **2. Colors**

- Centralized color definitions
    
- Supports light/dark mode variations
    
- Accessed with `Color("Primary")` or `UIColor(named:)`
    

#### **3. App Icons**

- Managed in the _AppIcon_ set
    
- Xcode validates required sizes for iOS, macOS, watchOS, tvOS
    

#### **4. Data Assets**

- JSON
    
- Binary files
    
- Custom data formats
    

#### **5. Localization**

- `.strings` files
    
- Localized asset variants