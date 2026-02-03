# Writing Your First JavaScript Code (Using the Browser Console)

## Introduction

In this lesson, we write our **very first line of JavaScript code**.

To get started as quickly as possible, we’ll use the **browser’s developer tools** instead of a code editor. In the next lesson, we’ll switch to the code editor that was installed earlier.

For now, everything will be done inside **Google Chrome**.

---

## Opening the Chrome Developer Tools

There are **three different ways** to open the Chrome Developer Tools. Use whichever feels most comfortable.

### Method 1: Keyboard Shortcut

* **Mac:** `Command + Option + J`
* **Windows:** `Ctrl + Alt + J`

This opens the **Console tab directly**, which is what we care about.

---

### Method 2: Right-Click Menu

1. Right-click anywhere on a webpage
2. Select **Inspect**
3. This opens the **Elements tab**
4. Switch to the **Console tab**

---

### Method 3: Chrome Menu

1. Open the Chrome menu
2. Go to **View → Developer → JavaScript Console**

This also takes you straight to the Console.

---

## The JavaScript Console

The Developer Tools contain many tabs, but for now, we’re only interested in the **Console**.

The JavaScript console allows us to:

* Write JavaScript code
* Run it immediately
* Test ideas quickly
* Debug errors during development

> ⚠️ Real applications are **not built in the console**, but it’s an excellent place to learn and experiment.

You can increase the font size using:

* **Mac:** `Command + +`
* **Windows:** `Ctrl + +`

---

## Writing Your First JavaScript Code

Let’s write our first line of JavaScript.

### Code Example: Alert Message

```javascript
alert("Hello world");
```

### Explanation

* `alert` is a **JavaScript function**
* The parentheses `()` are required
* `"Hello world"` is a **string** (plain text)
* There is **no space** between `alert` and the opening parenthesis

When you press **Enter**, JavaScript immediately evaluates the code and shows a popup with:

> **Hello world**

🎉 That’s your **first line of JavaScript code**.

---

## How the Console Works

Any code written in the console and executed by pressing **Enter**:

* Runs immediately
* Shows results right away
* Is great for experimentation

---

## Working with Variables and Conditions

Now let’s write some more JavaScript.
You don’t need to fully understand this yet — this is just a preview.

### Code Example: Variables and `if` Statement

```javascript
let JS = "amazing";

if (JS === "amazing") {
  alert("JavaScript is fun");
}
```

### What’s Happening Here?

* `let JS = "amazing";`
  → Creates a **variable** called `JS` and assigns it the value `"amazing"`

* `if (JS === "amazing")`
  → Checks whether `JS` is equal to `"amazing"`

* If the condition is true, JavaScript:
  → Displays an alert saying **“JavaScript is fun”**

When you press **Enter**, the alert appears.

---

## Changing the Variable Value

Now let’s change the value of `JS`.

```javascript
let JS = "boring";
```

Then run the same `if` statement again:

```javascript
if (JS === "amazing") {
  alert("JavaScript is fun");
}
```

### Result

* Nothing happens ❌

### Why?

* `JS` is now `"boring"`
* The condition `JS === "amazing"` is **false**
* Therefore, the alert does not run

---

## Re-running Previous Commands

You can scroll through previously executed commands by pressing:

* **Up Arrow (↑)** on your keyboard

This lets you quickly reuse or edit earlier code.

---

## Using the Console as a Calculator

The console can also perform **math operations**.

### Code Example: Math Expression

```javascript
40 + 8 + 23 - 10
```

### Result

JavaScript immediately returns the calculated value.

This shows that:

* The console can be used like a calculator
* It will become very useful later for testing logic and calculations

---

## Summary

In this lesson, you learned:

* How to open the **Chrome Developer Tools**
* How to use the **JavaScript console**
* How to write and run JavaScript code instantly
* Your first JavaScript command using `alert`
* Basic concepts like:

  * Strings
  * Variables
  * Conditions (`if`)
* How to use the console for quick math
