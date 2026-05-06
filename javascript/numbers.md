- [Back to JavaScript page](./README.md)

# 🔢 JavaScript Numbers Cheat Sheet

A practical reference for working with numbers in JavaScript.

---

## 📌 1. What is a Number?

JavaScript has only **one number type**:

```js
let x = 10; // integer
let y = 10.5; // decimal
```

👉 Both are of type number

## 🧠 2. Basic Operations

```js
let a = 10;
let b = 3;

a + b; // 13
a - b; // 7
a * b; // 30
a / b; // 3.33
a % b; // 1 (remainder)
a ** b; // 1000 (power)
```

## ⚠️ 3. Special Values

```js
1 / 0; // Infinity
"abc" / 2; // NaN
```

Check NaN

```js
Number.isNaN(NaN); // true
```

## 🔍 4. Type Checking

```js
typeof 10; // "number"
Number.isFinite(10); // true
```

## 🔄 5. Converting to Number

Number()

```js
Number("10"); // 10
Number("10.5"); // 10.5
```

parseInt()

```js
parseInt("10px"); // 10
```

parseFloat()

```js
parseFloat("10.5px"); // 10.5
```

## 🎯 6. Rounding

Math.round()

```js
Math.round(4.6); // 5
```

Math.floor()

```js
Math.floor(4.6); // 4
```

Math.ceil()

```js
Math.ceil(4.6); // 5
```

Math.trunc()

```js
Math.trunc(4.6); // 4
```

## 📊 7. Random Numbers

```js
Math.random(); // 0 to 0.999
Math.random() * 10; // 0 to 9.999
Math.floor(Math.random() * 10); // 0 to 9
Math.floor(Math.random() * 10) + 1; // 1 to 10
```

## ⚠️ 8. Common Gotchas

Operation with string & number:

```js
10 + "5"; // "105"
10 - "5"; // 5
10 * "5"; // 50
```

NaN Behavior

```js
NaN + 1; // NaN
NaN * 2; // NaN
```

## 🧮 9. Useful Math Methods

```js
Math.max(1, 5, 3); // 5
Math.min(1, 5, 3); // 1
Math.abs(-10); // 10
Math.pow(2, 3); // 8
Math.sqrt(16); // 4
```

## 💰 10. Number Formatting (Important)

### Intl.NumberFormat

```js
new Intl.NumberFormat().format(1000000); // "1,000,000"
```

### Currency

```js
new Intl.NumberFormat("en-US", {
  style: "currency",
  currency: "USD",
}).format(1000);
// "$1,000.00"
```

### Percentage

```js
new Intl.NumberFormat("en-US", {
  style: "percent",
}).format(0.5); // "50%"
```

## ⚠️ 11. Floating Point Issue

```js
0.1 + 0.2; // 0.30000000000000004
```

Fix

```js
Number((0.1 + 0.2).toFixed(2)); // 0.3
```

## 🔁 12. Number Methods

```js
(123).toString(); // "123"
(255).toString(16); // "ff"
```

## 💡 13. Best Practices

- Use Number() for conversion
- Use Number.isNaN() instead of isNaN()
- Avoid floating precision issues
- Use Intl.NumberFormat for UI
- Prefer Math.floor() for integers

## 🎯 14. Summary

- JS has one number type
- Supports integers and decimals
- NaN and Infinity are special values
- Use Math methods for calculations
- Use Intl API for formatting

- [Back to JavaScript page](./README.md)
