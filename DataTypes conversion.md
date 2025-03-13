# JavaScript: Data Type Conversion

## 📌 Types of Type Conversion
JavaScript has **two** types of type conversion:
1. **Implicit Conversion (Type Coercion)** → Done automatically by JavaScript.
2. **Explicit Conversion (Type Casting)** → Done manually using functions.

---

## 🔹 1. Implicit Type Conversion (Type Coercion)
JavaScript automatically converts types in certain operations.

### **String Conversion**
Numbers and booleans convert to strings when concatenated with strings.
```javascript
console.log("5" + 2);  // "52"
console.log("Hello" + true);  // "Hellotrue"
```

### **Number Conversion**
Strings and booleans convert to numbers in mathematical operations.
```javascript
console.log("5" - 2);  // 3
console.log("10" * "2");  // 20
console.log(true + 1);  // 2 (true → 1)
console.log(false - 1); // -1 (false → 0)
```

### **Boolean Conversion**
Falsy values (`"", 0, null, undefined, NaN, false`) convert to `false`, others to `true`.
```javascript
console.log(Boolean(0));   // false
console.log(Boolean(1));   // true
console.log(Boolean(""));  // false
console.log(Boolean("abc")); // true
```

---

## 🔹 2. Explicit Type Conversion (Type Casting)
We use functions to manually convert types.

### **String Conversion**
```javascript
console.log(String(123)); // "123"
console.log(String(true)); // "true"
console.log((99).toString()); // "99"
```

### **Number Conversion**
```javascript
console.log(Number("123")); // 123
console.log(Number("ABC")); // NaN
console.log(parseInt("10.5")); // 10
console.log(parseFloat("10.5")); // 10.5
```

### **Boolean Conversion**
```javascript
console.log(Boolean("Hello")); // true
console.log(Boolean(0)); // false
console.log(Boolean(1)); // true
```

---

## 🔥 Key Takeaways
✅ **Implicit conversion** happens automatically in JavaScript.  
✅ **Explicit conversion** uses `String()`, `Number()`, `Boolean()`, `parseInt()`, etc.  
✅ `+` (concatenation) converts numbers to strings, while `-`, `*`, `/` convert to numbers.  
✅ Falsy values (`"", 0, null, undefined, NaN, false`) always convert to `false`.  

---
Let me know if you need any modifications! 🚀
