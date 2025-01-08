# CSS

_Duration: ~30 mins_

_Optional Extension: Prettier_

## Cascading Style Sheets

Is latest version of CSS, offering features like animations, media queries, and advanced layout techniques for more dynamic and responsive web design.

Let’s see how we can improve the look and feel of the page we created in the previous HTML5 session.

## Background

CSS3 was officially introduced in 1996, but its more advanced features and full specification came about in stages, with various modules and properties added over time. It addressed limitations of previous CSS versions, particularly in areas like layout, animation, and multi-platform compatibility. The introduction of features like responsive design via media queries, improved layout models like Flexbox and Grid, and the ability to apply animations without JavaScript revolutionized modern web design.

Since its development, CSS3 has become an essential tool for web designers, providing powerful tools to create engaging, user-friendly, and visually appealing websites.

## Your First CSS

In the head element, after the title, we’ll add a new tag called **"style"**. This is where we’ll write our CSS code:

```
<head>
    <title>Your First HTML</title>
    <style></style>
</head>
```

Inside the style tag, we’ll add several styling rules. First, let’s adjust the size of the image. In the editor, type 'img' to reference the image element and add a pair of curly braces. Inside the braces, we write one or more style declarations. Each declaration contains a property and a value. Here, we can set the **width** property to _100px_, and end the line with a semicolon, so we can write multiple declarations:

```
<style>
    img {
        width: 100px;
    }
</style>
```

Next, the edges of the image are too sharp, so we can round them by setting the **border-radius** to _10px_.

> No need to memorize these properties. It is just to get a sense of how CSS works.

Here’s neat a trick: if you set the border-radius to half of the image’s width, you get a circular image. Set it to _50px_:

```
<style>
    img {
        width: 100px;
        border-radius: 50px;
    }
</style>
```

Now, our elements are stacked vertically, but I’d like the image to be aligned to the left side. To do that, we can set the **float** property to _left_. That looks better, but the image is too close to the text. To add some space between them, we can use the **margin-right** property and set it to _10px_:

```
<head>
img {
    width: 100px;
    border-radius: 50px;
    float: left;
    margin-right: 10px;
}
```

Next, let’s make the text bold. We can do this by setting the font-weight property to bold:

```
p {
    font-weight: bold;
}
```

What if we have another username text element and we only want to apply a style to it? We can add a class attribute to the first text element to categorize it. Add the class **text-username** to the first text element. The rule for the username class, declared with a dot (.), will only apply to the element with that class, regardless of the element type:

```
<!DOCTYPE html>
<html>
  <head>
    <title>Your First HTML</title>
    <style>
      img {
        width: 100px;
        border-radius: 50px;
        float: left;
        margin-right: 10px;
      }
      .text-username {
        font-weight: bold;
      }
    </style>
  </head>
  <body>
    <img src="images/myimage.png" alt="My image description" />
    <p class="text-username">@adriandelr</p>
    <p>I love working with HTML!</p>
  </body>
</html>
```

This is how CSS works, and it is a different syntax from HTML.

## More About CSS3

There are a lot of features, topics and style properties to cover.

To learn more, visit [W3Schools CSS Tutorial](hhttps://www.w3schools.com/css/).
