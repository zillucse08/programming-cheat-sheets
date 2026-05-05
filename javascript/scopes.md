- [Back to JavaScript page](./README.md)

# 🧠 JavaScript Scope Cheat Sheet

A quick reference for understanding variable scope in JavaScript.

---

## 📌 1. What is Scope?

Scope determines **where variables are accessible (visible)** in your code.

👉 Think: “Where can I use this variable?”

---

## 📦 2. Types of Scope

JavaScript has 3 types of scope:

1. Global Scope
2. Function Scope
3. Block Scope

---

## 🌍 3. Global Scope

A variable declared **outside any function or block** is global.

```js
let name = "Zillur";

function greet() {
  console.log(name); // ✅ accessible
}
```

## 🏠 4. Function Scope (Local Scope)

Variables declared inside a function are only accessible inside that function.

```js
function test() {
  let message = "Hello";
  console.log(message); // ✅
}

console.log(message); // ❌ Error
```

## 🧱 5. Block Scope (ES6)

Variables declared with let and const inside {} are block-scoped.

```js
{
  let x = 10;
  console.log(x); // ✅
}

console.log(x); // ❌ Error
```

## ⚠️ Important

```js
{
  var x = 10;
}

console.log(x); // ✅ Works (NOT block scoped)
```

👉 var ignores block scope

## ⚖️ 6. var vs let vs const

| Keyword | Scope    | Redeclare | Notes           |
| ------- | -------- | --------- | --------------- |
| var     | Function | ✅ Yes    | Old, avoid      |
| let     | Block    | ❌ No     | Preferred       |
| const   | Block    | ❌ No     | Cannot reassign |

## ⚠️ 7. Automatically Global (Danger)

If you assign a variable without declaring it, it becomes global.

```js
function test() {
  name = "Zillur"; // ❗ no let/var/const
}

test();
console.log(name); // ✅ global
```

👉 This is dangerous and should be avoided

## 🔒 8. Strict Mode

```JS
"use strict";

function test() {
  name = "Zillur"; // ❌ Error
}
```

👉 Prevents accidental global variables

## 🌐 9. Global Scope in Browser

In browsers:

Global scope = window object

```JS
var x = 10;          // global
let y = 20;          // global
const z = 30;        // global

console.log(window.x); // ✅ 10
console.log(window.y); // ✅ 20
console.log(window.z); // ✅ 30
```

👉 var attaches to window, let/const do NOT

## ⏳ 10. Variable Lifetime

Global → lives until page/browser closes
Function → destroyed after function ends

## 🧪 11. Example (Combined)

```JS
let globalVar = "I am global";

function outer() {
  let outerVar = "I am outer";

  if (true) {
    let blockVar = "I am block";

    console.log(globalVar); // ✅
    console.log(outerVar);  // ✅
    console.log(blockVar);  // ✅
  }

  console.log(blockVar); // ❌
}

outer();
```

## 💡 12. Best Practices

- Prefer let and const
- Avoid var
- Minimize global variables
- Use block scope for safety
- Always declare variables

## 🎯 Summary

- Scope = variable visibility
- Global = everywhere
- Function = inside function
- Block = inside {}
- let/const = modern and safe
- Avoid accidental globals

- [Back to JavaScript page](./README.md)
