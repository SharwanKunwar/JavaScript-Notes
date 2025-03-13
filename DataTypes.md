## 📌 JavaScript Data Types
JavaScript has **8** main data types, categorized as **Primitive** and **Non-Primitive**.

### 🔹 Primitive Data Types (Immutable)
- **String** → Represents text values.
  ```javascript
  let name = "Sharwan";
  ```
- **Number** → Represents integers & floating points.
  ```javascript
  let age = 21;
  let price = 99.99;
  ```
- **BigInt** → Handles very large numbers.
  ```javascript
  let bigNumber = 12345678901234567890n;
  ```
- **Boolean** → Represents `true` or `false`.
  ```javascript
  let isStudent = true;
  ```
- **Undefined** → A variable declared but not assigned a value.
  ```javascript
  let x;
  console.log(x); // undefined
  ```
- **Null** → Represents an intentional absence of value.
  ```javascript
  let y = null;
  ```
- **Symbol** → Unique and immutable identifier.
  ```javascript
  let sym = Symbol("id");
  ```

### 🔹 Non-Primitive (Reference) Data Type
- **Object** → Stores key-value pairs and complex data.
  ```javascript
  let person = { name: "Sharwan", age: 21 };
  ```
- **Array** →  A collection of ordered values, internally an object.
```javascript
let numbers = [10, 20, 30, 40];
console.log(numbers[1]); // Output: 20
```
- **function** → A block of reusable code that can be executed. Functions are also objects in JavaScript.
```javascript
function greet(name) {
  return "Hello, " + name + "!";
}

console.log(greet("Sharwan")); // Output: Hello, Sharwan!

```

---

## 🔥 Key Points:
- **Objects, arrays, and functions** are all **reference types**.
- **Arrays** are **objects** with indexed elements.
- **Functions** are **callable objects** with special properties.
