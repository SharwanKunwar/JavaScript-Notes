# JavaScript Arrays: Summary and Methods

## 1. **Creating Arrays**
```javascript
let arr1 = [1, 2, 3]; // Literal notation
let arr2 = new Array(3); // Creates an empty array with length 3
let arr3 = new Array(1, 2, 3); // Creates an array with values
```

## 2. **Accessing and Modifying Elements**
```javascript
arr1[0]; // Access first element
arr1[1] = 10; // Modify second element
arr1.length; // Get length of the array
```

## 3. **Adding & Removing Elements**
- **push()**: Adds elements at the end.
- **pop()**: Removes and returns the last element.
- **unshift()**: Adds elements at the beginning.
- **shift()**: Removes and returns the first element.
- **splice(start, deleteCount, ...items)**: Adds/removes elements at specific index.

```javascript
arr1.push(4); // [1, 10, 3, 4]
arr1.pop(); // [1, 10, 3]
arr1.unshift(0); // [0, 1, 10, 3]
arr1.shift(); // [1, 10, 3]
arr1.splice(1, 1, 20); // [1, 20, 3]
```

## 4. **Iterating Over Arrays**
- **forEach()**: Executes a function for each array element.
- **map()**: Creates a new array by applying a function to each element.
- **filter()**: Creates a new array with elements that pass a test.
- **reduce()**: Reduces array to a single value.

```javascript
arr1.forEach(item => console.log(item));
let squared = arr1.map(x => x * x);
let evens = arr1.filter(x => x % 2 === 0);
let sum = arr1.reduce((acc, val) => acc + val, 0);
```

## 5. **Searching & Finding**
- **indexOf(value)**: Returns index of first occurrence, or -1 if not found.
- **lastIndexOf(value)**: Returns last occurrence index.
- **includes(value)**: Checks if array contains value (returns `true/false`).
- **find(callback)**: Returns first element that matches condition.
- **findIndex(callback)**: Returns index of first match.
- **some(callback)**: Checks if at least one element satisfies a condition.
- **every(callback)**: Checks if all elements satisfy a condition.

```javascript
arr1.indexOf(10); // 1
arr1.includes(3); // true
arr1.find(x => x > 5); // First number greater than 5
arr1.findIndex(x => x > 5); // Index of first number greater than 5
arr1.some(x => x > 5); // true if any element is greater than 5
arr1.every(x => x > 0); // true if all elements are greater than 0
```

## 6. **Sorting & Reversing**
- **sort()**: Sorts array (default is lexicographic, use compare function for numbers).
- **reverse()**: Reverses array order.
- **localeCompare()**: Used for sorting strings in different languages.

```javascript
arr1.sort((a, b) => a - b); // Numeric sort
arr1.reverse();
["é", "a", "z"].sort((a, b) => a.localeCompare(b)); // Sorts considering locale
```
- **sort()**: Sorts array (default is lexicographic, use compare function for numbers).
- **reverse()**: Reverses array order.

```javascript
arr1.sort((a, b) => a - b); // Numeric sort
arr1.reverse();
```

## 7. **Joining & Slicing**
- **join(separator)**: Converts array to string.
- **slice(start, end)**: Extracts a portion of the array.
- **concat()**: Merges arrays.

```javascript
arr1.join('-'); // "1-10-3"
arr1.slice(1, 2); // Extracts part of array
arr1.concat([4, 5]); // [1, 10, 3, 4, 5]
```

## 8. **Checking & Transforming Arrays**
- **Array.isArray(value)**: Checks if a value is an array.
- **flat(depth)**: Flattens nested arrays up to given depth.
- **flatMap(callback)**: Maps and flattens the result.

```javascript
Array.isArray(arr1); // true
[1, [2, 3], [4, [5]]].flat(2); // [1, 2, 3, 4, 5]
```

## 9. **Converting to and from Arrays**
- **from(iterable)**: Creates an array from iterable objects.
- **of(...items)**: Creates an array from given values.
- **toString()**: Converts an array to a comma-separated string.

```javascript
Array.from("hello"); // ["h", "e", "l", "l", "o"]
Array.of(1, 2, 3); // [1, 2, 3]
[1, 2, 3].toString(); // "1,2,3"
```
- **from(iterable)**: Creates an array from iterable objects.
- **of(...items)**: Creates an array from given values.

```javascript
Array.from("hello"); // ["h", "e", "l", "l", "o"]
Array.of(1, 2, 3); // [1, 2, 3]
```

This summary provides a quick reference for all essential JavaScript array methods, making it easier to revise syntax and functionality. 🚀

