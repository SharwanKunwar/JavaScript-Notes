# JavaScript Execution Context

## Introduction
JavaScript Execution Context is the environment in which JavaScript code is executed. The JavaScript engine creates different execution contexts to manage the execution of code.

## Types of Execution Contexts
1. **Global Execution Context (GEC)**
   - This is the default execution context.
   - It is created when a web page is loaded.
   - Any code that is not inside a function is executed in this context.
   
2. **Function Execution Context (FEC)**
   - This is created every time a function is invoked.
   - Each function call gets its own execution context.
   - It contains a scope chain, local variables, and `this` keyword.
   
3. **Eval Execution Context**
   - Created when the `eval()` function is used to execute a string of JavaScript code.
   - Generally, it is not recommended due to security and performance concerns.

## How Execution Context Works
When JavaScript code runs, the JavaScript engine follows these steps:
1. **Creation Phase:**
   - The global execution context is created.
   - Function declarations are stored in memory.
   - Variables are initialized with `undefined` (Hoisting).
   
2. **Execution Phase:**
   - Code is executed line by line.
   - Function execution creates a new execution context.
   - Variables get assigned actual values.

## Example 1: Global & Functional Execution Context
```javascript
let Number01 = 10;
let Number02 = 20;

function sum(Number01, Number02) {
    let result = Number01 + Number02;
    return result;
}

let sumResult = sum(Number01, Number02);
let result = sum(4,5);
```
### Explanation:
- The global execution context is created when the script runs.
- `sum()` function is called twice, each creating a new function execution context.
- Variables `result` and `sumResult` store the returned values from function calls.

## Example 2: Returning Values to Global Execution Context
```javascript
let FirstName = "Sharwan";
let LastName = "Kunwar";

function PrintMyName(F_Name, L_Name){
    let FullName = F_Name + " " + L_Name;
    return FullName;
}

let storeMyName = PrintMyName(FirstName, LastName);
let myFriendName = PrintMyName("Parbesh", "Rawal");
console.log(storeMyName);  // Output: "Sharwan Kunwar"
console.log(myFriendName); // Output: "Parbesh Rawal"
```
### Explanation:
- The function `PrintMyName()` is called twice, each time creating a function execution context.
- Returned values are stored in global execution context variables (`storeMyName` & `myFriendName`).
- `console.log()` outputs the results.

## Conclusion
- Execution contexts help JavaScript manage the execution flow.
- Global execution context is created by default.
- Functions create a new execution context whenever they are invoked.
- JavaScript follows a two-phase process: Creation and Execution.
- Understanding execution contexts helps in debugging and optimizing JavaScript code.

---


