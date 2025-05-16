# 1. `setAddTask([...addTask, inputValue])` — Spreading the Array

💡 **Your Realization:**

> “We spread the `addTask` and append it to the `inputValue`”

✅ **Why it matters:**

- React state must be **immutable** — we never directly push or mutate.
- `...addTask` makes a **shallow copy** of the existing tasks.
- `[...addTask, inputValue]` builds a **new array** with the previous tasks + the new one.

🧠 **Think of it like:**

> “Hey React, here’s a brand new list — the old tasks, and one fresh one added.”

---

# ✅ 2. Controlled Components — `value` + `onChange`

💡 **Your Realization:**

> “When we take the input, we need to handle it using `onChange` and add its input value to state.”

✅ **Controlled input pattern:**

```jsx
<input 
  value={inputValue}
  onChange={(e) => setInputValue(e.target.value)} 
/>

```

---

## ✅ 3. `filter()` — Building a New Array with Logic

💡 **Your Realization:**

> “I thought `filter` removes things, but it actually builds a new array that satisfies the condition.”

🧠 **Mental model:**

```js
const filtered = arr.filter(condition);
