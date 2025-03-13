# JavaScript: let vs const vs var

## 1. var (Avoid using it)
- **Scope**: Function-scoped (accessible anywhere inside the function).
- **Redeclaration**: Allowed.
- **Reassignment**: Allowed.
- **Hoisting**: Hoisted but **not block-scoped**.
- **Issues**: Causes unexpected behavior due to lack of block scope.

```javascript
var x = 10;
if (true) {
    var x = 20; // Overwrites the previous x
}
console.log(x); // 20 (not block-scoped)
```

## 2. let (Use it when reassignment is needed)
- **Scope**: Block-scoped (only accessible inside `{}`).
- **Redeclaration**: ❌ Not allowed in the same scope.
- **Reassignment**: ✅ Allowed.
- **Hoisting**: Hoisted but **not initialized**.

```javascript
let y = 10;
if (true) {
    let y = 20; // Only inside this block
}
console.log(y); // 10 (block-scoped)
```

## 3. const (Use it when value should not change)
- **Scope**: Block-scoped, like `let`.
- **Redeclaration**: ❌ Not allowed.
- **Reassignment**: ❌ Not allowed.
- **Hoisting**: Hoisted but **not initialized**.
- **Requirement**: Must be assigned a value at declaration.

```javascript
const z = 10;
z = 20; // ❌ Error: Assignment to constant variable
```

## 🔥 Key Takeaways
✅ Use **let** for variables that may change.  
✅ Use **const** for variables that should stay the same.  
❌ Avoid **var** due to its function scope issues.  

---
