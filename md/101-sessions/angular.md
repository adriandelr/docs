# Angular

Framework for client applications using HTML, CSS, JavaScript / TypeScript.

## Advantages

-   MVC Pattern
-   Clean Structure
-   Re-usable Code
-   More Testable

## Architecture

### Front-end

Interactive views, components, and pages.

-   UI/UX
-   HTML, CSS, TypeScript, Angular

### Back-end

An access point hosted on one or more web server to process and store data in databases.

-   API (Application Programming Interface) - Endpoints accessible by HTTP protocol
-   Requests - POST/GET
-   HTTP Request > API/Endpoint > Data
-   Data + APIs
-   Business Logic

## Setup Development Environment

-   [NodeJS](https://nodejs.org/) - Runtime environment for executing JavaScript code without a browser.
-   AngularCLI - `npm i -g @angular/cli`, then `ng --version`
-   Project Creation/Scaffolding - `ng new (project-name)`
-   Run Application - using `ng serve` inside the project folder
-   Open server listening on [localhost:4200](http://localhost:4200/)

## Project Structure

(Root)

-   `node_modules` - 3rd party libraries / dependencies
-   `src` - source folder
    -   `app` - component (styles, view, tests, model)
    -   `assets` - static files
    -   `environments` - configuration setting for prod and dev
    -   `index.html` - contains app-root tag
    -   `main.ts` - initialize main module
    -   `polyfills.ts` - support for outdated browser feature
    -   `styles.css` - global styles
    -   `test.ts` - test environment setup
-   `angular.json` - standard angular configuration
-   `.editorconfig` - store IDE settings
-   `.gitignore` - exclude files from git/tracking
-   `karma.config.js` - test runner
-   `package.json` - standard node package file containing libraries or dependencies
-   `protractor.conf.js` - tool to run E2E tests
-   `tsconfig.json` - TypeScript compilation settings
-   `tslint.json` - static analysis code settings (checks for readability, maintainability and functionality errors)

## Webpack

Module bundler to build and compile automation tool and transpile TS to JS and SASS to CSS.

-   Bundles suites
-   Bundles stylesheets
-   Minifies bundles
    -   runtime
    -   polyfills
    -   styles
    -   vender
    -   main

### Hot Module Replacement or Reloading

Webpack automatically updates the browser after changes in source files.

## Angular Versions History

(2010) AngularJS - JavaScript framework, complex and lacking.

(2016) Angular2 - Built with TypeScript, cleaner and easier.

(2017) Angular 4(2.4) - Set to align version of Angular libraries.

(2018~) Angular - To avoid confusion, drop the version suffix.

(Present) Angular v13 - Latest

## Training Fundamentals

TypeScript and OOP.

### TypeScript

A programming language that has features of JavaScript, but has been improved to contain additional features.

#### Additional Features

-   Strong typing
-   Object oriented features
    -   Classes
    -   Interfaces
    -   Constructor
    -   Access Modifiers
    -   Fields
    -   Properties
    -   Generics
-   Catch errors at compile time instead of runtime
-   Intellisense

TypeScript transpiles to JavaScript that browser can work with.

#### Concepts

-   Declaring Variables
-   Types and Type Annotation
-   Type Assertions
-   Arrow Functions
-   Interfaces and Inline Annotation
-   Properties
-   Modules
