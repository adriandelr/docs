# HTML5

_Duration: ~45 mins_

_Required: VSCode / Live Server_

## Hyper Text Markup Language

Is the standard language used to create and structure web pages. It consists a series of elements that tell the browser how to display content.

## Background

HTML5 was developed to address the limitations of previous versions and to better support multimedia, graphics, and responsive design. It was first introduced in 2008 and became a W3C Recommendation in 2014.

It brought significant improvements, such as new semantic elements, multimedia audio/video support, APIs for offline storage, and more dynamic web applications.

## Your First HTML

Create a new folder named **“HTML”** and open it in [_VSCode_](https://code.visualstudio.com/). Since the folder is empty, add a new file called index.html. This typically represents the homepage of a website.

> To close the **Explorer** panel, press `CMD+B` on Mac or `CTRL+B` on Windows.

Next, we need to specify that this is an HTML5 document. Type a left angle bracket (<), and the first suggestion will be doctype, which stands for document type:

![html-declaration-intellisense](images/html-declaration-intellisense.png)

VSCode automatically generates this line of code for us. It tells the browser that this is an HTML5 document. This line is known as the **doctype declaration**:

![html-generated-declaration](images/html-generated-declaration.png)

### Declaration of Previous Version

In previous versions of HTML, the doctype declaration was much longer and more complicated, but HTML5 simplified it, making it shorter and cleaner.

### Case Sensitivity

It is not case-sensitive, so it doesn’t matter if you use uppercase or lowercase letters. But by convention, we use lowercase for everything, except for DOCTYPE, which is usually written in uppercase.

## Defining Basic Structure

We use `HTML Elements` to define the structure of the web page.

The first element we're going to use is the html element. Type 'html', then press tab:

![html-generated-tag](images/html-generated-tag.png)

On the left side, we have the opening tag, and on the right side, we have the closing tag.

> Most HTML elements have both an opening and a closing tag, but there are some exceptions that we will cover below.

Inside the html element, let's add more elements. Press Enter to break the line and make the syntax clearer. We’ll add two elements: head and body.

We use the **head** element to give browser information about this page.

For example, here we can use the **title** element to specify the title of this page that appears in the _tab name of the browser_:

![html-head-title-tags](images/html-head-title-tags.png)

Inside the **body** element, we’ll add the elements that will appear on the page.

Let’s say we want to display an image and some text elements on the page:

Type 'img' and press tab. The img element is different from the other elements we’ve used so far.

> There are two differences: first, it doesn’t have a closing tag. We only have an opening tag because the image element cannot contain any child elements.

Here we have two attributes, 'src' and 'alt'. With these attributes, we can supply additional information about an element:

![html-body-img-tag](images/html-body-img-tag.png)

Create a new folder called **"images"** and add any image you’d like to display on the page.

![html-body-img-alt-tags](images/html-body-img-alt-tags.png)

In the **src** attribute’s value presented by double quotes, we can add the relative path to our image.

The **alt** attribute, or alternative text, is used to provide text that will be displayed if the image cannot be loaded.

> You can provide a brief description of the image in the attribute's value, which also helps with accessibility for users with visual impairments.

To add a text element, we use the p tag. Inside the tag, you can add the text you want to display:

![html-body-p-tag](images/html-body-p-tag.png)

## Running Our Page With Live Server

By using the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension, we can host our index.html page directly from its directory and view it in the browser in real-time as we make changes.

With the document open, go to the **Status Bar** at the bottom of the IDE and click on the **“Go Live”** button to run the Live Server and view your HTML page in the browser.

> After running server, you’ll notice the web address is in numeric: **127.0.0.1:5500**. This represents the **local computer address**, and the number after the colon is the **port** where the web server is waiting or listening. After that, we have **/index.html**, a forward slash followed by the name of our file.

## More About HTML5

There are a lot of features, topics and tags to cover.

To learn more, visit [W3Schools HTML Tutorial](https://www.w3schools.com/Html/).
