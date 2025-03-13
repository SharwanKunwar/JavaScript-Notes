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
<hr>
<br><br><br><br>


# JavaScript Type Conversion

This script demonstrates how to convert a given value into different data types in JavaScript.

## Code:
```javascript
let value = 1; // Change this value to test different data types

// Converting to different types
let toBoolean = Boolean(value); 
let toNumber = Number(value);
let toString = String(value);
let toBigInt = BigInt(value); 
let toSymbol = Symbol(value.toString()); 
let toObject = Object(value);

// Logging results in the same format
console.log(value + " : " + toBoolean + " : " + typeof toBoolean);
console.log(value + " : " + toNumber + " : " + typeof toNumber);
console.log(value + " : " + toString + " : " + typeof toString);
console.log(value + " : " + toBigInt + " : " + typeof toBigInt);
console.log(value + " : " + toSymbol.toString() + " : " + typeof toSymbol);
console.log(value + " : " + JSON.stringify(toObject) + " : " + typeof toObject);
```



## Explanation:

| **Original Value** | **Converted To** | **Result** |
|--------------------|-----------------|------------|
| `Boolean(value)`  | Boolean          | `true` for truthy values, `false` for falsy values (`0`, `""`, `null`, `undefined`, `NaN`) |
| `Number(value)`   | Number           | Converts valid strings/numbers, `null → 0`, `true → 1`, `false → 0`, `undefined → NaN` |
| `String(value)`   | String           | Converts any value to its string representation |
| `BigInt(value)`   | BigInt           | Converts whole numbers to BigInt (fractions cause an error) |
| `Symbol(value.toString())` | Symbol | Creates a unique and immutable identifier |
| `Object(value)`   | Object           | Converts primitive values into object wrappers |

## How to Use:
1. Copy and paste the code into your JavaScript environment.
2. Modify the `value` variable to test different data types.
3. Run the script and observe the output in the console.

## Example Outputs:

For `value = 1`:
```javascript
1 : true : boolean
1 : 1 : number
1 : 1 : string
1 : 1n : bigint
1 : Symbol(1) : symbol
1 : {"valueOf":1} : object