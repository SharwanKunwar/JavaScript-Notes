# JavaScript Data Type Comparison

This document explains how different data types in JavaScript behave when compared using `==` (loose equality) and `===` (strict equality).

## Explanation:

| **Comparison**                | **Loose Equality (`==`)** | **Strict Equality (`===`)** |
|--------------------------------|--------------------------|-----------------------------|
| `1 == "1"`                    | `true` (type conversion) | `false` (different types)  |
| `0 == false`                  | `true` (both are falsy)  | `false` (different types)  |
| `null == undefined`            | `true` (special case)   | `false` (different types)  |
| `NaN == NaN`                  | `false` (NaN is never equal to NaN) | `false` |
| `[] == ""`                    | `true` (empty array converts to empty string) | `false` |
| `[] == 0`                     | `true` (empty array converts to 0) | `false` |
| `{ } == { }`                  | `false` (objects are compared by reference) | `false` |
| `"0" == false`                | `true` (string converts to number `0`) | `false` |
| `true == "1"`                 | `true` (`"1"` converts to `1`) | `false` |

## Rules to Remember:
1. **`==` (Loose Equality)** performs type conversion if necessary.
2. **`===` (Strict Equality)** checks both value and type.
3. **`null` and `undefined`** are only equal to each other with `==`, not with `===`.
4. **Objects and arrays** are compared by reference, not by value.
5. **NaN is not equal to itself** (`NaN !== NaN`).

## How to Use:
1. Copy and paste the following code into your JavaScript environment.
2. Run the script to observe the comparison results.

## Example Code:
```javascript
console.log(1 == "1", 1 === "1");  // true, false
console.log(0 == false, 0 === false);  // true, false
console.log(null == undefined, null === undefined);  // true, false
console.log(NaN == NaN, NaN === NaN);  // false, false
console.log([] == "", [] === "");  // true, false
console.log([] == 0, [] === 0);  // true, false
console.log({} == {}, {} === {});  // false, false
console.log("0" == false, "0" === false);  // true, false
console.log(true == "1", true === "1");  // true, false
```

### Example Output:
```arduino
true false
true false
true false
false false
true false
true false
false false
true false
true false
```