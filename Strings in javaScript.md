# 📜 JavaScript String Documentation

## 🔹 What is a String?
A **string** in JavaScript is a sequence of characters used to represent text. Strings are **immutable**, meaning once created, they cannot be changed.

```javascript
let message = "Hello, World!";
console.log(typeof message); // Output: string
```

---

## 🔹 Creating Strings
JavaScript provides multiple ways to create strings:

### 1️⃣ Using Double or Single Quotes
```javascript
let str1 = "Hello";
let str2 = 'World';
```

### 2️⃣ Using Backticks (Template Literals - ES6)
```javascript
let name = "Sharwan";
let greeting = `Hello, ${name}!`;
console.log(greeting); // Output: Hello, Sharwan!
```

### 3️⃣ Using String Constructor
```javascript
let str3 = new String("Hello");
console.log(typeof str3); // Output: object
```

---

## 🔹 Escape Characters
Escape sequences allow the inclusion of special characters in strings.

| Escape Sequence | Description |
|---------------|-------------|
| `\n` | New Line |
| `\t` | Tab Space |
| `\'` | Single Quote |
| `\"` | Double Quote |
| `\\` | Backslash |

Example:
```javascript
let text = "Hello\nWorld";
console.log(text);
```

---

## 🔹 String Methods
JavaScript provides a variety of built-in string methods.

### 1️⃣ `length` - Get String Length
```javascript
let str = "JavaScript";
console.log(str.length); // Output: 10
```

### 2️⃣ `toUpperCase()` & `toLowerCase()`
```javascript
console.log("hello".toUpperCase()); // Output: HELLO
console.log("WORLD".toLowerCase()); // Output: world
```

### 3️⃣ `charAt(index)` - Get Character at a Position
```javascript
console.log("JavaScript".charAt(4)); // Output: S
```

### 4️⃣ `slice(start, end)` - Extract a Part of the String
```javascript
let text = "Hello World";
console.log(text.slice(0, 5)); // Output: Hello
```

### 5️⃣ `substring(start, end)` - Similar to `slice()`, but does not accept negative indices.
```javascript
console.log("Hello World".substring(0, 5)); // Output: Hello
```

### 6️⃣ `replace(searchValue, newValue)` - Replace Part of the String
```javascript
let str = "I love JavaScript";
console.log(str.replace("JavaScript", "Python")); // Output: I love Python
```

### 7️⃣ `split(separator)` - Split String into an Array
```javascript
let text = "apple,banana,grape";
console.log(text.split(",")); // Output: ["apple", "banana", "grape"]
```

### 8️⃣ `trim()` - Remove Whitespace
```javascript
let text = "   Hello World   ";
console.log(text.trim()); // Output: "Hello World"
```

### 9️⃣ `match(regex)` - Match String using Regular Expressions
```javascript
let sentence = "The sky is blue.";
console.log(sentence.match(/sky/)); // Output: ["sky"]
```

---

## 🔹 String Concatenation
### 1️⃣ Using `+` Operator
```javascript
let first = "Hello";
let second = "World";
console.log(first + " " + second); // Output: Hello World
```

### 2️⃣ Using `concat()` Method
```javascript
let str1 = "Hello";
let str2 = "World";
console.log(str1.concat(" ", str2)); // Output: Hello World
```

---

## 🔹 String Performance Considerations
- **String Concatenation (`+`) vs Template Literals (`${}`)**: Template literals are generally **faster** and more **readable**.
- **Avoid Excessive String Modification**: Since strings are immutable, modifying them frequently (e.g., using `+=`) can lead to performance issues.
- **Use `join()` for Large String Concatenations**: When dealing with large strings, `array.join("")` is more efficient than repeated `+=`.

Example:
```javascript
let arr = ["Hello", "World", "!"].join(" ");
console.log(arr); // Output: Hello World !
```

---

## 🔹 Advanced String Manipulation
### 1️⃣ Regular Expressions (`match`, `search`, `replace`, `test`)
```javascript
let text = "I love JavaScript!";
let regex = /javascript/i; // Case-insensitive search
console.log(text.search(regex)); // Output: 7
```

### 2️⃣ Encoding & Decoding Strings
```javascript
let encoded = encodeURIComponent("Hello World!");
console.log(encoded); // Output: Hello%20World%21

let decoded = decodeURIComponent(encoded);
console.log(decoded); // Output: Hello World!
```

---

## 🔥 Key Takeaways
✅ **Strings are immutable** in JavaScript.
✅ **Template literals (`${}`) are the best way to concatenate dynamic values.**
✅ **Use built-in methods like `slice()`, `split()`, `replace()` for efficient string manipulation.**
✅ **Performance considerations matter when dealing with large strings.**
✅ **Regular expressions can be powerful for advanced string operations.**

---

🚀 **Explore & Experiment with JavaScript Strings!** 🎯

