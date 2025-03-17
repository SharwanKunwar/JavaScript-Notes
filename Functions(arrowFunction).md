# JavaScript Object and Arrow Function Examples

## Overview
This repository contains JavaScript code demonstrating object creation, methods, and arrow function usage. Below is a breakdown of the key concepts covered in the code.

---

## 1. JavaScript Object with Methods

### Object Declaration
An object `user` is created with the following properties:
- `Name`: "Mahakal"
- `age`: 100
- `address`: "kailas-parbat"
- `isMarried`: `true`
- `contact`: 9763290022
- `welcomeMessage()`: A method that prints a welcome message using the `Name` property.

### Method Execution
The `welcomeMessage` function is invoked, and later the `Name` property is updated to a new value (`"sharwan jung kunwar"`) and invoked again.

```javascript
user.welcomeMessage();
user.Name = "sharwan jung kunwar";
user.welcomeMessage();
```

---

## 2. Function and Arrow Function Differences

### Understanding `this` in Functions
One key difference between traditional functions and arrow functions is how they handle the `this` keyword:
- **Traditional Functions**: The `this` keyword refers to the object that calls the function.
- **Arrow Functions**: Arrow functions do not have their own `this`; instead, they inherit `this` from the surrounding lexical scope.

### Traditional Function
A function `some()` attempts to log `this.age`, but it does not work as expected because `this` in a traditional function depends on how the function is called. If it's called in a global context, `this` will refer to the global object (or `undefined` in strict mode), which does not have an `age` property.

```javascript
function some() {
    let age = 22;
    console.log(this.age);  // Undefined in non-object context
}
```

### Arrow Function Behavior
An arrow function `ArrowFunction01()` is declared, which also logs `this.age`. Unlike traditional functions, arrow functions do not have their own `this` binding. Instead, they inherit `this` from their lexical scope, meaning they take `this` from the surrounding function or execution context.

```javascript
const ArrowFunction01 = () => {
    let age = 22;
    console.log(this.age);  // Undefined
}
```
### Traditional Function
A function `some()` attempts to log `this.age`, but it does not work as expected due to `this` binding in non-object functions.

```javascript
function some() {
    let age = 22;
    console.log(this.age);  // Undefined in non-object context
}
```

### Arrow Function Behavior
An arrow function `ArrowFunction01()` is declared, which also logs `this.age`. Arrow functions do not have their own `this` binding, so they inherit from the surrounding lexical scope.

```javascript
const ArrowFunction01 = () => {
    let age = 22;
    console.log(this.age);  // Undefined
}
```

---

## 3. Arrow Functions for Arithmetic Operations

Arrow functions are widely preferred for their concise syntax and ease of use. They allow writing shorter, more readable code, especially for simple operations. Unlike traditional functions, arrow functions can omit the `return` keyword when using implicit returns, making them more concise.

### Sum of Two Numbers (Standard Arrow Function)
```javascript
const sumOfTwoNum = (num01, num02) => {
    let sum = num01 + num02;
    return console.log(sum);
}
```

### Compact Arrow Function
```javascript
const arrowFunction = (num01, num02) => num01 + num02;
let result = arrowFunction(5,10);
console.log(result);
```

### One-Line Return Arrow Function
```javascript
const arrowFunction02 = (num01, num02) => num01 + num02;
let result02 = arrowFunction02(10,10);
console.log(result02);
```

### Arrow Function With `{}` vs `()`
```javascript
const ArrowFunction03 = (x01, x02) => (x01 + x02);  // No need for return keyword
let result03 = ArrowFunction03(10,40);
console.log(result03);
```
```javascript
const ArrowFunction04 = (a, b) => { return a+b };  // Requires return keyword
let result04 = ArrowFunction04(10,90);
console.log(result04);
```

### Sum of Two Numbers (Standard Arrow Function)
```javascript
const sumOfTwoNum = (num01, num02) => {
    let sum = num01 + num02;
    return console.log(sum);
}
```

### Compact Arrow Function
```javascript
const arrowFunction = (num01, num02) => num01 + num02;
let result = arrowFunction(5,10);
console.log(result);
```

### One-Line Return Arrow Function
```javascript
const arrowFunction02 = (num01, num02) => num01 + num02;
let result02 = arrowFunction02(10,10);
console.log(result02);
```

### Arrow Function With `{}` vs `()`
```javascript
const ArrowFunction03 = (x01, x02) => (x01 + x02);  // No need for return keyword
let result03 = ArrowFunction03(10,40);
console.log(result03);
```
```javascript
const ArrowFunction04 = (a, b) => { return a+b };  // Requires return keyword
let result04 = ArrowFunction04(10,90);
console.log(result04);
```

---

## 4. Returning Objects from Functions

### Returning an Object from an Arrow Function
Arrow functions allow implicit returns when returning objects. To do so, wrap the object in parentheses `()`; otherwise, JavaScript may misinterpret the opening `{}` as a function block.

#### Implicit Return (Concise Syntax)
```javascript
const arrowFunction009 = (some01, some02) => ({ username: "sharwan", age: 22 });
let result009 = arrowFunction009();
console.log(result009);
```
Here, the object is returned implicitly without the `return` keyword.

#### Explicit Return (Standard Syntax)
```javascript
const arrowFunction010 = (some01, some02) => {
    return { username: "sharwan", age: 22 };
};
let result010 = arrowFunction010();
console.log(result010);
```
With curly braces `{}`, you must explicitly use `return` to return the object.

### Returning an Object Using Traditional Function
Traditional functions follow a standard return approach:
```javascript
const someWork = function(some01, some02){
    const object01 = {
        username: "parbesh",
        age: 22
    };
    return object01;
}
let result008 = someWork();
console.log(result008);
```

### Key Differences
- **Arrow Function Implicit Return**: Requires wrapping the object in `()` to avoid syntax errors.
- **Arrow Function Explicit Return**: Uses `{}` with `return` like traditional functions.
- **Traditional Function**: Always requires `return` for object output.

Using implicit return makes arrow functions more concise, but explicit return offers better readability when dealing with complex logic.

### Returning an Object from an Arrow Function
```javascript
const arrowFunction009 = (some01, some02) => ({ username: "sharwan", age: 22 });
let result009 = arrowFunction009();
console.log(result009);
```

### Returning an Object Using Traditional Function
```javascript
const someWork = function(some01, some02){
    const object01 = {
        username: "parbesh",
        age: 22
    };
    return object01;
}
let result008 = someWork();
console.log(result008);
```

---

## Conclusion
- Demonstrates object creation and method execution in JavaScript.
- Explores traditional vs. arrow function behaviors.
- Shows different ways to return values, including numbers and objects.
- Highlights the nuances of `this` keyword in functions and arrow functions.

This serves as a fundamental guide to understanding JavaScript objects and arrow functions.

