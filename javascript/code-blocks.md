# 🧱 JavaScript Code Blocks Cheat Sheet

A quick reference for understanding JavaScript code blocks and how they work.

---

## 📌 1. What is a Code Block?

A **code block** is a group of statements wrapped inside `{ }`.

`````js
{
  let x = 10;
  console.log(x);
}
👉 Used to group multiple statements together

## 📦 2. Why Code Blocks Matter

Code blocks are used to:

- Group multiple statements into one unit
- Control execution flow
- Define scope (with let and const)
- Improve code organization

👉 They allow multiple statements to behave as one bloc

## 🧠 3. Code Blocks in Functions

Every function body is a code block:

```js
function greet() {
  console.log("Hello");
}
```

👉 Function logic lives inside a block

## 🔀 4. Code Blocks in Conditions

```js
if (true) {
  console.log("Yes");
} else {
  console.log("No");
}
```

👉 Each if / else uses a block


## 🔁 5. Code Blocks in Loops

For Loop

```js
for (let i = 0; i < 3; i++) {
  console.log(i);
}
```

👉 Loop code runs inside its own block


## 🔁 5. Code Blocks in Loops

For Loop

````js
for (let i = 0; i < 3; i++) {
  console.log(i);
}
`````

👉 Loop code runs inside its own block

## 🔁 5.2. While Loop

```js
while (true) {
  break;
}
```

👉 Loops execute blocks repeatedly

## 🔒 6. Block Scope (Important)

Variables declared with let and const inside a block:

👉 Only accessible inside that block

```js
{
  let x = 10;
  console.log(x); // ✅
}

console.log(x); // ❌ Error
```

👉 This prevents unwanted variable conflicts

## ⚠️ 7. var is NOT Block Scoped

```js
{
  var x = 10;
}

console.log(x); // ✅ Works
```

👉 var ignores block scope
👉 Only let and const respect it

## 🧱 8. Standalone Code Blocks

Blocks can exist without functions or conditions:

```js
{
  let x = 10;
  let y = 20;
  let sum = x + y;
}
```

👉 Useful for:

- Temporary calculations
- Limiting variable scope
- Cleaner code organization

## 🧠 9. Why Use Standalone Blocks?

- Encapsulation
- Variables stay inside the block
- Temporary Usage
- Create → use → discard variables
- Cleaner Code
- Avoid global scope pollution

👉 Helps avoid naming conflicts

## 🧪 10. Combined Example

```js
let globalVar = "Global";

function test() {
  let functionVar = "Function";

  if (true) {
    let blockVar = "Block";

    console.log(globalVar); // ✅
    console.log(functionVar); // ✅
    console.log(blockVar); // ✅
  }

  console.log(blockVar); // ❌
}

test();
```

## 💡 11. Best Practices

- Always use {} even for single-line blocks
- Prefer let and const over var
- Use blocks to limit variable scope
- Avoid unnecessary global variables
- Keep blocks small and focused

## 🎯 Summary

- Code block = {} containing statements
- Used in functions, loops, conditions
- Enables grouping and control flow
- let / const = block scoped
- var = NOT block scoped
- Blocks help keep code clean and safe
