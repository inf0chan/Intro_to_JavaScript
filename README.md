# Intro to JavaScript

##  What is JavaScript?

JavaScript (JS) is a programming language that makes websites **interactive**. While HTML creates the structure and CSS adds the design, JavaScript adds the **behavior**.

With JavaScript, you can:

*  Create animations
*  Validate forms
*  Handle button clicks
*  Show popups
*  Build sliders and music players
*  Update webpage content without reloading

---

#  Features of JavaScript

* Lightweight and fast
* Runs directly inside the browser
* Works together with HTML and CSS
* Supports different programming styles
* Can be used for both Frontend and Backend development

---

#  JavaScript vs Java

| JavaScript                   | Java                                           |
| ---------------------------- | ---------------------------------------------- |
| Scripting language           | Programming language                           |
| Runs in browsers and Node.js | Runs on the Java Virtual Machine (JVM)         |
| Mostly used for websites     | Used for desktop, Android, and enterprise apps |
| Dynamically typed            | Statically typed                               |
| Prototype-based              | Class-based                                    |

> **Note:** JavaScript and Java are completely different languages.

---

#  What is the DOM?

DOM stands for **Document Object Model**.

It changes an HTML page into a tree of objects so JavaScript can access and control every element.

Using the DOM, JavaScript can:

* Find HTML elements
* Change text
* Change CSS styles
* Add or remove elements
* Respond to user actions

Example HTML:

```html
<h1>Hello World</h1>
```

Select it using JavaScript:

```javascript
document.querySelector("h1");
```

---

#  The `document` Object

The **document** object represents the whole webpage.

Examples:

```javascript
console.log(document);
console.log(document.title);
console.log(document.URL);
```

Change the page title:

```javascript
document.title = "My Website";
```

---

#  `document.body`

`document.body` gives access to the `<body>` section of the webpage.

Example:

```javascript
console.log(document.body);
```

Change the background color:

```javascript
document.body.style.backgroundColor = "lightblue";
```

---

#  Selecting HTML Elements

JavaScript provides different ways to find elements.

## `getElementById()`

Selects one element using its **id**.

HTML

```html
<h1 id="heading">Hello</h1>
```

JavaScript

```javascript
const heading = document.getElementById("heading");
```

---

## `getElementsByClassName()`

Selects all elements with the same class.

```javascript
const items = document.getElementsByClassName("item");
```

Returns an **HTMLCollection**.

---

## `getElementsByTagName()`

Selects all elements with the same tag.

```javascript
const paragraphs = document.getElementsByTagName("p");
```

Returns an **HTMLCollection**.

---

## `querySelector()`

Returns the **first matching element**.

By tag:

```javascript
document.querySelector("h1");
```

By class:

```javascript
document.querySelector(".box");
```

By id:

```javascript
document.querySelector("#heading");
```

---

## `querySelectorAll()`

Returns **all matching elements**.

```javascript
const boxes = document.querySelectorAll(".box");
```

Returns a **NodeList**.

Loop through all elements:

```javascript
boxes.forEach(box => {
    console.log(box);
});
```

---

# `querySelector()` vs `querySelectorAll()`

| `querySelector()`                  | `querySelectorAll()`          |
| ---------------------------------- | ----------------------------- |
| Returns the first matching element | Returns all matching elements |
| Returns one Element                | Returns a NodeList            |
| No loop needed                     | Usually used with a loop      |

---

# Reading Content

```javascript
const heading = document.querySelector("h1");

console.log(heading.innerText);
console.log(heading.textContent);
console.log(heading.innerHTML);
```

* **innerText** → Shows only visible text.
* **textContent** → Shows all text, even hidden text.
* **innerHTML** → Shows the HTML inside the element.

---

# Changing Content

Change text:

```javascript
document.querySelector("h1").innerText = "Welcome";
```

Add HTML:

```javascript
document.querySelector("p").innerHTML = "<b>Hello</b>";
```

---

# Changing CSS with JavaScript

```javascript
const heading = document.querySelector("h1");

heading.style.color = "blue";
heading.style.fontSize = "40px";
heading.style.backgroundColor = "yellow";
```

JavaScript can change CSS without editing the CSS file.

---

# Common `document` Methods

```javascript
document.getElementById()

document.getElementsByClassName()

document.getElementsByTagName()

document.querySelector()

document.querySelectorAll()

document.createElement()

document.appendChild()

document.remove()

document.removeChild()
```

---

# Key Takeaways

* JavaScript makes websites interactive.
* The **DOM** lets JavaScript control HTML.
* The **document** object represents the whole webpage.
* Use different selector methods to find HTML elements.
* `querySelector()` selects the first matching element.
* `querySelectorAll()` selects all matching elements.
* JavaScript can change text, styles, and even create or remove HTML elements dynamically.
