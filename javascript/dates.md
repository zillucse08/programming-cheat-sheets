- [Back to JavaScript page](./README.md)

# 📅 JavaScript Dates Cheat Sheet

A practical reference for working with dates and times in JavaScript.

---

## 📌 1. Creating Dates

### Current date/time

```js
let now = new Date();
```

Specific date

```js
new Date("2026-01-01");
new Date(2026, 0, 1); // Jan = 0
```

From timestamp (milliseconds)

```js
new Date(0); // Jan 1, 1970
```

## 🧠 2. Timestamp

```js
Date.now(); // current timestamp (ms)
```

### 📥 3. Get Methods

```js
let d = new Date();

d.getFullYear(); // 2025
d.getMonth(); // 0–11
d.getDate(); // 1–31
d.getDay(); // 0–6 (Sun–Sat)

d.getHours();
d.getMinutes();
d.getSeconds();
d.getMilliseconds();
```

### 📤 4. Set Methods

```js
let d = new Date();

d.setFullYear(2026);
d.setMonth(5); // June
d.setDate(15);

d.setHours(14);
d.setMinutes(30);
d.setSeconds(0);
```

## 🌐 5. Formatting Dates

toString()

```js
new Date().toString(); // Tue Jan 01 2026 00:00:00 GMT+0600 (Bangladesh Standard Time)
```

toDateString()

```js
new Date().toDateString(); // Jan 01 2026 (only date)
```

toISOString()

```js
new Date().toISOString(); // 2025-01-01T00:00:00.000Z
```

## 🌍 6. Locale Formatting (Modern)

toLocaleString()

```js
new Date().toLocaleString(); // Jan 1, 2026, 12:00:00 AM
```

Custom format

```js
new Intl.DateTimeFormat("en-US", {
  dateStyle: "medium",
  timeStyle: "short",
}).format(new Date()); // Jan 1, 2026, 12:00 AM
```

## ⏱️ 7. Date Math

Add days

```js
let d = new Date();
d.setDate(d.getDate() + 7); // add 7 days
```

Difference between dates

```js
let d1 = new Date("2025-01-01");
let d2 = new Date("2025-01-10");

let diff = d2 - d1; // milliseconds
```

## ⚠️ 8. Important Notes

Month starts from 0

```js
new Date(2025, 0, 1); // January
```

Date parsing can be tricky

```js
new Date("01-02-2025"); // ❗ not reliable
```

Always use ISO format:

```js
new Date("2025-01-02");
```

## 🌐 9. UTC Methods

```js
d.getUTCFullYear(); // UTC year
d.getUTCHours(); // UTC hours
```

Avoid timezone issues

## 🔁 10. Convert Date

```js
let d1 = new Date(); // 2025-01-01T10:00:00

let ts = d1.getTime(); // Date → number: 1762644000000
let d2 = new Date(ts); // number → Date: 2025-01-01T10:00:00
```

## 🧪 11. Real Example

Add days

```js
function addDays(date, days) {
  let d = new Date(date);
  d.setDate(d.getDate() + days);
  return d;
}
```

Format YYYY-MM-DD

```js
let d = new Date();
let formatted = d.toISOString().split("T")[0]; // YYYY-MM-DD
```

Check past/future

```js
new Date() > new Date("2025-01-01"); // true or false
```

### 💡 12. Best Practices

- Use ISO format (YYYY-MM-DD)
- Avoid manual string parsing
- Use Intl.DateTimeFormat for UI
- Be careful with timezones
- Use timestamps for calculations

### 🎯 13. Summary

- Date handles date & time
- Months start at 0
- Use get / set methods
- Use Intl for formatting
- Prefer ISO format for safety

- [Back to JavaScript page](./README.md)
