# JavaScript Fundamentals: Declaring Variables (`let`, `const`, `var`)

## Introduction

So far, we’ve been declaring variables using the **`let`** keyword.

However, JavaScript actually provides **three ways** to declare variables:

1. `let`
2. `const`
3. `var`

* `let` and `const` were introduced in **ES6 (ES2015)** → modern JavaScript
* `var` is the **old way** of declaring variables

In this lecture, we’ll learn:

* How these keywords differ
* When to use each one
* Which ones to avoid

---

## Cleaning Up Previous Code

Before starting a new lecture, previous code is usually moved to the bottom or commented out. This keeps the file clean and focused on the current topic.

This is just a workflow habit — not a language rule.

---

## Declaring Variables with `let`

### Purpose of `let`

We use **`let`** to declare variables that **can change later** during program execution.

Example:

```javascript
let age = 30;
age = 31;
```

Here:

* The variable `age` starts at `30`
* Later, it is changed to `31`

This is perfectly valid.

---

### Reassigning (Mutating) Variables

In technical terms:

* Reassigning a new value to a variable is called **mutation**
* A variable whose value can change is called **mutable**

Example:

```javascript
let age = 30;
age = 31; // mutation
```

The value changed from `30` to `31`, so the variable was mutated.

This is **exactly what `let` is designed for**.

---

### Declaring Empty Variables with `let`

`let` also allows you to declare variables **without assigning a value immediately**:

```javascript
let year;
year = 1991;
```

This is useful when:

* You want to declare variables at the top of a file
* You only assign values later (for example, based on conditions)

---

## Declaring Variables with `const`

### Purpose of `const`

We use **`const`** for variables whose values **should never change**.

Example:

```javascript
const birthYear = 1991;
```

This variable is **immutable**.

---

### Reassigning a `const` Variable (Not Allowed)

```javascript
const birthYear = 1991;
birthYear = 1990;
```

❌ This produces an error:

```text
TypeError: Assignment to constant variable
```

That’s exactly the point of `const`.

---

### Immutable Variables

In technical terms:

* Variables declared with `const` are **immutable**
* They **cannot be mutated**

This makes `const` ideal for values that should never change.

---

### Real-World Example

* **Birth year** → never changes → use `const`
* **Age** → changes over time → use `let`

```javascript
const birthYear = 1991;
let age = 30;
age = 31;
```

---

### Empty `const` Variables Are Not Allowed

This is illegal:

```javascript
const year;
```

JavaScript throws this error:

```text
SyntaxError: Missing initializer in const declaration
```

Why?

* `const` **requires an initial value**
* You must assign a value at declaration time

---

## Best Practice: `const` vs `let`

### Recommended Rule

👉 **Use `const` by default**
👉 **Use `let` only when the value must change**

Why?

* Fewer variable mutations = fewer bugs
* Immutable values are easier to reason about
* Your code becomes more predictable

---

### Example

If a variable never changes:

```javascript
const country = "Nigeria";
```

If it changes later:

```javascript
let score = 0;
score = 10;
```

From this point onward, the instructor will mostly use `const`.

---

## Declaring Variables with `var` (Avoid This)

### What Is `var`?

* `var` is the **old way** of declaring variables
* Used before ES6

Example:

```javascript
var job = "programmer";
job = "teacher";
```

This works — no errors.

---

### Why `var` Is Bad

Although `var` looks similar to `let`, it behaves **very differently under the hood**.

There are important differences related to:

* Scope
* Hoisting
* Global behavior

These differences will be covered in **Section 7**, once you understand:

* Blocks
* Functions

For now, the rule is simple:

🚫 **Never use `var` in modern JavaScript**

---

## Declaring Variables Without `let`, `const`, or `var` (Very Bad Practice)

JavaScript allows this:

```javascript
lastName = "Schmedtmann";
console.log(lastName);
```

This works — but it’s a **terrible idea**.

---

### Why This Is Dangerous

* The variable is **not created in the current scope**
* JavaScript creates a property on the **global object**
* This leads to:

  * Hard-to-find bugs
  * Unpredictable behavior

---

### Golden Rule

✅ **Always declare variables properly**

Use:

* `const`
* `let`

Never rely on implicit variable creation.

---

## Final Summary

### Variable Declaration Keywords

| Keyword | Use Case                  | Should You Use It?  |
| ------- | ------------------------- | ------------------- |
| `const` | Value should never change | ✅ Yes (default)     |
| `let`   | Value needs to change     | ✅ Yes (when needed) |
| `var`   | Old, legacy behavior      | ❌ No                |
| none    | Creates global variables  | ❌ Never             |

---

## Encouragement & Next Steps

Even though the code doesn’t do much yet, you’re building **strong foundations**.

These fundamentals are critical:

* Clean code
* Fewer bugs
* Better long-term understanding

Next up 👉 **Operators in JavaScript** — where things start getting more interesting 🚀