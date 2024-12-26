# Basics

10 sets of questions per topic listed.

## HTML

**1. Define HTML.**

`Hyper Text Markup Language Standard` markup language for creating Web pages that describes the structure of a Web page. It consists of a series of elements that tell the browser how to display the content.

**2. What is the basic structure of an HTML template?**

By the use of HTML tag names, these are `html`, `head`, `title`, `body` tags.

**3. What are semantic and non-semantic elements in HTML?**

Semantic elements clearly defines its content (`html/head/body/header/table/section/article/p/a`), while Non-Semantic elements tells nothing about its content (`div/span/b/i`).

<details>
  <summary>Examples</summary>

##### Semantic Elements

-   Common elements
    -   `<html>`
    -   `<head>`
    -   `<body>`
    -   `<ul>, <ol>, <li>` - ordered and unordered lists
    -   `<p>` - paragraph
    -   `<a>` - anchor
    -   `<table>` - table
    -   `<form>` - forms
    -   `<img>` - images
    -   `<h1>, <h2>, <h3>, <h4>, <h5>, <h6>` - headings
-   Sectioning elements
    -   `<article>` - self-contained blocks
    -   `<aside>` - sidebars
    -   `<nav>` - navigation blocks
    -   `<section>` - content blocks
-   Semantic flow elements
    -   `<main>` - main content, used once per page
    -   `<header>` - header section
    -   `<footer>` - footer section
    -   `<audio>` - audio embeds
    -   `<video>` - video embeds
    -   `<figure>` - block-level image

##### Non-Semantic Elements

-   `<div>` - division
-   `<span>` - inline container
-   `<b>` - bold text without importance
-   `<i>` - italic text

</details>

**4. What are attributes in HTML tag?**

A tag that contains a field inside an element tag.

<details>
  <summary>Examples</summary>

```html
<div class="myClass">
	<input type="text" />
</div>
```

</details>

**5. Name some new features in HTML5?**

-   DOCTYPE declaration: `<!DOCTYPE html>`
-   Semantic Elements: `section, header, nav, footer, article, main, figure, figcaption and progress`
-   Intro of audio and video
-   Vector Graphics
-   Placeholder and Email attribute
-   Storage - application cache, web SQL db, and web storage

**6. What are list elements in HTML?**

-   Ordered List(`<ol>`) - Lists items in order by numbered or alphabetical.
-   Unordered List(`<ul>`) - Lists items in an unordered way by bullet or other format.
-   Definition List(`<dl>`) - Lists items in arranged form or dictionary.

**7. What are selector attributes and their symbols?**

-   id(`#`) - specifies a unique id for an element.
-   class(`.`) - specific a class name for an element.

Both used in style sheet and js to manipulate an element.

**8. What are the differences of `<div>` and `<span>` tags?**

`<div>`(display as block) defines a division while `<span>`(contains no styles) is an inline container to mark up texts

**9. What is HTML/Web Accessibility?**

Ability to give context to screen readers or people with disability using Semantic elements.

**10. What can you do to improve web performance?**

-   Optimize resources by adding them locally as part of the project. Avoid adding dependencies from external soruces.
    -   Unnecessary images
    -   Unnecessary JavaScript
    -   Excessive CSS
    -   Unnecessary plugins
-   SEO (Search Engine Optimization) with clear and clean HTML document can help web crawlers track the right information.
-   Minify HTML, CSS, JavaScript files using Minification techniques. It is ideal to write comments, but the browser ignores it.
-   Enable prefetching of necessary resources before they are rendered.
-   CDN, compression and caching will improve speed of the content nearest to the user.
-   Optimize your images to with proper compression settings and size.
-   Use of minimal frameworks, plugins and settings for CSS and JS.

## CSS

**1. Define CSS.**

`Cascading Style Sheets` describes how HTML elements will look like when display on screen or controls the styles and layout.

**2. What are the ways of adding CSS to an HTML document?**

External - use of `<link>` tag to reference the style sheet.

Internal - use of `<style>` tag to add CSS properties.

Inline - use of `style` attribute to add CSS properties.

**3. What is the difference between margin and padding?**

Margin is the spacing outside of a container, while padding is the space inside.

