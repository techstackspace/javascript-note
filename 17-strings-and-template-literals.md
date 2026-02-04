# JavaScript Fundamentals: Template Literals (Strings)

## Why Strings Matter

Strings are a **core building block** of programming.
In JavaScript, we often need to **build strings dynamically** by combining text with variables and calculations.

---

## Setting Up the Example

Let’s start by creating some variables describing a person:

```javascript
const firstName = 'Jonas';
const job = 'teacher';
const birthYear = 1991;
const year = 2037;
```

We want to build a sentence like:

> *I'm Jonas, a 46 year old teacher!*

---

## Old Way: String Concatenation with `+`

We already know that we can use the **plus (`+`) operator** to concatenate strings.

```javascript
const jonas =
  "I'm " +
  firstName +
  ', a ' +
  (year - birthYear) +
  ' years old ' +
  job +
  '!';

console.log(jonas);
```

### Important Details

* **Quotes matter**:

  * If you need a single quote inside the string (like `"I'm"`), you must wrap the string in **double quotes**
* Parentheses are needed here:

  ```javascript
  (year - birthYear)
  ```

  so the calculation happens **before** concatenation
* JavaScript automatically converts the number to a string (**type coercion**)

### Result

```text
I'm Jonas, a 46 years old teacher!
```

### Problem with This Approach

* Hard to read
* Easy to mess up spaces
* Too many `+` operators
* Hard to maintain for complex strings

---

## Modern Solution: Template Literals (ES6 / ES2015)

Template literals make string building **cleaner, safer, and more readable**.

### Syntax Rules

* Use **backticks** (`` ` ``), not quotes
* Insert variables or expressions using:

  ```javascript
  ${expression}
  ```

---

## Using Template Literals

```javascript
const jonasNew = `I'm ${firstName}, a ${year - birthYear} year old ${job}!`;
console.log(jonasNew);
```

### What’s Happening Here?

* `${firstName}` → replaced with `"Jonas"`
* `${year - birthYear}` → JavaScript expression (calculation allowed!)
* `${job}` → replaced with `"teacher"`

✔ No `+`
✔ No space juggling
✔ Much easier to read

---

## Debugging Tip

If something doesn’t work, **read the error message carefully**.

For example, this would be wrong:

```javascript
`I'm ${firstName}, a ${year - birthYear} year old teacher!`
```

Because `"teacher"` is not the variable — `job` is.

Correct version:

```javascript
`I'm ${firstName}, a ${year - birthYear} year old ${job}!`
```

---

## You Can Use Backticks for Any String

Template literals don’t *require* placeholders.

This works just fine:

```javascript
console.log(`Just a regular string`);
```

### Developer Preference

Some developers:

* Use backticks for **all strings**
* Avoid thinking about single vs double quotes
* Easily add variables later if needed

This is a **style choice** — both are valid.

---

## Multiline Strings (Huge Win 🚀)

### Before Template Literals (Old & Ugly)

```javascript
console.log('String with\n\
multiple\n\
lines');
```

This works only because of a **JavaScript quirk**, and it’s hard to read.

---

### With Template Literals (Clean & Natural)

```javascript
console.log(`String
with
multiple
lines`);
```

✔ No special characters
✔ Looks exactly like the output
✔ Extremely useful for HTML generation later

---

## Why Template Literals Are So Important

* Easier string assembly
* Supports expressions
* Great for debugging
* Perfect for HTML and UI work
* One of the **most-used ES6 features**

---

## Key Takeaways

* Use `+` only for very simple strings
* Prefer **template literals** for:

  * Dynamic strings
  * Readability
  * Multiline content
* Use `${}` to inject variables or calculations
* Backticks are powerful and flexible

