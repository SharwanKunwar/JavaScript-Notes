# 📌 Stack vs. Heap Memory in JavaScript  

JavaScript uses **Stack** and **Heap** memory to manage data efficiently.  

---

## 🔹 Stack Memory (Primitive Data Types)  
- **Stores**: Primitive values (`Number`, `String`, `Boolean`, `null`, `undefined`, `Symbol`, `BigInt`).
- **Memory Allocation**: Stored in a fixed-size, fast-access **stack**.
- **Behavior**: Follows **LIFO (Last In, First Out)**.
- **Copying Values**: When assigned to another variable, **a copy is created**.

### ✅ Example (Stack Memory)
```javascript
let a = 10;
let b = a; // Copy of 'a' is assigned to 'b'
b = 20;

console.log(a); // Output: 10 (unchanged)
console.log(b); // Output: 20
```
<hr><hr>
<br><br><br><br>

# 🔹 Heap Memory (Reference Data Types)  

## 📌 Stores:
- **Objects, Arrays, and Functions**.  
- **Memory Allocation**: Stored in **heap**, accessed via **reference**.  
- **Behavior**: Changing a reference variable affects all variables pointing to the same object.  

### ✅ Example (Heap Memory)
```javascript
let obj1 = { name: "Sharwan" };
let obj2 = obj1; // Reference to the same object in heap
obj2.name = "Jung";

console.log(obj1.name); // Output: Jung
console.log(obj2.name); // Output: Jung
```


# 🔥 Key Differences: Stack vs. Heap Memory  

| Feature         | Stack Memory            | Heap Memory                        |
|----------------|------------------------|------------------------------------|
| **Data Type**   | Primitive values        | Reference types (objects, arrays, functions) |
| **Memory Location** | Stack (Fixed-size, Fast) | Heap (Dynamic, Slow) |
| **Copy Behavior** | Stores a **copy** of the value | Stores a **reference** to the value |
| **Modification** | Changes **do not** affect original | Changes **affect all references** |

---

## 🚀 Summary  
- **Stack** is for **primitive values**, **Heap** is for **objects, arrays, and functions**.  
- **Primitive types are copied**, **reference types share memory**.  
- **Use stack for small, fixed-size data** and **heap for complex, dynamic data**.  

---

