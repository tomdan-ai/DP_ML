# 🧩 DOM Manipulation in JavaScript — A Complete Beginner's Guide

---

## 🎯 **Lesson Objective**

By the end of this lesson, you'll understand:

* What the **DOM (Document Object Model)** is
* How to **select**, **modify**, **create**, and **remove** HTML elements
* How to **handle events** and make your web page **interactive**

---

## 🏗️ 1. What Is the DOM?

The **Document Object Model (DOM)** is a tree-like representation of your web page.
Each HTML element becomes a **node** that JavaScript can access and manipulate.

👉 Think of it like this:

```html
<html>
  <body>
    <h1>Hello World!</h1>
    <p>This is my first DOM lesson.</p>
  </body>
</html>
```

Becomes something like:

```
Document
 └── html
      └── body
           ├── h1
           └── p
```

So when you use JavaScript to access or change `h1`, you're talking to the DOM.

---

## 🧭 2. Selecting Elements

To manipulate elements, you first need to **select** them.

### ✅ Common Selection Methods:

```js
// Select by ID
const heading = document.getElementById("main-title");

// Select by class
const items = document.getElementsByClassName("list-item");

// Select by tag
const paragraphs = document.getElementsByTagName("p");

// Select using modern query selectors
const firstButton = document.querySelector("button");
const allButtons = document.querySelectorAll("button");
```

🧠 **Tip:**
`querySelector()` returns the **first match**
`querySelectorAll()` returns **all matches** (a NodeList you can loop through).

---

## ✏️ 3. Changing Content and Attributes

Once you've selected an element, you can change its **text**, **HTML**, or **attributes**.

### Example:

```html
<h1 id="main-title">Old Title</h1>
```

```js
const title = document.getElementById("main-title");

// Change text
title.textContent = "New Title using textContent";

// Change inner HTML (can add tags)
title.innerHTML = "<span style='color:blue'>New <b>Styled</b> Title</span>";

// Change attributes
title.setAttribute("class", "highlight");
```

🧠 **Tip:**
Use `.textContent` when you only want to insert text (safer).
Use `.innerHTML` only when you're intentionally inserting HTML.

---

## 🎨 4. Styling Elements

You can change CSS styles directly using the `.style` property:

```js
const box = document.querySelector(".box");

box.style.backgroundColor = "purple";
box.style.color = "white";
box.style.padding = "20px";
box.style.borderRadius = "10px";
```

Or toggle classes dynamically (cleaner!):

```js
box.classList.add("active");
box.classList.remove("hidden");
box.classList.toggle("dark-mode");
```

---

## 🧱 5. Creating and Removing Elements

You can **create**, **insert**, or **delete** elements dynamically.

### Example:

```js
// Create a new element
const newItem = document.createElement("li");
newItem.textContent = "New list item";

// Add it to an existing list
const list = document.querySelector("ul");
list.appendChild(newItem);

// Remove an element
const oldItem = document.querySelector("li:first-child");
oldItem.remove();
```

Other useful methods:

* `append()` – adds inside at the end
* `prepend()` – adds inside at the beginning
* `before()` / `after()` – adds outside before or after the element

---

## 🖱️ 6. Handling Events

You can make your page **interactive** by responding to user actions like clicks or key presses.

### Example:

```html
<button id="changeBtn">Change Color</button>
<p id="message">Click the button to change my color!</p>
```

```js
const button = document.getElementById("changeBtn");
const message = document.getElementById("message");

button.addEventListener("click", () => {
  message.style.color = "green";
  message.textContent = "Color changed!";
});
```

🧠 **Why `addEventListener()`?**
It's the preferred way to attach events — you can add multiple listeners and remove them later.

---

## 🔁 7. Traversing the DOM

Sometimes you need to move **up**, **down**, or **across** the DOM tree.

```js
const parent = document.querySelector(".container");
const firstChild = parent.firstElementChild;
const lastChild = parent.lastElementChild;

// Move to parent
const child = document.querySelector(".item");
const parentOfChild = child.parentElement;

// Move to siblings
const next = child.nextElementSibling;
const prev = child.previousElementSibling;
```

---

## 🧠 8. Real-World Example: Dynamic To-Do List

Let's combine what we've learned!

```html
<input type="text" id="todoInput" placeholder="Add a task">
<button id="addBtn">Add</button>
<ul id="todoList"></ul>
```

```js
const input = document.getElementById("todoInput");
const button = document.getElementById("addBtn");
const list = document.getElementById("todoList");

button.addEventListener("click", () => {
  const task = input.value.trim();
  if (task === "") return;

  const li = document.createElement("li");
  li.textContent = task;

  li.addEventListener("click", () => {
    li.style.textDecoration = "line-through";
  });

  list.appendChild(li);
  input.value = "";
});
```

✅ Features:

* Adds new items dynamically
* Strikes through completed tasks
* Teaches creation, event handling, and styling

---

## 🧹 9. Best Practices

* ✅ Use `.textContent` for safe text updates
* ⚠️ Avoid frequent DOM updates in loops — batch them or use fragments
* 🧩 Use `classList` instead of inline styles for maintainable design
* 🧼 Remove event listeners when elements are removed to prevent memory leaks

---

## 🏁 10. Summary

You've learned how to:

* Access the DOM
* Change text, HTML, and styles
* Add and remove elements
* Handle user events
* Traverse the DOM tree

With this, you can **build interactive web pages without any framework** — and truly understand how tools like React, Vue, and Angular work under the hood.

---

## 📚 Next Steps

* Practice each example in the browser console
* Build a small project combining multiple concepts
* Explore the MDN Web Docs for deeper learning
