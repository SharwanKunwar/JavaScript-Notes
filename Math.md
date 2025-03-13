# JavaScript Math Object

The `Math` object in JavaScript provides a set of mathematical functions and constants for performing calculations. It is a built-in object, meaning you don't need to instantiate it.

## Math Constants

| Constant     | Description                                          | Value            |
|--------------|------------------------------------------------------|------------------|
| `Math.PI`    | Ratio of a circle's circumference to its diameter    | 3.14159...       |
| `Math.E`     | Euler's number (Base of natural logarithms)          | 2.718...         |
| `Math.SQRT2` | Square root of 2                                    | 1.414...         |

**Example:**

```javascript
console.log(Math.PI); // Output: 3.141592653589793
```


# Math Methods in JavaScript

## 1️⃣ Rounding Methods

| Method              | Description                      | Example                       |
|---------------------|----------------------------------|-------------------------------|
| `Math.round(x)`     | Rounds to nearest integer        | `Math.round(4.6)` // 5         |
| `Math.floor(x)`     | Rounds down                      | `Math.floor(4.9)` // 4         |
| `Math.ceil(x)`      | Rounds up                        | `Math.ceil(4.1)` // 5          |
| `Math.trunc(x)`     | Removes decimal part             | `Math.trunc(4.9)` // 4         |

## 2️⃣ Random Number Generation

| Method               | Description                                      | Example                                                      |
|----------------------|--------------------------------------------------|--------------------------------------------------------------|
| `Math.random()`      | Generates a random number between 0 and 1       | `Math.random()` // 0.5678...                                 |
| Random Integer       | Generate a random integer between min and max   | `let randomNum = Math.floor(Math.random() * 10) + 1;` // Between 1 and 10 |

## 3️⃣ Power & Root Functions

| Method              | Description                         | Example                           |
|---------------------|-------------------------------------|-----------------------------------|
| `Math.pow(x, y)`    | Raises `x` to the power of `y`      | `Math.pow(2, 3)` // 8             |
| `Math.sqrt(x)`      | Square root of `x`                  | `Math.sqrt(25)` // 5              |
| `Math.cbrt(x)`      | Cube root of `x`                    | `Math.cbrt(27)` // 3              |

## 4️⃣ Absolute & Sign Functions

| Method              | Description                              | Example                       |
|---------------------|------------------------------------------|-------------------------------|
| `Math.abs(x)`       | Returns the absolute value of `x`        | `Math.abs(-5)` // 5            |
| `Math.sign(x)`      | Returns 1 (positive), -1 (negative), or 0| `Math.sign(-10)` // -1         |

## 5️⃣ Trigonometric Functions

| Method              | Description                      | Example                           |
|---------------------|----------------------------------|-----------------------------------|
| `Math.sin(x)`       | Sine of `x` (radians)           | `Math.sin(Math.PI / 2)` // 1      |
| `Math.cos(x)`       | Cosine of `x` (radians)         | `Math.cos(0)` // 1                |
| `Math.tan(x)`       | Tangent of `x` (radians)        | `Math.tan(Math.PI / 4)` // 1      |

## 6️⃣ Logarithmic & Exponential Functions

| Method              | Description                        | Example                           |
|---------------------|------------------------------------|-----------------------------------|
| `Math.log(x)`       | Natural log (base e)               | `Math.log(10)`                    |
| `Math.log10(x)`     | Logarithm base 10                  | `Math.log10(100)` // 2            |
| `Math.exp(x)`       | `e` raised to the power of `x`     | `Math.exp(1)` // 2.718...         |

## 🔥 Key Takeaways

✅ `Math` is a built-in object for mathematical operations.  
✅ `Math.random()` is useful for generating random values.  
✅ Rounding, trigonometric, logarithmic, and exponential methods are available.  
✅ Use `Math.PI`, `Math.E`, and other constants for precise calculations.
