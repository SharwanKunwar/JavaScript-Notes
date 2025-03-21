# JavaScript Functionality Summary

## 1. Calculate Total Using Rest Operator
This section demonstrates the use of the **rest operator (`...x`)** in JavaScript functions to handle multiple arguments as an array.

### Code Example:
```javascript
function CalculateTotal(...x) {
    return x;
}

let price = CalculateTotal(10, 20, 30, 40, 50);
let card = 0; // Initialize with 0 to store the sum

console.log(typeof price); // 'object' since it's an array
console.log(typeof card);  // 'number'

price.forEach(element => {
    console.log(element);
    card += element; // Summing all elements
});

console.log("\n\n");
console.log(card); // Prints total sum
console.log("Added into card");
```
### Output:
- Prints each price value.
- Logs the total sum of the array elements.
- Displays a confirmation message.

---

## 2. Passing Objects to Functions
This section demonstrates how to pass JavaScript **objects** to functions and access their properties dynamically.

### Code Example:
```javascript
const person = {
    name: "John Doe",
    age: 30
}
const facebook = {
    name: "Parbesh Rawal",
    age: 23
}
const unpredictable_code = {
    name: "Sharwan Jung Kunwar",
    age: 21
}

function handleObject(anyobject) {
    console.log(`UserName: ${anyobject.name}\nAge: ${anyobject.age}\n`);
}

handleObject(person);
handleObject(facebook);
handleObject(unpredictable_code);

handleObject({
    name: "Mahakal",
    age: 22
});
```
### Output:
- Logs name and age of different user objects passed to the function.
- Demonstrates handling **anonymous objects** directly in function calls.

---

## 3. Passing Arrays to Functions
This section shows how **arrays** can be passed to functions and manipulated within them.

### Code Example:
```javascript
const myUserArray = ["parbesh", "suman", "kabita", "roshan", "manish"];
myUserArray.push("harry");
myUserArray.push("Karishma");

function ReturnCurrentUser(users) {
    return users[users.length - 1]; // Returns the last user in the array
}

let myCurrentUser = ReturnCurrentUser(myUserArray);

console.log(`Total users: ${myUserArray.length}`);
console.table(myUserArray);
console.log(`${myCurrentUser} is logged in`);
```
### Output:
- Logs the total number of users.
- Uses `console.table()` to display the list of users in a structured format.
- Logs the most recently added user as the "logged-in" user.

---

## 4. All About basic Functions
This section covers various function types, including function declarations, parameter handling, and return values.

### Code Example:
```javascript
// Function Definitions

// Function 01: Greeting
function greeting(){
    console.log("Jay Mahakal");
}

// Function 02: Blank Space
function blankSpace(x) {
    for(let i = 0; i < x; i++) {
        console.log("\n");
    }
}

// Function 03: Sum
function sum(num01, num02) {
    if(typeof num01 === "number" && typeof num02 === "number") {
        return num01 + num02;
    } else {
        console.log("Both inputs should be numbers");
        return "Invalid input";
    }
}

// Function 04: Say My Name
function sayMyName(name) {
    return `Hey ${name}, how was it going?`;
}

// Function 05: Logging Message
function logginMessage(userName = "user") {
    return `${userName} just Logged in`;
}

// Function Calls
blankSpace(2);
greeting();
blankSpace(2);
greeting();
blankSpace(1);

// Sum Function Call
let result = sum(6, 4);
console.log(result);

// Say My Name Function Call
let say = sayMyName("Sharwan");
console.log(say);

// Logging Message Function Call
let logMessage = logginMessage("Parbesh");
console.log(logMessage);

blankSpace(2);
```
### Output:
- Logs greeting messages.
- Inserts blank spaces dynamically.
- Computes and logs the sum of two numbers.
- Displays a personalized greeting message.
- Logs user login messages.

---

## Key Takeaways
- **Rest Operator (`...x`)**: Used to collect multiple function arguments into an array.
- **Objects in Functions**: Objects can be passed and accessed dynamically in functions.
- **Arrays in Functions**: Arrays can be manipulated and used within functions to retrieve or modify values.
- **Using `console.table()`**: A cleaner way to display array contents in a tabular format.
- **Default Function Parameters**: Functions can have default values to handle missing arguments.

---

### Author
Sharwan Jung Kunwar


