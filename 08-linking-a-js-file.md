# Writing JavaScript in Files and Running It in the Browser

## Introduction

Now that we understand **what JavaScript is**, let’s learn how to:

* Write JavaScript in a **real file**
* Connect it to an **HTML document**
* Run the code in the **browser**

This is a big step, because this is how real JavaScript development actually works.

---

## Downloading the Starter Code

To get started with this course, you first need to download the **starter code** from the GitHub repository created for the course.

### How to Download

1. Go to the course GitHub repository (linked at the very beginning of the course)
2. Click the **green button**
3. Choose **Download ZIP**

> GitHub’s design may change over time, but you should always look for a green button that allows you to download the repository as a ZIP file.

### If the Green Button Is Not Visible

* On smaller screens or mobile devices, the button may not appear
* In that case, scroll down to the **FAQ section**
* Use the direct download link provided there

📌 **Important:**
Make sure to read through the FAQ section before continuing with the course. Many common questions are already answered there.

---

## Understanding the Starter Code Structure

After downloading, extract the ZIP file.

Inside, you’ll see:

* One folder per **section or project**
* Each section contains:

  * a **starter** folder
  * a **final** folder

### Starter vs Final

* **Starter folder:**
  The starting point for your work in each section
* **Final folder:**
  The finished code as it should look at the end

👉 If something goes wrong while coding, you can compare your code with the **final** version to find and fix mistakes.

For now, we’ll work only with the **starter** folder.

---

## Opening the Project in VS Code

1. Open **VS Code**
2. Create a **new window**
3. Click **Open Folder**
4. Select the **starter folder**
5. Click **Open**

Inside, you’ll see an `index.html` file.

---

## Why We Need HTML

JavaScript is usually attached to an **HTML document**, especially when building **front-end applications**.

That means:

* JavaScript code runs **because** it’s connected to HTML
* We always need an HTML file as a starting point

---

## Adding JavaScript with a `<script>` Tag

In HTML, JavaScript is written inside a `<script>` tag.

For now, we’ll write JavaScript **directly inside the HTML file** (this is called an *inline script*).

### Example: Inline JavaScript in HTML

```html
<script>
  let JS = "amazing";

  if (JS === "amazing") {
    alert("JavaScript is fun");
  }
</script>
```

### Notes

* Semicolons (`;`) mark the end of a line

  * They’re not mandatory, but they’re considered good practice
* Don’t worry yet about how the code works — just focus on writing and running it

---

## Running the Code in the Browser

To execute the JavaScript:

1. Open `index.html` in **Google Chrome**
2. The alert appears immediately:

   > **JavaScript is fun**

This confirms:

* JavaScript is correctly attached
* The browser is executing the code

Reloading the page will show the alert again.

---

## Viewing the Page Content

The text shown on the page comes from the HTML, for example:

```html
<h1>JavaScript Fundamentals – Part 1</h1>
```

This confirms:

* You opened the correct file
* Both HTML and JavaScript are working

---

## Using the Editor and Browser Side by Side

For a better workflow:

* Place **VS Code on one side**
* Place **Chrome on the other**
* Hide the sidebar in VS Code using:

  * `Ctrl + B` (Windows)
  * `Cmd + B` (Mac)

---

## Why Calculations Don’t Show Automatically

Let’s add a calculation:

```javascript
40 + 8 + 23 - 10;
```

After saving and reloading:

* No alert
* No visible output on the page
* Nothing in the console

### Why?

* The browser console only auto-displays results **when you type directly into it**
* JavaScript files do **not** show results automatically

---

## Displaying Output with `console.log`

To show results in the console, you must explicitly tell JavaScript to do so.

```javascript
console.log(40 + 8 + 23 - 10);
```

After saving and reloading:

* Open **Developer Tools → Console**
* The result appears
* Chrome shows the file name and line number (e.g. `index.html:31`)

### Key Concept

* The console is a **separate environment**
* `console.log()` creates a “bridge” from your script to the browser console

---

## Inline Script vs External Script

Right now, the JavaScript lives **inside the HTML file**.

This is called an **inline script**.

### Downsides of Inline Scripts

* Poor separation of concerns
* Harder to maintain
* Not scalable for real projects

👉 Best practice is to use **external JavaScript files**.

---

## Creating an External JavaScript File

1. Create a new file called:

```
script.js
```

2. Move your JavaScript code into it:

```javascript
let JS = "amazing";

if (JS === "amazing") {
  alert("JavaScript is fun");
}

console.log(40 + 8 + 23 - 10);
```

VS Code may auto-format the file — that’s normal and helpful.

---

## Linking the JavaScript File to HTML

Now the HTML file needs to know where the JavaScript lives.

At the **end of the `<body>`**, add:

```html
<script src="script.js"></script>
```

### Important Details

* The file name must match exactly
* The JavaScript file must be in the **same folder** as `index.html`
* No code goes inside this `<script>` tag

---

## Final Result

After saving and reloading:

* Alert appears ✔️
* Console output appears ✔️

If nothing happens:

* Check file names
* Check spelling (`script`, `src`)
* Check for JavaScript errors
* Ensure both files are in the same folder

---

## Clean Separation of Concerns

Now you have:

* **HTML** → structure and content
* **JavaScript** → logic and behavior

This setup is:

* Cleaner
* Easier to maintain
* The standard way real projects are built

---

## Summary

You now know how to:

* Download and use starter code
* Open a project in VS Code
* Write JavaScript in files
* Link JavaScript to HTML
* Run code in the browser
* Output results using `console.log`

