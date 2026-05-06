- [Back to JavaScript page](./README.md)

# 🔍 JavaScript String Search Cheat Sheet

A curated reference for **searching and matching strings** in modern JavaScript.

---

## 📌 1. includes() (Most Used)

```js
"Hello World".includes("World"); // true
"Hello World".includes("hello"); // false (case sensitive)
"Hello World".includes("World", 0); // true (start index)
```

** 👉 Use for checking existence **
Features

- Returns true/false
- Case-sensitive

** 👉 Preferred for simple checks **

## 📌 2. startsWith() / endsWith()

```js
"Hello".startsWith("He"); // true
"Hello".endsWith("lo"); // true
```

** 👉 Use cases **

- Prefix validation
- File extensions

## 📌 3. indexOf()

```js
"Hello".indexOf("l"); // 2
```

** 👉 Notes **

- Returns index or -1
- Older method

** 👉 Use includes() for readability **

## 📌 4. lastIndexOf()

```js
"Hello Hello".lastIndexOf("Hello"); // 6
```

** 👉 Finds last occurrence **

## 📌 5. search() (Regex-based)

```js
"Hello World".search("World"); // 6
"Hello World".search(/world/i); // 6 (case-insensitive)
```

** 👉 Useful when working with patterns **

## 📌 6. match() (Regex Matches)

```js
"Hello World".match("World"); // ["World", index: 6, input: "Hello World", groups: undefined]
"Hello World".match(/world/i); // ["World", index: 6, input: "Hello World", groups: undefined]
"Hello World".match(/l/g); // ["l", "l"] (all occurrences)
```

```js
"Hello 123".match(/\d+/); // ["123"]
```

** 👉 Notes **

- Returns array or null
- Supports regex

## 📌 7. matchAll() (Modern)

```js
[..."test1test2".matchAll(/\d/g)];
```

```js
// Returns an iterator
const iterator = "test1test2".matchAll(/\d/g);
```

** 👉 Returns all matches (iterator) **

## 📌 8. test() (Regex)

```js
/\d/.test("Hello1"); // true
```

** 👉 Best for validation checks **

## 📌 9. exec() (Advanced)

```js
/\d+/.exec("abc123"); // ["123"]
```

** 👉 More control than match() **

## 📌 10. Global flag (g)

```js
"Hello World".match(/l/g); // ["l", "l"]
```

** 👉 Find all occurrences **

## ⚖️ 10. Comparison Table

| Method       | Return Type | Use Case       |
| ------------ | ----------- | -------------- |
| includes()   | boolean     | simple check   |
| startsWith() | boolean     | prefix         |
| endsWith()   | boolean     | suffix         |
| indexOf()    | number      | position       |
| search()     | number      | regex position |
| match()      | array/null  | extract match  |
| matchAll()   | iterator    | all matches    |
| test()       | boolean     | validation     |
| exec()       | array/null  | advanced regex |

## 🧪 11. Real Examples

```js
// Check email
email.includes("@");
// Validate number
/^\d+$/.test("123"); // true
// Extract numbers
"Order 123".match(/\d+/); // ["123"]
Case-insensitive search
"Hello".search(/hello/i);
```

## ⚠️ Removed / Avoided

Not included intentionally:

- Complex outdated patterns ❌
- Redundant examples ❌
- Overuse of indexOf() ❌

## 💡 12. Best Practices

- Use includes() for simple checks
- Use startsWith() / endsWith() for structure
- Use regex (test, match) for validation
- Avoid overusing indexOf()
- Keep logic readable

## 🎯 13. Summary

- Use modern methods for clarity
- Regex = powerful search tool
- Choose method based on use case
- Prefer readability over clever tricks

- [Back to JavaScript page](./README.md)
