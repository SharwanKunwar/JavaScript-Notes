# IIFE (Immediately Invoked Function Expression)

## 📌 What is IIFE?
An **Immediately Invoked Function Expression (IIFE)** is a JavaScript function that runs immediately after being defined. It is a self-executing function that does not require explicit invocation.

---

## 🔹 Syntax
```javascript
// Classic IIFE
(function() {
    console.log("IIFE executed!");
})();

// Arrow Function IIFE
(() => {
    console.log("IIFE executed!");
})();
```

---

## 🎯 Purpose of IIFE
- ✅ **Avoids polluting the global scope** by creating a private scope.
- ✅ **Encapsulates variables** to prevent conflicts with other scripts.
- ✅ **Executes code immediately** without requiring a function call.
- ✅ **Used in module patterns** to create private and public methods.

---

## 🔄 Working Flow
1. **Function is wrapped inside parentheses** to treat it as an expression.
2. **It executes immediately** using `()` at the end.
3. **Creates its own scope**, preventing variable conflicts.
4. **Runs once and does not persist** unless explicitly returned.

---

## 🚀 Examples
### 🔹 Encapsulating Variables to Avoid Conflicts
```javascript
(function() {
    let count = 0;
    console.log("Count:", count);
})();
console.log(typeof count); // undefined (not accessible globally)
```

### 🔹 Using IIFE with Parameters
```javascript
((name) => {
    console.log(`Hello, ${name}!`);
})("Sharwan");
```

### 🔹 Prevent Global Scope Pollution in Loops
```javascript
for (var i = 1; i <= 3; i++) {
    (function(i) {
        setTimeout(() => console.log(i), 1000);
    })(i);
}
// Outputs: 1, 2, 3 (instead of 3, 3, 3)
```

---

## 📌 Quick Notes
✔ **Immediately invoked** function, runs as soon as defined.  
✔ **Encapsulates variables**, preventing global pollution.  
✔ **Used for private scopes & module patterns.**  
✔ **Avoids variable hoisting issues in loops.**  
✔ **Syntax: `(function(){})()` or `(() => {})()`.**  

---

### 📌 Author
**Sharwan Kunwar** 🚀 | *Unpredictable Coders*
