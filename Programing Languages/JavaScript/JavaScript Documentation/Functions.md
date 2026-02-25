JavaScript offers **four main ways** to define functions, each with its own syntax and use case

### **Function Declaration**

This is the classic way to define a function:

```JavaScript
function greet(name) {
  console.log(`Hello, ${name}`);
}

greet("Alice");
```

> **What is hoisting?** 
> 
> Hoisting is JavaScript's behavior of moving function and variable declarations to the top of their scope before code execution. 
> 
> This means you can call a function _before_ it's defined—if it's declared using the `function` keyword. However, variables declared with `let` or `const` are _not_

- Can be called **before** its definition due to _hoisting_.
    
- Great for reusable logic.

---

### **Function Expression**

Here, the function is assigned to a variable:

```JavaScript
const greet = function(name) {
  console.log(`Hello, ${name}`);
};

greet("Bob");
```

- Cannot be called before it's defined.
    
- Useful for passing functions as arguments.

---

### **Arrow Function**

A modern and concise syntax introduced in ES6:

```JavaScript
const greet = (name) => {
  console.log(`Hello, ${name}`);
};

greet("Charlie");
```

>**What is ES6?** 
>ES6 (also known as ECMAScript 2015) is a major update to JavaScript that introduced modern features like `let`, `const`, arrow functions (`=>`), template literals, classes, modules, and more. 
>
>It made JavaScript more powerful, readable, and easier to write—especially for larger applications.

- Does **not** have its own `this` context.
    
- Ideal for short, anonymous functions and callbacks.

---

### **Method Function (Object Method)**

Functions can also be defined inside objects:

```JavaScript
const person = {
  greet(name) {
    console.log(`Hi, ${name}`);
  }
};

person.greet("Dana");
```

- Common in object-oriented programming.
    
- Has access to the object’s `this`.

---

### Summary Table

|Type|Hoisted|Own `this`|Syntax Style|
|---|---|---|---|
|Function Declaration|✅|✅|Traditional|
|Function Expression|❌|✅|Flexible|
|Arrow Function|❌|❌|Modern|
|Method Function|❌|✅|Object-based|