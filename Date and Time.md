# JavaScript Date and Time

JavaScript provides the `Date` object to work with dates and times. It allows us to create, manipulate, and format dates.

## 1. Creating a Date Object
The `Date` object can be created in multiple ways:

### 1.1 Using the Current Date and Time
```javascript
const now = new Date();
console.log(now); // Outputs the current date and time
```

### 1.2 Creating a Specific Date
```javascript
const specificDate = new Date(2025, 2, 14); // Year, Month (0-based), Day
console.log(specificDate);
```
> **Note:** Months in JavaScript start from `0` (January = 0, February = 1, etc.).

### 1.3 Using a Date String
```javascript
const dateFromString = new Date("2025-03-14T10:30:00");
console.log(dateFromString);
```

### 1.4 Using Timestamps (Milliseconds since Jan 1, 1970)
```javascript
const timestampDate = new Date(1672531200000);
console.log(timestampDate);
```

## 2. Getting Date Components
You can extract specific parts of a date using getter methods.

| Method | Description | Example Output |
|--------|------------|---------------|
| `getFullYear()` | Gets the year | `2025` |
| `getMonth()` | Gets the month (0-11) | `2` (March) |
| `getDate()` | Gets the day of the month (1-31) | `14` |
| `getDay()` | Gets the day of the week (0-6, where 0 = Sunday) | `5` (Friday) |
| `getHours()` | Gets the hour (0-23) | `10` |
| `getMinutes()` | Gets the minutes (0-59) | `30` |
| `getSeconds()` | Gets the seconds (0-59) | `45` |

### Example
```javascript
const date = new Date();
console.log("Year:", date.getFullYear());
console.log("Month:", date.getMonth() + 1); // +1 to make it human-friendly
console.log("Day:", date.getDate());
console.log("Weekday:", date.getDay());
console.log("Hours:", date.getHours());
console.log("Minutes:", date.getMinutes());
console.log("Seconds:", date.getSeconds());
```

## 3. Setting Date Components
Setter methods allow modifying an existing `Date` object without creating a new one.

| Method | Description |
|--------|------------|
| `setFullYear(year)` | Sets the year |
| `setMonth(month)` | Sets the month (0-11) |
| `setDate(day)` | Sets the day of the month |
| `setHours(hours)` | Sets the hour |
| `setMinutes(minutes)` | Sets the minutes |
| `setSeconds(seconds)` | Sets the seconds |

### Example
```javascript
const date = new Date();
date.setFullYear(2030);
date.setMonth(5);  // June (0-based index)
date.setDate(25);
console.log(date);
```

## 4. Formatting Dates

### 4.1 Using `toLocaleString()`
```javascript
const date = new Date();
console.log(date.toLocaleString("en-US"));  // MM/DD/YYYY, HH:MM:SS AM/PM
console.log(date.toLocaleString("en-GB"));  // DD/MM/YYYY, HH:MM:SS
console.log(date.toLocaleString("fr-FR"));  // DD/MM/YYYY, HH:MM:SS
```

### 4.2 Using `toISOString()`
```javascript
const date = new Date();
console.log(date.toISOString()); // Outputs in ISO format (YYYY-MM-DDTHH:mm:ss.sssZ)
```

### 4.3 Custom Formatting
```javascript
const date = new Date();
const formattedDate = `${date.getFullYear()}-${date.getMonth() + 1}-${date.getDate()}`;
console.log(formattedDate); // Outputs YYYY-MM-DD
```

## 5. Working with Time

### 5.1 Getting Timestamps
```javascript
console.log(Date.now());
```

### 5.2 Comparing Dates
```javascript
const date1 = new Date("2025-03-14");
const date2 = new Date("2025-03-15");

if (date1 < date2) {
    console.log("date1 is earlier than date2");
}
```

### 5.3 Adding Time (e.g., Add 7 Days)
```javascript
const date = new Date();
date.setDate(date.getDate() + 7);
console.log(date); // Outputs a date 7 days in the future
```

## 6. Handling Time Zones
JavaScript uses the system's local time zone, but you can adjust it:

```javascript
const date = new Date();
console.log(date.toUTCString());  // Converts to UTC time
console.log(date.toTimeString()); // Outputs local time
```

## 7. Date Libraries for Advanced Usage
For better date manipulation, use libraries like:

- **Moment.js** (deprecated but still widely used)
- **date-fns** (lightweight and modern)
- **Luxon** (powerful for time zones)

Example using `date-fns`:
```javascript
import { format, addDays } from "date-fns";

const today = new Date();
const futureDate = addDays(today, 7);

console.log(format(futureDate, "yyyy-MM-dd")); // Outputs YYYY-MM-DD
```

# Conclusion
- JavaScript's `Date` object allows you to create, manipulate, and format dates.
- Use `getFullYear()`, `getMonth()`, etc., to extract parts of a date.
- Modify dates using `setFullYear()`, `setMonth()`, etc.
- Format dates using `toLocaleString()`, `toISOString()`, or custom logic.
- Work with timestamps using `Date.now()`.
- Use external libraries like `date-fns` for better date handling.

Understanding how to manipulate dates effectively is crucial for many applications, including scheduling, data analysis, and user interactions. Mastering JavaScript's `Date` object will help you build more dynamic and reliable applications.

Happy Coding! 🚀
