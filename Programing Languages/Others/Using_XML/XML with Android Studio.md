Android Studio uses XML for its activities

---
## Structure of a XML in Android Studio

### When to use android and app:

#### Android
- Refers to **standard system attributes**.
    
- Used for layout, text, color, size, etc.s 

#### App
- Refers to **custom or library-specific attributes**.
    
- Used with components like ConstraintLayout, Navigation, etc.

---
### Layout and Entities

Layout
```xml
<androidx.constraintlayout.widget.ConstraintLayout
	xmlns:android="http://schemas.android.com/apk/res/android"  
    xmlns:app="http://schemas.android.com/apk/res-auto"  
    xmlns:tools="http://schemas.android.com/tools"  
    android:id="@+id/id_activity"  
    android:layout_width="match_parent"  
    android:layout_height="match_parent"  
    tools:context=".activiti_name">

</androidx.constraintlayout.widget.ConstraintLayout>
```

Entities
```xml
<TextView 
	android:id="@+id/id_name"
	android:layout_width="150dp"
	android:layout_height="wrap_content"
/> 
```

---
## Perks and AddOns

Inside the `res` folder we can find alot more folders but the most important are `layouts` folder that has all the activities thet we have already seen above, also the `values` folder in that we have the themes and other thing like the `style` to have the code more clean, the `fonts` folder for the font files and also `strings` in where we have the text thats in the activities this way its more easy to change or to manage different languages

Example of style:
```xml
<?xml version="1.0" encoding="utf-8"?>  
<resources>  
    <style name="home_buttons">  
        <item name="android:layout_width">120dp</item>  
        <item name="android:layout_height">wrap_content</item>  
        <item name="android:layout_marginTop">12dp</item>  
        <item name="android:fontFamily">@font/roboto_mono_semibold</item>  
        <item name="layout_constraintHorizontal_bias">0.500</item>  
        <item name="layout_constraintEnd_toEndOf">parent</item>  
        <item name="layout_constraintStart_toStartOf">parent</item>  
        <item name="cornerRadius">5dp</item>  
    </style>
</resources>
```

Example of strings:
```xml
<resources>  
    <string name="app_name">Snake_JoanLluchFonoll</string>  
  
    <string name="snake">Snake</string>  
  
    <string name="play">PLAY</string>  
    <string name="setting">SETTINGS</string>  
    <string name="about">ABOUT</string>  
    <string name="exit">EXIT</string>  
</resources>
```
