# TypeScript

_Duration: ~3 hrs_

_Required Applications: NodeJS_

_Required Familiarity: Basic JavaScript_

## Intro

**TypeScript** is a programming language developed by _Microsoft_ to overcome the limitations of JavaScript.

It is built on top of JavaScript, making every JavaScript file a valid TypeScript file.

## Advantages

It enhances JavaScript with powerful features that help developers create more robust and maintainable applications more efficiently.

### Static Typing

This is the most important feature that TypeScript provides.

Programming languages can be categorized into two types:

#### Statically Typed

In **statically typed languages** like C++, C#, and Java, the types of variables are determined at compile time or during coding.

For instance, in statically typed languages, when we declare a variable as an integer, and it can only store integer values. Assigning a string or any other data type to this variable would result in a compile-time error:

```
int count = 3;
count = "c";
```

#### Dynamically Typed

In **dynamically typed languages** like JavaScript, Python, and Ruby, the type of variables is determined at runtime, and it can change during the execution of the program.

We can declare a variable, set it to a number, and later change it to a string. This variable does not have a fixed or static type. Its type is determined and can change at runtime:

```
int count = 3;
count = "c";
Math.round(count);
```

While this offers flexibility, it can also introduce problems. For instance, if we pass this variable to a function expecting a number, the application might misbehave or crash.

The issue here is that we won’t discover these problems until we run the application or perform unit tests. This requires testing every function with various edge cases to catch potential bugs.

> TypeScript aims to address this challenge by providing `static typing`, allowing us to catch errors at compile time, before running the application.

TypeScript is essentially JavaScript with `type checking`. We explicitly declare the type of our variables, similar to statically typed languages.

Then, we pass our code through the TypeScript compiler, which checks for errors and let us know if something is wrong, `allowing us to catch issues at compile time`.

## Drawbacks

### Compilation

There is always a compilation step involved because browsers don’t directly understand TypeScript code.

We need to pass our code through the TypeScript compiler, which transpiles it into JavaScript.

This process of converting TypeScript into JavaScript is called **transpilation**.

### Code Discipline

You need to be more disciplined when writing code in TypeScript.

If you’re a programmer looking for quick results and prefer a more relaxed approach, you might feel that TypeScript is getting in the way.

However, for large projects with multiple developers, sticking to vanilla JavaScript could lead to more time spent on debugging and dealing with issues.

In such cases, TypeScript can save time in the future.

For simpler applications, though, you can certainly go for vanilla JavaScript if you prefer a simpler approach.

## Course Setup

