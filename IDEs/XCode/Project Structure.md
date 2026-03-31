Xcode organizes your app into a set of folders and files that define how your project is built, how resources are managed, and how your code is structured. Understanding this layout makes it much easier to navigate, scale, and maintain your app.

---
### Main Components

#### **1. Project Navigator**

The left sidebar where you browse all files in your project:

- Source files (`.swift`, `.m`, `.h`)
    
- Storyboards / SwiftUI Views
    
- Asset catalogs
    
- Frameworks & Packages
    
- Configuration files (`Info.plist`, `.xcconfig`)
    

#### **2. Targets**

Each target represents a build product:

- iOS app
    
- macOS app
    
- Watch app
    
- Unit tests
    
- UI tests
    

Targets define:

- Build settings
    
- Linked frameworks
    
- Capabilities (Push, iCloud, etc.)
    

#### **3. Build Settings**

A detailed configuration area controlling:

- Compilation options
    
- Swift version
    
- Optimization levels
    
- Code signing
    
- Build paths
    

#### **4. Build Phases**

Defines the order of operations during the build:

- Compile Sources
    
- Link Binary With Libraries
    
- Copy Bundle Resources
    
- Run Script Phases
    

#### **5. Schemes**

A scheme tells Xcode how to:

- Build
    
- Run
    
- Test
    
- Profile
    
- Archive
    

Useful for switching between environments (Debug, Release, Staging).

#### **6. Asset Catalogs**

Stores:

- App icons
    
- Images
    
- Colors
    
- Data sets
    

Keeps resources organized and optimized for all device sizes.

#### **7. Info.plist**

A configuration file containing:

- App permissions
    
- Display name
    
- Supported orientations
    
- URL schemes