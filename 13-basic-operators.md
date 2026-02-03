# JavaScript Fundamentals: Basic Operators

## What Is an Operator?

An **operator** allows us to:

* Transform values
* Combine multiple values
* Perform work with values

JavaScript has many categories of operators, including:

* Arithmetic (mathematical) operators
* Assignment operators
* Comparison operators
* Logical operators (later)
* And more

In this lecture, we focus on the **most important basic operators**.

---

## Arithmetic (Mathematical) Operators

Arithmetic operators are used to perform math calculations.

### Common Arithmetic Operators

| Operator | Meaning        |
| -------- | -------------- |
| `+`      | Addition       |
| `-`      | Subtraction    |
| `*`      | Multiplication |
| `/`      | Division       |
| `**`     | Exponentiation |

---

### Example: Calculating Age

```javascript
const now = 2037;

const ageJonas = now - 1991;
console.log(ageJonas);
```

**Output:**

```
46
```

Jonas is 46 years old in the year 2037.

---

### Calculating Another Person’s Age

```javascript
const ageSarah = now - 2018;
console.log(ageJonas, ageSarah);
```

**Output:**

```
46 19
```

Here we logged **multiple values** in a single `console.log` by separating them with commas.

---

### Why Variables Matter (Avoid Repetition)

Instead of repeating `2037` multiple times, we store it in a variable:

```javascript
const now = 2037;
const ageJonas = now - 1991;
const ageSarah = now - 2018;
```

This way:

* We avoid duplicated values
* We only change the year in one place if needed

---

### More Arithmetic Examples

```javascript
console.log(
  ageJonas * 2,
  ageJonas / 10,
  2 ** 3
);
```

**Explanation:**

* `ageJonas * 2` → multiplication
* `ageJonas / 10` → division
* `2 ** 3` → exponentiation (2 × 2 × 2)

**Output:**

```
92 4.6 8
```

---

## The `+` Operator with Strings (Concatenation)

The `+` operator is also used to **join strings**.

```javascript
const firstName = "Jonas";
const lastName = "Schmedtmann";

console.log(firstName + lastName);
```

**Output:**

```
JonasSchmedtmann
```

---

### Adding a Space Between Strings

```javascript
console.log(firstName + " " + lastName);
```

**Output:**

```
Jonas Schmedtmann
```

This process is called **string concatenation**.

> There’s a better modern way using template strings — covered later.

---

## Assignment Operators

### Basic Assignment (`=`)

```javascript
let x = 10 + 5;
console.log(x);
```

**Output:**

```
15
```

* `+` runs first
* Then `=` assigns the result to `x`

---

### Compound Assignment Operators

#### Addition Assignment (`+=`)

```javascript
x += 10;
// same as: x = x + 10
```

If `x` was 15, now it becomes:

```
25
```

---

#### Multiplication Assignment (`*=`)

```javascript
x *= 4;
// same as: x = x * 4
```

If `x` was 25:

```
100
```

---

### Increment and Decrement Operators

#### Increment (`++`)

```javascript
x++;
```

Same as:

```javascript
x = x + 1;
```

#### Decrement (`--`)

```javascript
x--;
x--;
```

If `x` was 101, it becomes:

```
99
```

---

## Comparison Operators

Comparison operators are used to **produce Boolean values** (`true` or `false`).

### Common Comparison Operators

| Operator | Meaning               |
| -------- | --------------------- |
| `>`      | Greater than          |
| `<`      | Less than             |
| `>=`     | Greater than or equal |
| `<=`     | Less than or equal    |

---

### Example: Comparing Ages

```javascript
console.log(ageJonas > ageSarah);
```

**Output:**

```
true
```

This asks:

> “Is Jonas older than Sarah?”

Answer: **Yes → true**

---

### Checking Full Age (18+)

```javascript
console.log(ageSarah >= 18);
```

* If Sarah is **18 or older**, result is `true`
* If she’s **younger than 18**, result is `false`

#### Example Changes

```javascript
const ageSarah = now - 2020;
console.log(ageSarah >= 18);
```

**Output:**

```
false
```

---

## Storing Comparison Results

Instead of logging directly, we usually store results in variables:

```javascript
const isFullAge = ageSarah >= 18;
```

This variable now holds a **Boolean value**.

VS Code even recognizes it as a Boolean automatically.

---

## Combining Math and Comparisons

We can do everything in one line:

```javascript
console.log(
  now - 1991 > now - 2018
);
```

This works because JavaScript:

1. Calculates both ages
2. Then compares the results

This raises an important question:

👉 **How does JavaScript know what to calculate first?**

That’s handled by **operator precedence**, which is exactly what the **next lecture** is about.

---

## Key Takeaways

* Operators transform or combine values
* Arithmetic operators handle math
* `+` also concatenates strings
* Assignment operators modify variables
* Comparison operators return Booleans
* JavaScript evaluates expressions in a specific order
