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
let count: number = 5;
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

In the file, you’ll find several settings, most of which are commented out by default. We’ll only be using some of these options.

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

...
