# TypeScript

_Duration: ~2 hrs_

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
int number = 3;
number = "c";
```

#### Dynamically Typed

In **dynamically typed languages** like JavaScript, Python, and Ruby, the type of variables is determined at runtime, and it can change during the execution of the program.

We can declare a variable, set it to a number, and later change it to a string. This variable does not have a fixed or static type. Its type is determined and can change at runtime:

```
int number = 3;
number = "c";
Math.round(number);
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

...
