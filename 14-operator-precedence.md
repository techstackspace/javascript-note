# JavaScript Fundamentals: Operator Precedence

## What Is Operator Precedence?

**Operator precedence** defines the **order in which JavaScript executes operators** in an expression.

This explains why expressions like this work correctly:

```javascript
now - 1991 > now - 2018
```

Even though subtraction and comparison are mixed, JavaScript knows **what to execute first**.

---

## Revisiting the Example

```javascript
const now = 2037;
const ageJonas = now - 1991;
const ageSarah = now - 2018;

console.log(ageJonas > ageSarah);
```

### Why Does This Work?

Because:

* Subtraction (`-`) has **higher precedence**
* Comparison (`>`) has **lower precedence**

So JavaScript:

1. Calculates both subtractions
2. Compares the results

---

## Operator Precedence Table (MDN)

JavaScript has a **well-defined precedence table**, which you can find on **MDN (Mozilla Developer Network)** by searching:

> *MDN operator precedence*

MDN is a **core documentation site** you’ll use a lot as a JavaScript developer.

### Key Takeaways from the Table

* Parentheses `()` have the **highest precedence**
* Mathematical operators run **before** comparison operators
* Assignment operators have **very low precedence**
* Some operators run **left → right**
* Others run **right → left**

You **do not** need to memorize precedence numbers — just understand the general rules.

---

## Left-to-Right vs Right-to-Left Execution

### Left-to-Right Example (Subtraction)

```javascript
console.log(25 - 10 - 5);
```

**Result:**

```text
10
```

This is evaluated as:

```text
(25 - 10) - 5
```

Because subtraction runs **left to right**.

---

## Right-to-Left Example (Assignment)

### Declaring Multiple Variables

```javascript
let x, y;
```

Both `x` and `y` are declared with the value `undefined`.

---

### Chained Assignment

```javascript
x = y = 25 - 10 - 5;
```

Let’s break this down.

#### Step 1: Subtraction (higher precedence)

```javascript
x = y = 10;
```

#### Step 2: Assignment (right to left)

```javascript
y = 10;
x = 10;
```

### Final Values

```javascript
console.log(x, y);
```

**Output:**

```text
10 10
```

---

### Why Assignment Must Be Right-to-Left

If assignment ran left-to-right:

* `x` would get the value of `y`
* But `y` would still be `undefined`
* That would produce incorrect results

So this behavior is **logical and intentional**.

---

## The Highest Precedence: Parentheses `()`

Just like in mathematics, **parentheses force execution order**.

---

## Example: Calculating an Average

### Logging Ages

```javascript
console.log(ageJonas, ageSarah);
```

---

### ❌ Incorrect Average (No Parentheses)

```javascript
const averageAge = ageJonas + ageSarah / 2;
console.log(averageAge);
```

**Why this is wrong:**

* Division happens before addition
* JavaScript evaluates it as:

  ```text
  ageJonas + (ageSarah / 2)
  ```

**Result example:**

```text
55.5
```

This makes no sense for an average.

---

### ✅ Correct Average (With Parentheses)

```javascript
const averageAge = (ageJonas + ageSarah) / 2;
console.log(averageAge);
```

Now:

1. Addition happens first
2. Division happens second

✔️ Correct and logical result.

---

## Key Takeaways

* JavaScript follows strict operator precedence rules
* Math operators run before comparisons
* Assignment runs right to left
* Parentheses override everything
* When in doubt → **use parentheses**
