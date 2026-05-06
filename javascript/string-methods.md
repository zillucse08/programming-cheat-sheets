- [Back to JavaScript page](./README.md)

# 🔤 JavaScript String Methods Cheat Sheet

A curated list of **modern, useful string methods** (ES6+ focused).

---

## 📌 1. Basic Methods

### length

```js
let str = "Hello";
str.length; // 5
```

### toUpperCase / toLowerCase

```js
let str = "Hello";
str.toUpperCase(); // "HELLO"
str.toLowerCase(); // "hello"
```

## 🔍 2. Searching

### includes()

```js
"Hello World".includes("World"); // true
```

### startsWith() / endsWith()

```js
"Hello".startsWith("He"); // true
"Hello".endsWith("lo"); // true
```

### indexOf()

```js
"Hello".indexOf("l"); // 2
```

## ✂️ 3. Extracting Parts

### slice()

```js
"Hello".slice(1, 4); // "ell"
```

### substring()

```js
"Hello".substring(1, 4); // "ell"
```

**👉 Similar to slice, but no negative index support**

## 🔁 4. Replacing

### replace()

```js
"Hello World".replace("World", "JS"); // "Hello JS"
```

### replaceAll()

```js
"apple apple".replaceAll("apple", "banana");
```

## 🧩 5. Splitting & Joining

### split()

```js
"apple,banana".split(","); // ["apple", "banana"]
```

### join()

```js
let arr = ["apple", "banana", "cherry"];
arr.join(", "); // "apple, banana, cherry"
```

## ➕ 6. Combining Strings

### concat()

```js
"Hello".concat(" ", "World"); // "Hello World"
```

**👉 Prefer template literals instead**

## 🧼 7. Trimming

### trim()

```js
"  Hello  ".trim(); // "Hello"
```

### trimStart() / trimEnd()

```js
"  Hello".trimStart(); // "Hello"
"Hello  ".trimEnd(); // "Hello"
```

## 🧠 8. Character Access

### charAt()

```js
"Hello".charAt(1); // "e"
```

### at() (modern)

```js
"Hello".at(-1); // "o"
```

## 🔢 9. Padding

### padStart() / padEnd()

```js
"5".padStart(3, "0"); // "005"
"5".padEnd(3, "0"); // "500"
```

## 🔁 10. Repeat

### repeat()

```js
"ha".repeat(3); // "hahaha"
```

## ⚖️ 11. Comparison

### localeCompare()

```js
"a".localeCompare("b"); // -1 (a comes before b)
```

**👉 Better for sorting strings**

🧪 12. Real Examples
Clean user input

```js
let input = "  hello ";
input.trim().toLowerCase(); // "hello"
```

Check email

```js
email.includes("@");
```

Format text

```js
let name = "zillur";
name.charAt(0).toUpperCase() + name.slice(1);
```

## 💡 13. Best Practices

- Use includes() instead of indexOf()
- Use slice() over substring()
- Prefer template literals over concat()
- Use trim() for user input
- Avoid deprecated methods

## 🎯 14. Summary

- Strings are immutable
- Use modern methods (includes, slice, replaceAll)
- Prefer readability over old patterns
- Clean input before processing

- [Back to JavaScript page](./README.md)