**4. What are the common symbols used in CSS?**

-   Id and Class Selectors - `# .`
-   Curly Brackets - `{ }`
-   Colon and Semi-Colon - `: ;`
-   Parenthesis and Slashes - `( ) /`

**5. Can you name some of the modules used in CSS version 3?**

##### Modules

-   Selectors
-   Box Model
-   Backgrounds and Borders
-   Text Effects
-   2D/3D Transformations
-   Animations
-   Multiple Column Layout
-   User Interface

**6. What is the difference between Block & Inline element?**

Block Elements have line breaks and sets the element to full width of the container. (`<div>`)

Inline Elements does not have line breaks and does not have an element to set its width or height. (`<span>, <strong>, <img> and <a>`)

**7. What is CSS specificity?**

Specifies the level or rank on which style declaration will be used to an element.

##### Level of Selector

-   Inline style
-   IDs
-   Classes, Attributes and pseudo-classes
-   Elements and pseudo-elemets

Example: When both ID and Class is set to an element, the styles declared in ID will take effect.

**8. What is `pointer-events` property? How safe is it?**

Controls whether the element should react to mouse events. It is safe for elements without children as this property affects them.

**9. What are the units used in CSS?**

##### Absolute Units

-   `px` - absolute unit/resolution per pixel

##### Relative Units

-   `em` - Relative to the parent element
-   `rem`: Relative to the root element (HTML tag)
-   `%` - Relative to the parent element
-   `vw` - Relative to the viewport’s width
-   `vh` - Relative to the viewport’s height

**10. What is MobileFirst and MediaQueries? Example of Mobile Framework(Bootstrap)?**

In responsive web, it means designing for mobile before designing for desktop or larger screen.

MediaQueries are used to create breakpoints in screen sizes using `@media` rule that includes properties and conditions.

Bootstrap is a framework for developing responsive, mobile-first websites. Some of its features:

-   Grid System
-   Flex
-   Display Properties
-   Position

## JavaScript

**1. Define Javascript.**

One of the world's most popular scripting language that is used to create dynamic web pages and controls the actions of elements.

**2. What is Internal and External JavaScript?**

Internal - code is placed in the head and body section.

External - code is stored in a separate external file. Referenced by a `.js` extension.

**3. What are the advantages of using External JavaScript?**

-   Separation of Code
-   Code Maintainability
-   Better Performance

**4. What are Var, Let and Const variables?**

Var

-   Used in the earlier versions
-   Non-blocking, available anywhere within the document or function

Let

-   Used in 2015, ES6
-   Block Scope, has scope only within the block where it is declared

Const

-   Similar to definitions of Let variable
-   Except that it cannot be redeclared and reassigned - constant

**5. What are Objects in JavaScript?**

-   Built-in data type for storing unordered key-value pairs
-   Hold items of any data type
-   Uses Curly brackets to declare or assign key and value `{ key: 'value'}`,
-   Dot notation `.` to access object properties

**6. What are Arrays in JavaScript?**

-   List of ordered stored data
-   Hold items of any data type
-   Uses Square Brackets `['1','2','3']` with individual data separated by commas
-   Has native `push` and `pop` methods

**7. How can we select an element using JavaScript?**

By using

-   `document.querySelector(".element/#element");`
-   `document.getElementById("element")`
-   `document.getElementsByClassName("element")`

querySelector()

-   Only returns the first element

querySelectorAll()

-   Returns all the matches

**8. What are `window`, `document` and `screen` context in JavaScript?**

Window - is the main JavaScript object. It is the root itself or the DOM (Document Object Model) in a browser.

Document - an object inside of `window` that contains DOM elements.

Screen - an object inside of `window` that contains information about the display or screen dimensions.

**9. What is the Spread Operator?**

-   It is similar to `concat` that joins two or more strings
-   Combine or Copy values inside array or objects in another array or object
-   Uses an ellipses(`...`) before an object name

<details>
  <summary>Examples</summary>

```js
{...objectOne, ...objectTwo}

[one, two, ...array]
```

</details>

**10. What is a ServiceWorker?**

Is a little program that runs in the background alongside your regular app code, it takes care of things such as mock datas and handlers, push notifications and response caching.