The first thing we need is [Node-LTS](https://nodejs.org/), because we will use the its package manager called npm, to install the _TypeScript compiler_.

### Code Completion

Once installed, open the terminal window and run:

```
npm i -g typescript
```

`i` to install the package, and `-g` to set it globally.

This allows us to access TypeScript from any folder by simply typing the package name.

> If you’re on macOS or Linux and encounter a permission error while running this command, you need to prefix it with `sudo`. It stands for _superuser do_ and grants the necessary permissions to execute the command.

To verify our installation, we type `tsc`, which stands for _TypeScript Compiler_, followed by `-v` to check the installed version:

```
tsc -v
> Version 5.6.3
```

> We are running TypeScript this version. You might install a newer version, but don’t worry, everything we will cover here will still apply to newer TypeScript compilers.

## Your First TypeScript

Create a new folder for our project and name it **training-ts**, then open the folder in VSCode.

Inside the folder, add a new file called **basics.ts**.

Earlier, we covered that TypeScript is built on top of JavaScript, so we can say that TypeScript is a `extension` of JavaScript.

In basics.ts, we can write any JavaScript code, and it will be valid TypeScript code:

```
console.log('Hello TypeScript');
```

Open the terminal with `CTRL + backtick` (`), and by using the TypeScript compiler, we can compile _basics.ts_:

```
tsc basics.ts
```

Go into the same folder, and you can see the result of the compilation. The **basics.js** file is generated after running the compiler.

We have the exact same code because, we haven’t used any TypeScript-specific features.

Let’s write some TypeScript code.

In our file, we declare a variable using the `let` keyword called **age**, and annotate it with _number_. Then, we can initialize it with a value:

```
let count: number = 0;
```

By typing a colon followed by the type, we can `annotate` or specify the type of the variable.

Here is the exciting part: since we declared _count_ as a number, we cannot assign it a string or any other type. If we try to do that, we’ll get an error, like this:

```
count = "hi";
> Error: Type 'string' is not assignable to type 'number'.
```

With TypeScript, we can catch many mistakes at compile time. We do not have to run our application or unit tests to realize we accidentally set a _number_ to a _string_. The TypeScript compiler will let us know right away.

Let’s remove the problematic line and recompile our file. Look at the JavaScript code that the TypeScript compiler generated:

```
basics.js
var count = 5;
```

Instead of the let keyword, we have var, because by default, the TypeScript compiler uses an older version of JavaScript called ES5.

> ECMAScript is a standard or specification, while JavaScript is the implementation of that specification. ES5 is an older specification that has been around for a long time, and its features have been implemented in browsers for over a decade now.

To set up the TypeScript compiler to generate modern JavaScript, you can adjust the configuration to target a newer version of JavaScript.

By default, TypeScript uses `var` instead of `let`, and _type annotations_ are `excluded` in the output. These annotations are only for the TypeScript compiler and do not appear in the final JavaScript code, as JavaScript itself doesn’t include variable types.

## TypeScript Compiler Configuration

Let us create a configuration file for the TypeScript compiler.

Inside our project folder, run:

```
tsc --init

> Created a new tsconfig.json with:

  target: es2016
  module: commonjs
  strict: true
  esModuleInterop: true
  skipLibCheck: true
  forceConsistentCasingInFileNames: true


You can learn more at https://aka.ms/tsconfig
```

This generates a **tsconfig.json** file with the following settings.

Exit the terminal window and open the newly generated configuration file.

In the file, you will find several settings, most of which are commented out by default. We’ll only be using some of these options.

Don not feel intimidated by all these settings. We do not need to learn them all.

If you are curious, you can view a description of each setting to understand its purpose.

We will discuss a few key ones:

**target**: Specifies the version of JavaScript that the TypeScript compiler will generate.

It is set to _es2016_, which is an older standard that has already been implemented in all browsers.

> In the target's blank value field, use `Ctrl + Space` to trigger IntelliSense and view all the valid values available.

We can leave the default and use it as the safest option for all browser applications.

> Depending on where you plan to deploy your application, you can opt for a higher target, which often leads to shorter and more concise code.

**module**: Determines how the TypeScript compiler resolves modules and defines the module system for generating the output JavaScript code.

Common values for the module property include:

- commonjs (for Node.js applications)
- es6 or esnext (for ES modules)
- amd, system, umd (other module formats for different environments)

This setting helps TypeScript determine how to structure the import/export statements in the compiled JavaScript code.

**rootDir**: Specifies the directory that holds our source files.

It is set to `./`, which represents the current folder. By convention, we typically place our source code in a separate folder.

Back in our project panel, let’s create a new folder named **src** and move _basics.ts_ inside, then delete _basics.js_.

Enable and change the value of `rootDir` to `./src`.

**outDir**: A similar setting that specifies the directory where our JavaScript files will be placed.

Enable it and change the value to `./dist`.

When we compile our code using the TypeScript compiler, the generated JavaScript files will be stored in this distributable folder.

**removeComments**: A useful setting to remove all comments from our TypeScript code, making the generated JavaScript code cleaner and shorter.

**noEmitOnError**: By default, when we compile our code, the TypeScript compiler will still generate JavaScript files even if there are errors.

This is likely not what we want, so the best approach is to always enable this setting.

> This ensures that if there are any mistakes in the code, the TypeScript compiler will not generate any JavaScript files.

With this configuration file in place, we can now go back to the terminal and compile our code by simply running `tsc`, which will compile all TypeScript files in the project.

We now have a new folder called **dist** that contains our JavaScript file.

## Debugging In TypeScript

Let see how to debug a TypeScript application in VSCode.

## Emitting Source Map

This is incredibly helpful when things go wrong, allowing us to run our code line by line and observe exactly what happens behind the scenes.

We need to follow a few steps:

First, we navigate to the **tsconfig.json** file.

In the `emit` section, we enable the `sourceMap` feature.

It is a file that indicates how each line of our TypeScript code corresponds to the generated JavaScript code.

Let me show you how to do this:

Back in the terminal, let us recompile our code. In the output folder,

you will notice a new file called `basics.js.map`:

```
{"version":3,"file":"basics.js","sourceRoot":"","sources":["basics.ts"],"names":[],"mappings":";AAAA,mCAAmC;AACnC,IAAI,KAAK,GAAW,CAAC,CAAC"}
```

This is our source map. It contains code that indicates how our TypeScript code maps to the corresponding JavaScript code.

This file isn’t meant for us to interpret directly. It’s designed for debuggers and machines to use for accurate debugging.

## Breakpoint Example

Let’s close this file.

To make debugging more engaging, let’s head over to **basics.ts** and add some logic.

For example, we can write a condition: if count is less than 3, we will add 3 to it:

```
let count: number = 0;
if (count < 3) count += 1;
```

Next, we will click on the left side of the first line to insert a breakpoint (🔴).

When we begin debugging, the execution will pause at this breakpoint, allowing us to step through the code line by line from that point onward.

## Creating Our `launch.json`

Next, we go to the debug panel and click on **"Create and Launch"** to generate the **launch.json** file.

From the dropdown, we select _Node.js_, which creates a new file in our project directory.

This file contains configuration settings that instruct _VSCode_ on how to debug the application:

```
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "type": "node",
      "request": "launch",
      "name": "Launch Program",
      "skipFiles": ["<node_internals>/**"],
      "program": "${workspaceFolder}/temp/src/basics.ts",
      "outFiles": ["${workspaceFolder}/**/*.js"]
    }
  ]
}

