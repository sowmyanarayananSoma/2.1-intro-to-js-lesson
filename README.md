# JavaScript Fundamentals Lesson Plan

## 1. Introduction to JavaScript

### 🧠 What Is JavaScript?

JavaScript is a **programming language** that makes web pages **interactive and dynamic**.

If a web page *responds* when you click, type, scroll, or move the mouse — that’s JavaScript at work.

---

### 🧩 How It Fits with HTML and CSS

Think of a website like a person:

| Layer | Role | Analogy |
| --- | --- | --- |
| **HTML** | Gives structure and content — the text, headings, images, buttons | 🦴 **Skeleton** |
| **CSS** | Adds color, spacing, and layout to make it look nice | 👕 **Clothes** |
| **JavaScript** | Makes it *move* and *react* — it listens and responds to user actions | 🧠 **Brain and muscles** |

So, when you click a button and something happens, that’s JavaScript telling the browser *how to react*.

---

### 🖥️ Example

```html
<button onclick="alert('Hello!')">Click Me</button>

```

- **HTML:** Creates the button
- **CSS:** Defines appearance
- **JavaScript:** Defines behavior when clicked

Without JavaScript, a website only displays information.

With JavaScript, it can *do* things — like show messages, update data, or react instantly.

---

## 2. Inline, Internal, and External JavaScript

### 1️⃣ Inline JavaScript

**Definition:** JavaScript code written **directly inside an HTML element’s tag** using attributes like `onclick`.

```html
<button onclick="alert('Hello!')">Click Me</button>

```

**Pros:** Quick, simple for testing.

**Cons:** Messy and unscalable.

**Use case:** For very small demos or quick tests.

---

### 2️⃣ Internal JavaScript

**Definition:** Code written inside a `<script>` tag within the HTML file.

```html
<!DOCTYPE html>
<html>
<body>
  <button onclick="sayHello()">Click Me</button>
  <script>
    function sayHello() {
      alert("Hello from internal JavaScript!");
    }
  </script>
</body>
</html>

```

**Pros:** Simple, all-in-one.

**Cons:** Not reusable for multiple pages.

**Use case:** For small projects or practice.

---

### 3️⃣ External JavaScript

**Definition:** JavaScript stored in a separate `.js` file and linked using `<script src="">`.

**index.html**

```html
<script src="script.js"></script>

```

**script.js**

```jsx
function sayHello() {
  alert("Hello from external JavaScript!");
}

```

**Pros:** Clean, reusable, ideal for large projects.

---

## 3. Variables and Data Types

### 🎯 Objectives

By the end of this section, learners can:

1. Create variables using `var`, `let`, and `const`.
2. Identify basic JavaScript data types.
3. Use `console.log()` and `window.alert()`.
4. Test code in the browser console.

---

### 🧰 Setup

- Use **VS Code or Windsurf** with `variables.html`.
- Open browser console (Inspect → Console).
- Keep browser and code editor visible.

---

### Step 1: Console & Messages

**Concept:** The browser console is like a sandbox for testing JavaScript.

```html
<script>
window.alert("Hello!");
console.log("Hello from console!");
</script>

```

- `alert()` shows a pop-up.
- `console.log()` prints messages inside DevTools.

**Student Task:** Type both commands in the console and compare.

---

### Step 2: Variables and Data Types

### 🧠 Concept

Variables store data for reuse — like labeled boxes.

```jsx
let name = "Soma";
let age = 32;
let isStudent = true;
console.log(name, age, isStudent);

```

### Data Types

| Type | Example | Description |
| --- | --- | --- |
| Number | `42` | Numeric values |
| String | `'Hello'` | Text |
| Boolean | `true` | True/false |
| Undefined | `let x;` | Not assigned |
| Null | `let y = null;` | Empty on purpose |

**Demo:**

```jsx
console.log(typeof 42); // number
console.log(typeof "Hello"); // string
console.log(typeof true); // boolean
console.log(typeof undefined); // undefined
console.log(typeof null); // object (quirk)

```

---

### Updating Variables

```jsx
let color = "blue";
color = "green";
console.log(color);

```

