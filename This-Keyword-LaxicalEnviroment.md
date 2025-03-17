## --- This in traditional function ---
**Explanation:** In traditional functions, this points to the global object (e.g., window in browsers). In this case, this.age will be undefined because age is not defined on the global object.
```javascript
console.log("\nTraditional function result\n");

const tradtionalFuction = function(a, b){
    let age = 22;
    console.log(this.age);  // 'this' points to the global object (in browser, window object)
    return a + b;
}

let result = tradtionalFuction(2, 2);
console.log(result);
```


## --- This in Arrow function ---
**Explanation:** Arrow functions do not have their own this. Instead, they inherit this lexically from the surrounding context. In this case, this refers to the global object, so this.age will be undefined.
```javascript
console.log("\n\nArrow function result\n");
const arrowFunction = (num01, num02) => {
    let age = 22;
    console.log(this.age);  // 'this' is lexically inherited from the surrounding environment (global context)
    return num01 + num02;
}

let result02 = arrowFunction(5, 10);
console.log(result02);
```


## --- This in object inside Arrow function ---
**Explanation:** In the object method, the arrow function inside does not bind this to the object. Instead, it points to the global context, which leads to undefined for both this.websiteName and this.date.
```javascript
console.log("\n\nObject inside Arrow function result\n");
const myObj = {
    websiteName: "Unpredictable Website",
    date: "2021-09-01",
    welcomeMessage: () => {
        // Here 'this' does not refer to myObj because arrow functions lexically bind 'this' from the surrounding environment
        return console.log(`Welcome to ${this.websiteName} on ${this.date}`);  // 'this' refers to global context
    }
}
myObj.welcomeMessage();  // Will print 'Welcome to undefined on undefined' because 'this' is pointing to the global object
```

## --- This in object ---
**Explanation:** In this case, this correctly refers to the object (Human). It allows access to the properties of the object such as this.Name.
```javascript
const Human = {
    Name: "Sharwan Jung Kunwar",
    age: 22,
    address: "Kathmandu",
    welcomeMessage: function(){
        console.log(`Hello ${this.Name}, Welcome to the world of JavaScript`);  // Here 'this' correctly refers to the object itself
    }
}

Human.welcomeMessage();  // Will print 'Hello Sharwan Jung Kunwar, Welcome to the world of JavaScript'
```


## --- Lexical Environment Demo ---
**Explanation:** Arrow functions capture the lexical environment at the time they are defined. In this case, the arrow function inside outerFunction correctly logs outerVar, which is from the outer scope.
```javascript
function outerFunction() {
    let outerVar = "I am from the outer function";
    const innerArrowFunction = () => {
        // The arrow function has a lexical environment that 'remembers' the context where it was defined
        console.log(outerVar);  // 'this' is not involved here, but it will refer to the surrounding context
    };
    innerArrowFunction();
}

outerFunction();  // Will print 'I am from the outer function' because the arrow function remembers the enclosing scope
```


## --- This in Lexical Environment ---
**Explanation:** The arrow function inside the showDetails method uses this from the method's scope. So it correctly accesses the name and age properties of the object.

```javascript
const lexicalExample = {
    name: "Lexical Example",
    age: 30,
    showDetails: function() {
        console.log(`Name: ${this.name}, Age: ${this.age}`);
        // Using an arrow function inside the object method to demonstrate lexical scoping of `this`
        const innerArrow = () => {
            console.log(`Inside arrow function -> Name: ${this.name}, Age: ${this.age}`);
        };

        innerArrow();  // Inherits 'this' from the showDetails method, so it accesses the object's properties
    }
};

lexicalExample.showDetails();
```

## --- This in lexical Enviroment ---
**Explanation:** In this example, the arrow function accessSome inside showDetails correctly inherits this from the object, allowing it to access this.Name and this.address.
```javascript
const MyLexicalExample = {
    Name: "Sharwan Jung Kunwar",
    age: 22,
    address: "kathmandu",
    showDetails: function()
    {        
        console.log(`Address: ${this.address}`);
        const accessSome = () => {
            console.log(`Name: ${this.Name}`);
            
        }
        accessSome();
    }
}

MyLexicalExample.showDetails(); 
```
<br>

# Conclusion

* **Traditional functions:** this points to the global object (or undefined in strict mode).
* **Arrow functions:** this is lexically inherited from the surrounding context, meaning they don't have their own this.
* **Object methods:** this correctly refers to the object when using traditional functions.
* **Lexical scoping:** Arrow functions capture and remember their defining context, allowing access to variables from the surrounding scope.

**This demonstration highlights the difference between traditional and arrow functions when dealing with this in JavaScript.**