# JavaScript Object Literals

## What is an Object Literal?
An **object literal** in JavaScript is a simple and direct way to define an object using curly braces `{}`. It is the most commonly used method to create objects.

## Creating an Object Literal
```javascript
let person = {
    name: "John",
    age: 30,
    city: "New York"
};
```
Here, `name`, `age`, and `city` are **keys (properties)**, and `"John"`, `30`, and `"New York"` are their respective **values**.

## Accessing Object Properties
### 1. Using Dot Notation (Preferred)
```javascript
console.log(person.name); // Output: "John"
```
### 2. Using Bracket Notation
```javascript
console.log(person["age"]); // Output: 30
```
Bracket notation is useful when property names are dynamic or contain special characters.

## Adding & Modifying Properties
```javascript
person.country = "USA";  // Add new property
person.age = 31;         // Modify existing property
console.log(person);
```

## Removing Properties
```javascript
delete person.city;
console.log(person);
```

## Object with Methods (Functions inside Objects)
```javascript
let user = {
    name: "Alice",
    greet: function() {
        console.log("Hello, I am " + this.name);
    }
};

user.greet(); // Output: "Hello, I am Alice"
```
🔹 `this` refers to the object itself.

## Looping Through Object Properties
### Using `for...in` Loop
```javascript
for (let key in person) {
    console.log(key + ": " + person[key]);
}
```

## Object Methods: `Object.keys()`, `Object.values()`, `Object.entries()`
```javascript
console.log(Object.keys(person));   // ["name", "age", "country"]
console.log(Object.values(person)); // ["John", 31, "USA"]
console.log(Object.entries(person)); // [["name", "John"], ["age", 31], ["country", "USA"]]
```

## Nested Object Literals
```javascript
let student = {
    name: "Emma",
    address: {
        city: "London",
        zip: "E1 6AN"
    }
};

console.log(student.address.city); // Output: "London"
```

## Conclusion
✔ Object literals are the simplest way to create objects in JavaScript.  
✔ They allow easy property access, modification, and method definition.  
✔ Useful functions like `Object.keys()` and `Object.values()` help manage objects efficiently.  

---