---

### var vs let vs const

```jsx
var city = "Toronto";
let country = "Canada";
const continent = "North America";

```

**Guideline:**

- `var` → old, avoid.
- `let` → changeable.
- `const` → fixed.

> “Start with const; switch to let if needed.”
> 

---

### Mini Exercise

```jsx
let firstName = "Alex";
let lastName = "Ramos";
let fullName = firstName + " " + lastName;
console.log(fullName);

```

**Ask:** What happens when you mix strings and numbers?

---

### JavaScript Identifiers

Rules:

- Can include letters, digits, `_`, `$`.
- Must begin with a letter, `_`, or `$`.
- Case-sensitive.
- Cannot use reserved words.

Examples:

```jsx
let _lastName = "Johnson";
let _x = 2;

```

Preferred Casing:

- **camelCase** → variables
- **SCREAMING_SNAKE_CASE** → constants

---

### Practice Activity

```jsx
const hobby = "Hiking";
let hoursPerWeek = 5;
let lovesNature = true;
console.log(hobby, hoursPerWeek, lovesNature);

```

---

### Wrap-Up Points

- Variables store and reuse info.
- Use `let` for changeable, `const` for fixed.
- Test with the console.

---

### Optional Challenge

```html
<p id="output"></p>
<script>
let username = prompt("What’s your name?");
document.getElementById("output").innerText = `Welcome, ${username}!`;
</script>

```

Shows how JavaScript can update HTML.

---

## 4. Operators and Expressions

### 🎯 Objectives

Learners will:

1. Explain operators and expressions.
2. Use arithmetic, comparison, and logical operators.
3. Predict expression results.

---

### Step 1: What Are Operators and Expressions

**Concept:** Symbols that perform operations on values.

```jsx
console.log(2 + 3);
console.log("Hello " + "World");

```

Expression = values + operators → result.

---

### Step 2: Arithmetic Operators

| Operator | Name | Example | Result |
| --- | --- | --- | --- |
| + | Addition | `5 + 3` | 8 |
| - | Subtraction | `5 - 3` | 2 |
| * | Multiplication | `5 * 3` | 15 |
| / | Division | `6 / 3` | 2 |
| % | Modulus | `7 % 3` | 1 |
| ** | Exponentiation | `2 ** 3` | 8 |

**Demo:**

```jsx
let x = 10, y = 3;
console.log("Add:", x + y);
console.log("Subtract:", x - y);

```

---

### Step 3: Comparison and Logical Operators

### Comparison

| Operator | Meaning | Example | Result |
| --- | --- | --- | --- |
| == | Equal (value) | `5 == "5"` | true |
| === | Strict Equal | `5 === "5"` | false |
| != | Not Equal | `3 != 5` | true |
| !== | Strict Not Equal | `3 !== "3"` | true |
| > | Greater than | `8 > 6` | true |
| < | Less than | `2 < 1` | false |
| >= | Greater or Equal | `6 >= 6` | true |
| <= | Less or Equal | `4 <= 3` | false |

**Demo:**

```jsx
let a = 5, b = "5";
console.log(a == b);  // true
console.log(a === b); // false

```

> Always prefer === for predictable comparisons.
> 

---

### Logical

| Operator | Meaning | Example | Result |
| --- | --- | --- | --- |
| && | AND | `true && false` | false |
|  |  |  | OR |
| ! | NOT | `!true` | false |

**Demo:**

```jsx
let age = 20;
let hasID = true;
console.log(age >= 18 && hasID); // true
console.log(age >= 18 || hasID); // true
console.log(!hasID); // false

```

---

### Mini Challenge

```jsx
let num = 7;
console.log(num > 0 && num <= 10);

```

Predict what happens for 12 or 0.

---

### Wrap-Up Points

- **Arithmetic:** performs math.
- **Comparison:** returns true/false.
- **Logical:** combines boolean values.
- Always test expressions in the console.

---

✅ **End of Lesson Summary:**

Students now understand how JavaScript adds logic, interactivity, and intelligence to web pages through variables, operators, and expressions.
