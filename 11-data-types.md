# JavaScript Fundamentals: Data Types

## Introduction

In the last lecture, we talked about **values and variables**.

Now, in every programming language, **values can have different types**, depending on the kind of data they hold.

We’ve already seen:

* **Numbers**
* **Strings**

But JavaScript has **more data types**, and in this lecture we’ll look at **all of them**, focusing especially on **primitive data types**.

---

## Objects vs Primitive Values

In JavaScript, **every value** is either:

* an **object**, or
* a **primitive value**

Objects are more complex structures, and we’ll learn about them later.

For now, we’ll focus only on **primitive data types**.

---

## The 7 Primitive Data Types in JavaScript

JavaScript has **seven primitive data types**:

1. `number`
2. `string`
3. `boolean`
4. `undefined`
5. `null`
6. `symbol`
7. `bigint`

Let’s go through them one by one.

---

## 1. Number

The **number** type is used for all numeric values.

```javascript
23
```

### Important Detail

In JavaScript:

* **All numbers are floating-point numbers**
* Even integers like `23` are internally stored as `23.0`

```javascript
23 === 23.0 // true
```

Unlike many other languages:

* There is **no separate integer type**
* All numbers are simply of type `number`

---

## 2. String

A **string** is a sequence of characters, used for text.

```javascript
"Jonas"
'Hello World'
```

### Rules for Strings

* Strings **must be inside quotes**
* You can use **single** or **double** quotes
* Without quotes, JavaScript thinks it’s a variable name

❌ Wrong:

```javascript
Jonas
```

✅ Correct:

```javascript
"Jonas"
```

---

## 3. Boolean

The **boolean** type represents logical values.

A boolean can be **only one of two values**:

* `true`
* `false`

```javascript
true
false
```

Booleans are mainly used to:

* Make decisions in code
* Control program logic

We’ll see much more of this later.

---

## The Most Important Data Types

The three most commonly used data types are:

* **number**
* **string**
* **boolean**

However, JavaScript also has four more primitive types, which can be a bit confusing at first.

---

## 4. Undefined

`undefined` is the value of a variable that:

* Has been declared
* But **has not been assigned a value**

Example:

```javascript
let children;
```

```javascript
console.log(children);
```

Output:

```text
undefined
```

### Meaning of `undefined`

* It represents an **empty value**
* JavaScript assigns it automatically

---

## 5. Null

`null` also represents an empty value.

* It means **“nothing”**
* It is used intentionally by the developer
* It’s similar to `undefined`, but used in different situations

For now:
👉 Just know that **`null` exists** — we’ll discuss the details later.

---

## 6. Symbol (ES2015)

* Introduced in **ES2015**
* Represents a **unique and immutable value**
* Rarely used in beginner-level JavaScript

We’ll briefly revisit this near the end of the course.

---

## 7. BigInt (ES2020)

* Introduced in **ES2020**
* Used for **very large integers**
* Numbers that are too big for the normal `number` type

We’ll cover this in a later section.

---

## Summary of Primitive Types

| Type      | Description                        |
| --------- | ---------------------------------- |
| number    | All numeric values                 |
| string    | Text                               |
| boolean   | true / false                       |
| undefined | Variable declared but not assigned |
| null      | Intentional empty value            |
| symbol    | Unique, immutable value            |
| bigint    | Very large integers                |

---

## Dynamic Typing in JavaScript

JavaScript uses **dynamic typing**.

### What This Means

* You **do not declare data types manually**
* JavaScript automatically determines the type
* **The value has a type, not the variable**

Example:

```javascript
let x = 23;     // number
x = "Jonas";   // string
```

This is completely valid in JavaScript.

---

## Why This Matters

Dynamic typing is:

* Very flexible
* Very powerful

But it can also:

* Lead to hard-to-find bugs if you’re not careful

---

## Comments in JavaScript

### Single-Line Comments

```javascript
// This is a comment
```

Anything after `//` is ignored by JavaScript.

Used to:

* Explain code
* Divide code into sections
* Temporarily disable code

---

### Commenting Out Code

```javascript
// console.log(40 + 8 + 23 - 10);
```

The code won’t run, but it’s not deleted.

Shortcut in VS Code:

* **Mac:** `Cmd + /`
* **Windows:** `Ctrl + /`

---

### Multi-Line Comments

```javascript
/*
This is a multi-line comment.
Everything here is ignored.
*/
```

Used to:

* Disable large blocks of code
* Keep previous code as reference

---

## The `typeof` Operator

JavaScript provides the `typeof` operator to check data types.

```javascript
typeof true
```

To see the result:

```javascript
console.log(typeof true);
```

Output:

```text
boolean
```

---

### More Examples

```javascript
console.log(typeof 23);
console.log(typeof "Jonas");
```

Output:

```text
number
string
```

---

## Booleans in Variables

```javascript
let javaScriptIsFun = true;
console.log(javaScriptIsFun);
```

Output:

```text
true
```

Remember:

* The **value** has the type
* The **variable** just stores it

---

## Dynamic Typing in Action

```javascript
let javaScriptIsFun = true;
javaScriptIsFun = "Yes!";
```

What happened?

* The variable was **not recreated**
* The value inside it was **replaced**
* The type changed from `boolean` to `string`

This is dynamic typing.

---

## Undefined in Practice

```javascript
let year;
console.log(year);
console.log(typeof year);
```

Output:

```text
undefined
undefined
```

Key point:

* `undefined` is **both the value and the type**

---

### Reassigning an Undefined Variable

```javascript
year = 1991;
console.log(typeof year);
```

Output:

```text
number
```

Again, dynamic typing in action.

---

## The `typeof null` Bug (Important!)

```javascript
console.log(typeof null);
```

Output:

```text
object
```

⚠️ This is a **known bug in JavaScript**.

* `null` is **not** an object
* This behavior exists for legacy reasons
* It will never be fixed

👉 Always remember this quirk when using `typeof`.

---

## Final Recap

* JavaScript has **7 primitive data types**
* The most important are:

  * number
  * string
  * boolean
* JavaScript uses **dynamic typing**
* The **value** has a type, not the variable
* Comments help explain and control code
* `typeof` helps inspect data types (with one famous bug)