```

We are using _Node.js_ to launch the program.

Inside the file, there is a label called `Launch Program`, which tells _VSCode_ which program to run during debugging.

We can see that our `program` starts here. In the source folder, we have **index.ts**.

In the `outFiles`, we have ouroutput files that are generated and stored in our project workspace as files with the `.js` extension.

### Pre Launch Task

First, we need to create a default build task.

Go to `Command Palette` by using `F1`.

Type in `Configure Default Build Task` and select our **tsconfig.json** from our directory:

```
{
  "version": "2.0.0",
  "tasks": [
    {
      "type": "typescript",
      "tsconfig": "tsconfig.json",
      "problemMatcher": ["$tsc"],
      "group": {
        "kind": "build",
        "isDefault": true
      },
      "label": "tsc: build - tsconfig.json"
    }
  ]
}
```

In _launch.json_, under _program_, we need to add one more setting called `preLaunchTask`. We’re going to set it to a string with this value:

```
"program": "${workspaceFolder}/src/basics.ts",
"preLaunchTask": "tsc: build - tsconfig.json",
"outFiles": ["${workspaceFolder}/**/*.js"]
```

With this setting, we are telling _VSCode_ to use the TypeScript compiler to build our application using the **tsconfig.json** configuration file.

This ensures that the TypeScript code is compiled before debugging starts.

## Start Our Debugging

Let’s go back to **basics.ts**.

To start debugging, we can go to the debug panel and click on `Launch Program` or if you prefer to use a shortcut, use `F5`.

This will start the debugging session and pause at the breakpoint we set earlier.

## Debugging Tools

Now that our program has started, the execution has paused right at the breakpoint.

At the top, we have a set of debugging tools for controlling the execution flow of our code. These include:

- **Step Over:** Executes the current line and moves to the next. Shortcut: F10

- **Step Into**: Steps into a function if the current line contains a function call.

- **Step Out**: Steps out of the current function and continues execution from the next line.

- **Restart**: Restarts the debugging session.

- **Stop**: Stops the debugging session.

In the `tooltip`, you’ll see the shortcut for each tool.

For example, the shortcut for stepping over a line is `F10`.

### Variables

On the left side, under the **Variables** section, you can see all the variables detected during this debugging session.

Under `Local`, we have the _count_ variable.

As we execute each line, you will see the value of this variable get updated accordingly.

### Watch

If there is something you do not see in the _Variables_ window, you can go to the **Watch** window and add a watch expression.

For example, we can insert the _count_ variable, which is initially set to _undefined_:

![ts-watch](images/ts-watch.png)

This will allow us to track its value as we step through the code.

Let us step over line by line and see our value gets updated, but since our code terminated, we no longer see the expected value.

Add a _console.log_ at the end of the line to execute an output of our _count_ value:

```
console.log(count);
```

Step over until the last line and see that the value is 1.

This is how debugging works in _VSCode_.

It is incredibly useful when things go wrong, as we can start our program and execute it line by line, inspecting variables and code behavior at each step.

## Fundamentals

Let us dive into the basics of TypeScript and explore its key concepts:

- **any** type
- Arrays
- Tuples
- Enums
- Functions
- Objects

These will serve as the foundation for upcoming concepts.

## Built-In Types

**JavaScript** comes with built-in types such as:

- number
- string
- boolean
- null
- undefined
- object

**TypeScript** expands on this by adding new types such as:

- any
- unknown
- never
- enum
- tuple

Throughout the section, you will see each of these steps in detail.

Let us see how we can work with primitive types in TypeScript.

In our code below, we declare a variable with the type _number_ and set the value:

```
let count: number = 1;
```

We are `annotating or explaining` the type of _count_ using this syntax.

Let’s also declare a variable of type string and assign the value and a boolean:

```
let count: number = 1;
let subject: string = 'TS';
let isDone: boolean = false;
```

In TypeScript, explicit _type annotations_ are not always necessary since the compiler can infer the variable type based on its assigned value.

For example, since we’ve assigned a _number_ to this variable, the TypeScript compiler automatically recognizes it as a number, eliminating the need for explicit annotation.

```
let count = 1;
let subject = 'TypeScript';
let isDone = true;
```

Hover over the variable, and you can see that TypeScript has inferred the same type.

## **any** Type

In TypeScript, there’s a type called **any**, which can represent any value.

If we declare a variable without initializing it, TypeScript assumes it has the any type.

This means we can assign it a number first and later a string, but doing so goes against the core principle of TypeScript, which is type safety.

By using any, we lose the benefits of type checking, which is one of the main advantages of TypeScript.

As a best practice, it’s recommended to avoid using the any type whenever possible.

Let us look at an example. Say we have a function called display that takes a text parameter and logs it to the console:

```
function display(text) {
  console.log(text);
}
```

Notice that we have a compilation error.

The error message says that the parameter document implicitly has an any type.

**Implicitly** means we haven’t explicitly defined the type for this parameter, so the compiler is inferring or guessing the type.

Suppose we’re working on a JavaScript project that we’re converting to TypeScript, and at this point, it’s not feasible to explicitly annotate this parameter with a specific type.

In such cases, we have to use the any type.

Now, we have **two options** to suppress this error:

The option is to explicitly annotate the parameter with _any_, signaling to the compiler that we acknowledge its type as any.

The _second option_ is to modify the **tsconfig.json** file.

Under the Type Checking section, you’ll find that _strict_ is enabled, which turns on several basic type-checking features.

One of these is **noImplicitAny**, removing the comment will enable the feature, causing the compiler to flag implicit any types as errors.

To suppress these errors, you can disable noImplicitAny by setting it to _false_:

```
"noImplicitAny": false
```

Back in _basics.ts_, the error is gone. Use it caution only if you know what you're doing.

Otherwise, disabling type checking defeats the purpose of using TypeScript, as it takes away its key benefits.

Lastly, revert the changes made in the config.

## Arrays

In JavaScript, we can define an **array** like this:

```
let IDs = [1, 2, 3];
```

One key feature of JavaScript arrays is that each element can have a different type.

For example, we can have two integers followed by a string, and this is completely valid JavaScript code. This is because JavaScript arrays are dynamic, allowing elements of different types:

```
let IDs = [1, 2, '3'];
```

If we pass this array to a function expecting a list of integers, the third element (a string) will cause an issue. This is where TypeScript helps—by allowing us to explicitly apply a type annotation to enforce type safety.

If _IDs_ is a number array, TypeScript will immediately show an error at compile time, preventing potential runtime issues:

```
let IDs: numbers[] = [1, 2, '3'];
```

Revert the string to an integer to fix the issue. In this case, we do not even need to apply a type annotation because every element in the array is a number. If we remove the type annotation, the compiler can still infer the type of the variable automatically.

If we start with an empty array, the type of this variable will be _any_:

```
let IDs = [];
```

This is something we should avoid because an any array allows a mix of different types. For example, the first element could be a integer, while the second could be a string or a boolean.

If you want to use an empty array, you should explicitly apply a type annotation, such as a IDs array, to ensure type safety.

### Code Completion

Let me show you another great benefit of using TypeScript, **code completion** or **IntelliSense**.

If we type _IDs.forEach_ and pass an arrow function like _n_ =>, then type _n._ inside the function, we can see all the properties and methods available for number objects:

```
let IDs = [];
IDs.forEach(n -> n.)
```

Since our editor knows the type of n, it provides code completion, making these methods easily accessible.

This is a powerful productivity-boosting feature that we do not get with plain JavaScript.

## Tuples

TypeScript has a special type called a tuple, which is a fixed-length array where each element has a specific type.

**Tuples** are often used when working with pairs of values.

For example, if we want to represent a user with two values, an ID and a name. We declare a variable and annotate it using a special syntax:

```
// 1, Adrian
let person
```

We use square brackets and specify that the first element is a number and the second is a string. Then, we initialize the variable accordingly:

```
let person = [number, string] = [1, 'Adrian'];
```

This ensures that our array always has exactly two elements - nothing more, nothing less.

If we add a third element to the tuple, we get a compilation error stating that [number, string, number] is not assignable to [number, string].

This enforces that the tuple must have exactly two elements with the specified types.

Before, we get code completion, or IntelliSense.

If we access the first element, we see all the methods of number objects:

```
person[0].
```

Similarly, if we access the second element, we see all the properties and methods of string objects:

```
person[1].
```

One thing to note about _tuples_ is that, internally, they are represented as plain JavaScript arrays.

So, when we compile our TypeScript code, it simply results in a regular JavaScript array:

```
"use strict"
let person = [1, 'Adrian];
//# sourceMappingURL=basics.js.map
```

> It is a good practice to keep _tuples_ limited to just two values. Using more than that can make your code harder to read and understand.

For example, if you add a boolean and another number to a tuple, it becomes unclear what these values represent:

```
let person: [number, string, boolean, number] = [1, Adrian, true, 0]
```

This makes the code harder to understand. _Tuples_ are most useful when dealing with two values, like key-value pairs, where their purpose is clear.

## Enums

...
