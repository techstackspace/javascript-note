# JavaScript Fundamentals: Values and Variables

## Introduction

Welcome back.

Now we’ll start **really learning the JavaScript language**, beginning with **values and variables**.

Before we begin, let’s clean up some existing code:

* Remove code that isn’t doing anything
* Remove alert popups so they don’t interrupt us constantly

Throughout this section, we’ll use **people-related examples** (names, ages, jobs) to keep things intuitive.

---

## What Is a Value?

A **value** is a piece of data.
It’s the **most fundamental unit of information** in programming.

### Examples of Values

```javascript
"Jonas"
```

This text is a value.

To see it in the console:

```javascript
console.log("Jonas");
```

Reloading the page prints:

```
Jonas
```

Another value:

```javascript
23
```

```javascript
console.log(23);
```

You’ll see:

```
23
```

### Values in Expressions

```javascript
40 + 8 + 23 - 10
```

Here:

* `40`, `8`, `23`, and `10` are all **values**
* The operators combine them into a **new value**
* The final value is `61`

👉 A **value** is the smallest unit of information in JavaScript.

---

## What Is a Variable?

One of the most powerful things we can do with values is **store them in variables**.

### Declaring a Variable

```javascript
let firstName = "Jonas";
```

This is called **declaring a variable**.

What happens here:

* A variable named `firstName` is created in memory
* The value `"Jonas"` is stored inside it

This is exactly what we did earlier with:

```javascript
let JS = "amazing";
```

---

## Variables as Boxes (Mental Model)

Think of a variable as a **box**:

* The **label** on the box is the variable name
* The **content** of the box is the value

So here:

* Box label: `firstName`
* Value inside: `"Jonas"`

Whenever we use the label, JavaScript gives us the value.

---

## Using Variables

```javascript
console.log(firstName);
```

Output:

```
Jonas
```

If we change the value:

```javascript
let firstName = "Bob";
console.log(firstName);
```

Output:

```
Bob
```

Change it back:

```javascript
let firstName = "Jonas";
```

---

## Reusing Variables

```javascript
console.log(firstName);
console.log(firstName);
console.log(firstName);
```

Every time JavaScript sees `firstName`, it replaces it with `"Jonas"`.

### Why This Is Powerful

If we change the value **once**:

```javascript
let firstName = "Matilda";
```

All references update automatically.

Without variables, we’d have to change the value **everywhere manually**.

👉 This is one of the biggest advantages of variables.

---

## Variable Naming Conventions

### camelCase (JavaScript Standard)

```javascript
let firstName;
let myFirstJob;
let currentJob;
```

* First word: lowercase
* Each new word: uppercase first letter
* This is the **standard convention in JavaScript**

---

### Alternative Style (Not Common in JavaScript)

```javascript
let first_name;
```

This style is common in languages like Ruby or Python, but **camelCase is preferred in JavaScript**.

---

## Rules for Naming Variables (Hard Rules)

### ❌ Cannot Start With a Number

```javascript
let 3years = 3; // ❌ Syntax Error
```

Error:

* **SyntaxError: Invalid or unexpected token**

---

### ✅ Allowed Characters

Variable names can contain:

* Letters
* Numbers
* `_` (underscore)
* `$` (dollar sign)

❌ Not allowed:

```javascript
let Jonas&Matilda = "JM"; // ❌
```

Error:

* `&` is not allowed in variable names

✅ Allowed:

```javascript
let Jonas_Matilda = "JM";
```

---

## Reserved JavaScript Keywords

Some words are **reserved** and cannot be used as variable names.

❌ Examples:

```javascript
let new = 27;
let function = 5;
```

These cause syntax errors because:

* `new` and `function` are JavaScript keywords

✅ Workarounds:

```javascript
let _new = 27;
let $function = 5;
```

---

### The Special Case of `name`

```javascript
let name = "Jonas";
```

This is technically allowed, but:

* It can cause problems
* It’s better to avoid it

✅ Better:

```javascript
let firstName = "Jonas";
```

---

## Uppercase Variable Names

### ❌ Not for Regular Variables

```javascript
let Person = "Jonas"; // Not illegal, but discouraged
```

Uppercase variable names are usually reserved for:

* Object-oriented programming concepts (later in the course)

---

### ✅ Constants in Uppercase

```javascript
let PI = 3.1415;
```

Why uppercase?

* The value will **never change**
* This is a widely accepted convention

VS Code even highlights these differently because it recognizes the pattern.

---

## Descriptive Variable Names (Very Important)

### ❌ Bad Example

```javascript
let job1 = "programmer";
let job2 = "teacher";
```

This tells us almost nothing.

---

### ✅ Good Example

```javascript
let myFirstJob = "programmer";
let myCurrentJob = "teacher";
```

Now it’s immediately clear:

* What the value represents
* Why it exists

👉 Always aim for **clarity over brevity**.

---

## Final Recap: What Is a Variable?

A variable is:

* A **box**
* With a **name (label)**
* That stores a **value**

Example:

```javascript
let myFirstJob = "programmer";
console.log(myFirstJob);
```

Output:

```
programmer
```

If we change it once:

```javascript
myFirstJob = "coder";
```

The change applies everywhere the variable is used.

---

## Key Takeaway

Variables are:

* One of the **most important concepts in programming**
* Essential for writing clean, maintainable code

👉 Make sure you truly understand values and variables before moving on — everything else builds on them.
