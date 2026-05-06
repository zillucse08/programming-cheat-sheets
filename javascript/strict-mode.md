- [Back to JavaScript page](./README.md)

# 🔒 JavaScript Strict Mode Cheat Sheet

A quick reference for understanding and using strict mode in JavaScript.

---

## 📌 1. What is Strict Mode?

Strict mode is a way to **enforce stricter parsing and error handling** in JavaScript.

👉 Helps you write **cleaner, safer code**  
👉 Prevents silent errors and bad practices

---

## 🚀 2. How to Enable Strict Mode

### Global Scope

```js
"use strict";

x = 10; // ❌ Error
```

## Function Scope

```js
function test() {
  "use strict";
  x = 10; // ❌ Error
}
```

👉 Only applies inside that function

## ⚠️ 3. Prevents Undeclared Variables

```js
"use strict";
x = 10; // ❌ ReferenceError
```

👉 Without strict mode → becomes global
👉 With strict mode → throws error

## ❌ 4. Disallows Duplicate Parameters

```js
"use strict";
function test(a, a) {
  // ❌ Error
  console.log(a);
}
```

## ⛔ 5. Disallows Deleting Variables

```js
"use strict";

var x = 10;
delete x; // ❌ TypeError
```

## 🚫 6. Disallows Octal Literals

```js
"use strict";

var x = 010; // ❌ SyntaxError (not 8!)
```

👉 Old-style octal numbers are not allowed

## 🔒 7. Makes "this" Safer

```js
"use strict";

function test() {
  console.log(this);
}

test(); // undefined
```

👉 Without strict mode → this = global object
👉 With strict mode → this = undefined

## 🚫 8. Disallows Reserved Keywords

```js
"use strict";
var eval = 10; // ❌ Error
```

👉 Strict mode reserves certain words like `eval`, `arguments`, `interface`, etc., that cannot be used as variable names.

## ⚠️ 9. Prevents Silent Errors

```js
"use strict";

const obj = {};
Object.defineProperty(obj, "x", { value: 10, writable: false });

obj.x = 20; // ❌ Error (instead of silent fail)
```

👉 Makes bugs visible

## 10 Overview table

| Feature                 | Without Strict Mode  | With Strict Mode                       |
| ----------------------- | -------------------- | -------------------------------------- |
| Undeclared variables    | Become global        | ❌ ReferenceError                      |
| `this` in functions     | Global object        | undefined                              |
| Deleting variables      | Works silently       | ❌ TypeError                           |
| Duplicate parameters    | Allowed              | ❌ Error                               |
| Octal literals          | Allowed (010 = 8)    | ❌ SyntaxError                         |
| Silent property changes | Silent fail          | ❌ Error                               |
| `eval()` usage          | More powerful        | Restricted                             |
| Function declarations   | Allowed in any order | Must be declared before use (hoisting) |

## 🧠 11. Where to Use Strict Mode?

- At the top of files (recommended)
- Inside functions (when needed)
- Automatically enabled in ES Modules

## 💡 12. Best Practices

- Always use strict mode (or ES Modules)
- Avoid undeclared variables
- Use let and const
- Write cleaner, predictable code

## 🎯 13. Summary

- Strict mode = safer JavaScript
- Prevents bad syntax and hidden bugs
- Turns silent errors into visible errors
- Changes behavior of this
- Required for modern JS standards

- [Back to JavaScript page](./README.md)
