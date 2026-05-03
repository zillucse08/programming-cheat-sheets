# 📦 JavaScript Modules Cheat Sheet

A complete reference for JavaScript Modules (ESM + CommonJS).

---

## 📌 1. What are Modules?

Modules allow you to split JavaScript code into separate files.

### Why use modules?

- Better organization
- Reusable code
- Avoid global scope pollution
- Easier maintenance

---

## 📦 2. Module Systems

### CommonJS (Node.js - legacy)

```js
const fs = require("fs");

module.exports = {
  greet() {
    return "Hello";
  },
};
```
