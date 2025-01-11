# JavaScript

_Duration: ~2 hr_

_Required Applications: NodeJS_

_Required Extension: Live Server_

## Reputation

**JavaScript** is currently one of the most popular and widely used programming languages. It is growing faster than any other language, with major companies like Netflix, Walmart, and PayPal.

> You can work as a front-end, back-end, or full-stack developer.

## What It Does

You can develop dynamic and interactive web applications, build server-side applications using frameworks like _Node.js_, create mobile apps, design games, and even develop desktop applications.

## Background

It was initially designed to run solely in web browsers, which is why each browser includes a JavaScript engine capable of executing JavaScript code.

For instance, Firefox uses the SpiderMonkey _JavaScript engine_, while Chrome uses _V8_. In _2009_, **Ryan Dahl**, an innovative engineer, embedded Chrome’s open-source JavaScript engine into a **C++** program, creating what is now known as Node.

In summary, JavaScript code can be executed either in a browser or in Node, both of which provide _a runtime environment_ for running JavaScript code.

## NodeJS

**Node** is `C++` program that includes Google's V8 JavaScript engine. Now with this, we can run JavaScript code outside of the browser. We can pass our our JavaScript code to Node for execution, and this means, with JavaScript, we can build the _backend_ for our web and mobile applications.

## ECMAScript

**ECMAScript** is a `specification` that JavaScript adheres to, defined by the standards organization ECMA. The first version was released in 1997, and since _2015_, they have been issuing annual updates with the newest specification, known as `ES2015` or `ES6`. This specification introduced numerous new features to JavaScript.

## JavaScript In Use

Each browser comes with a built-in _JavaScript engine_, allowing us to write and execute JavaScript code directly without needing any extra tools. This isn’t the approach used for building production application. It’s simply convenient for quick demonstrations.

Open Chrome, right-click on an empty space, and select **“Inspect”**. This will open the Developer Tools. Navigate to the **Console** tab, where you can write and execute any valid JavaScript code examples.

Enter the following:

![js-log-hello](images/js-log-hello.png)

You can also enter mathematical expressions here:

```
> 3 + 4
◀ 7
```

You can also use methods like:

```
> alert('hey') (Displays a popup dialog with the message)
◀ undefined
```

> The left-pointing arrow in the console shows the return value of the expression. If a function doesn’t return a value, it will return `undefined`.

## Course Setup

1. Begin by creating a folder named **‘training-js’**.

2. Within the folder, create an HTML file and name it _index.html_.

3. In the HTML file, do `!+tab` followed by the Tab key to generate a boilerplate document.

4. In the same folder, create a JavaScript file named _basics.js_.

## Script Placement (Internal)

In HTML, scripts can be added either within the `<head>` itself or in the `<body>` section.

```
<head>
    ...
    <title>Document</title>
    <script>
        ...
    </script>
</head>
```

> Third-party code or scripts can be added here as an exception.

### Ideal Placement

The browser parses the file from top to bottom.

Scripts in the `<head>` can block the rendering of elements, keeping the page occupied.

By placing scripts at the end, just before the closing `</body>` tag, elements are rendered first, and the scripts are executed afterward:

```
<body>
    ...
    <script>
        ...
    </script>
</body>
```

## File Reference (External)

To reference an external file, we need to add a **src** attribute to the `<script>` tag:

```
<script src="basics.js">
    ...
</script>
```

This informs the browser that our JavaScript code is located in the _basics.js_ file.

## Comment Expression

```
// We can add comments that JavaScript ignores during execution.
// Preceded by two forward slashes, they are solely for documenting.
// It helps other developers understand how the code is written.
```

> To understand more about comments, check out [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments) extension.

## Statement

Expresses an action to be performed.

Every statement must be ended with a semicolon `;`.

Add this line to our _basics.js_ file:

```
console.log("Hello JavaScript"); // My first JavaScript code
```

## Separation Of Concerns

In real-world applications, we often have thousands of lines of code.

We do not want to write all of that code inline here.

We want to **separate and extract** our JavaScript from the HTML code.

## Quick Recap

**HTML** is focused on content, while **JavaScript** controls how our web page behaves.

### JavaScript In Node

Node is a program that incorporates Google’s V8 JavaScript engine.

We can provide it with a piece of JavaScript code, and it will execute just like in a browser.

In the terminal, run:

```
node basics.js
> Hello JavaScript
```

## Variables

We use it to store data temporarily in the computer’s memory.

We store the data in a location and assign it a name.

With this name, we can retrieve the data from a specific location in the future.

### Previously, Before ES6

We use the `var` keyword to declare a variable.

> The best practice is to use the `const/let` keyword to declare a variable.

> By default, the value of a variable is undefined.

```
let name = "Adrian";
console.log(name);
```

<details>
  <summary>More on var, let, const</summary>

**var**

- Used in the earlier versions.
- Non-blocking, available anywhere within the document or function.

**let**

- Used in 2015, ES6.
- Block Scope, has scope only within the block where it is declared.

**const**

- Similar to definitions of Let variable.
- Except that it cannot be redeclared and reassigned - constant.

</details>

### Rules When Naming Variables

- It cannot be a `reserved keyword` (let, if, etc.).
- The naming should be `meaningful`.
- It cannot start with a `number` (1name).
- It cannot contain a `space` or `hyphen` (-).
- Use `camel case` notation.

```
let firstName;
```

- It is `case-sensitive`.

```
let FirstName;
```

- To separate multiple variables, use `commas`.

```
let firstName, lastName;
```

- The modern best practice is to declare each variable on a `separate line`.

```
let firstName = "Adrian";
let lastName = "Del Rosario";
```

## Constants

...
