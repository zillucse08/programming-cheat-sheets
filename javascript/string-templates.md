- [Back to JavaScript page](./README.md)

# 🧵 JavaScript String Templates Cheat Sheet

A quick reference for working with template literals (string templates) in JavaScript.

---

## 📌 1. What are String Templates?

String templates (template literals) are strings defined using **backticks (` `)**.

```js
let text = `Hello World`;
```

👉 Introduced in ES6
👉 More powerful than normal strings

## 🔤 2. Syntax

```js
let message = `This is a template string`;
```

👉 Uses backticks instead of quotes

##🔄 3. Multiline Strings

```js
let text = `Hello
World
JavaScript`;
```

👉 No need for \n

## 🔗 4. String Interpolation

Insert variables directly using ${}:

```js
let name = "Zillur";
let text = `Hello ${name}`;
```

## ➕ 5. Expressions Inside Strings

```js
let price = 10;
let quantity = 2;

let total = `Total: ${price * quantity}`;
```

👉 You can run JavaScript expressions inside ${}

## 🔧 6. Variables Inside Templates

```js
let firstName = "Zillur";
let lastName = "Rahman";

let fullName = `${firstName} ${lastName}`;
```

## ⚖️ 7. Template vs Normal String

Normal String

```js
let text = "Hello " + name + "!";
```

Template String

```js
let text = `Hello ${name}!`;
```

👉 Cleaner and more readable

## 🧠 8. HTML Templates

```js
let name = "Zillur";

let html = `
  <div>
    <h1>${name}</h1>
  </div>
`;
```

👉 Very useful for UI rendering

## 🔁 9. Loop Example

```js
let items = ["Apple", "Banana"];

let list = `
<ul>
  ${items.map((item) => `<li>${item}</li>`).join("")}
</ul>
`;
```

## 🧪 10. Tagged Templates (Advanced)

```js
function tag(strings, value) {
  return strings[0] + value.toUpperCase();
}

let result = tag`Hello ${"world"}`;
```

👉 Allows custom processing of template strings

## ⚠️ 11. Key Notes

- Use backticks ( ), NOT quotes
- ${} works only inside template strings
- Supports multiline and expressions
- Cleaner than string concatenation

## 💡 12. Best Practices

- Use template strings instead of + concatenation
- Use for HTML generation
- Keep expressions simple
- Avoid overly complex logic inside ${}

## 🎯 13. Summary

- Template strings use backticks
- Support interpolation ${}
- Allow multiline strings
- Improve readability
- Useful for dynamic content

- [Back to JavaScript page](./README.md)
