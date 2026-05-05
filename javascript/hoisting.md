- [Back to JavaScript page](./README.md)

# 🚀 JavaScript Hoisting Cheat Sheet

A complete reference for understanding hoisting in JavaScript.

---

## 📌 1. What is Hoisting?

Hoisting is JavaScript's behavior of **moving declarations to the top of their scope** before execution.

👉 This means you can use variables or functions **before they are declared** :contentReference[oaicite:0]{index=0}

---

## 🧠 2. How JavaScript Sees Your Code

```js
console.log(x);
var x = 5;
```

👉 JavaScript internally treats it like:

```js
var x;
console.log(x); // undefined
x = 5;
```

👉 Only the declaration is moved, NOT the value

## ⚠️ 3. Hoisting with var

```js
console.log(x); // undefined
var x = 10;
```

## Key Behavior

- Declaration is hoisted
- Initialization is NOT hoisted
- Default value = undefined

## 4. Initialization is NOT Hoisted

```js
var x = 5;
console.log(x + y); // NaN or undefined
var y = 7;
```

👉 Internally:

```js
var x = 5;
var y;
console.log(x + y);
y = 7;
```

👉 Only declaration moves, not assignment

## 🔥 5. Hoisting with let and const

```js
console.log(a);
let a = 10;
```

👉 ❌ ReferenceError

## Why?

Variables are hoisted BUT:

- Not initialized
- Stay in Temporal Dead Zone (TDZ)

👉 Cannot access before declaration

## ⛔ 6. Temporal Dead Zone (TDZ)

```js
console.log(x); // ❌ Error
let x = 5;
```

👉 TDZ = Time between:

Start of scope
Variable declaration

👉 Variable exists but is NOT usable

## 🔁 7. Function Hoisting

Function Declaration ✅

```js
sayHello();

function sayHello() {
console.log("Hello");
}

👉 Works because:
```

Function is fully hoisted

## Function Expression ❌

```js
sayHello(); // ❌ Error

var sayHello = function () {
  console.log("Hello");
};
```

👉 Reason:

- var sayHello is hoisted as undefined
- Function is NOT assigned yet

## ⚖️ 8. Summary Table

Type Hoisted Initialized Behavior
var ✅ Yes ✅ undefined usable before declare
let ✅ Yes ❌ No TDZ error
const ✅ Yes ❌ No TDZ error
function declaration ✅ Yes ✅ Yes fully usable
function expression ✅ (var) ❌ No behaves like var

## 🧪 9. Real Example

```js
var a = 1;

function test() {
  console.log(a); // undefined
  var a = 2;
}

test();
```

## 👉 Internally:

```js
function test() {
  var a;
  console.log(a);
  a = 2;
}
```

## 💡 10. Best Practices

- Always declare variables at the top
- Avoid using variables before declaration
- Prefer let and const
- Avoid var in modern JS
- Use strict mode to prevent bugs

👉 Declaring variables at the top helps avoid confusion and errors

## 🎯 11. Key Takeaways

- Hoisting moves declarations, not values
- var → hoisted + initialized as undefined
- let/const → hoisted but blocked (TDZ)
- Functions → fully hoisted
- Misunderstanding hoisting causes bugs

- [Back to JavaScript page](./README.md)
