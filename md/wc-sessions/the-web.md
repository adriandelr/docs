# The Web

_Duration: ~30 mins_

## www - World Wide Web

A network of interconnected documents or information on the internet via hypertext links.

## Web Development

#### Front-End / UI-UX

The graphical interface that you view and interact with in the browser.

#### Back-End / Database

The component that stores the data driving the Front-End.

#### Full-Stack / End-to-End

Both the client-side and server-side.

## Web Architecture

The structure and design of a web system, outlining how its components interact and function together.

Key Points

- Describes the different types of web architectures (Monolithic, Microservices, Serverless, etc.) and their benefits.
- Explores the importance of APIs in connecting various components of a web application.
- Details how a proper web architecture can handle high traffic, complex features, and ensure reliability.
- Touches on best practices for scaling applications and making them adaptable to future growth.

It highlights that choosing the right architecture for the specific needs of an application is key to its success, with a strong focus on adaptability and scalability.

It is a solid foundation on web application architecture, offering insights into modern practices, design models, and best practices for building scalable and efficient web apps.

![web-architecture](images/web-architecture.png)

The architecture covers components like front-end, back-end, databases, APIs, microservices, cloud infrastructure, and containers.

The diagram helps explain the flow of data and interaction between each component.

## Languages

#### HTML (Hyper Text Markup Language Standard)

The building blocks that make up our web pages.

#### CSS (Cascading Style Sheets)

To design and enhance the appearance of web pages.

#### JavaScript

To incorporate features and interactivity into our web pages.

#### TypeScript

A programming language developed by Microsoft to overcome some of the limitations of JavaScript.

## JavaScript libraries and frameworks

Used for building user interfaces, particularly for `single-page applications` (SPAs).

![js-lib-fw](images/js-lib-fw.png)

Building websites usually involves many repetitive tasks, which is where front-end frameworks and libraries come in.

A framework or library provides a lot of reusable code, allowing us to complete tasks more quickly.

That’s why many companies use popular frameworks like **React**, **Angular**, and **Vue**.

You don’t need to learn all of these. Different companies use different tools based on the needs of their projects.

When starting out, focus on `React` since it’s the most popular tool to date.

## Version Control System

We use version control systems to manage project history and collaborate effectively with others.

## Browsing The Web

What happens when you browse the internet?

**URL** stands for `Uniform Resource Location`

A way for finding a resource on the internet.

#### URL Breakdown

The components of a URL include:

1. **Scheme** (http, https, ftp): The protocol used.
2. **Host** (www.example.com): The domain name or IP address.
3. **Port** (:8080): An optional number of a specific port.
4. **Path** (/path/to/resource): The directory or file location on the server.
5. **Query** (?id=123&name=John): Parameters and values to display dynamic content.
6. **Fragment** (#section): A reference to a specific part of the page, indicated by a hash.

#### Web Resources

Refer to any content or data available over the internet that can be accessed or interacted with. These can include:

1. **Web Pages**: HTML documents that contain text, images, and other content.
2. **Images and Videos**: Media files such as .jpg, .png, .mp4, etc.
3. **Files**: Documents like PDFs, Word files, and software downloads.
4. **APIs**: Interfaces that allow different applications to communicate with each other.
5. **Databases**: Structured collections of data that websites or applications query to retrieve information.
6. **Scripts**: JavaScript or other coding resources used to add interactivity or functionality to websites.
7. **Fonts and Stylesheets**: Resources for styling and typography (CSS files, web fonts).
8. **Server Resources**: Servers that store and deliver content or handle requests.

These resources can be accessed using a `URL`, and each serves a specific role in delivering content or functionality on the web.

#### Client and Server

The client (browser) requests a service, and the server responds by providing it.

#### HTTP (Hypertext Transfer Protocol)

A simple text-based language used for communication between the client and server.

#### HTTPS (Secure)

Transferred messages are secured through encryption.

Structured HTTP Protocol

<details>
  <summary>Request</summary>

```
GET /index.html HTTP/2.0
Host: https://adriandelr.github.io/
Accept-Language: en-us
```

</details>

## Request and Response

We send and receive these messages via the protocol.

<details>
  <summary>Response</summary>

```
HTTP/2.0 200 OK
Date: 1 Jan 2022 09:00
Content-Type: text/html

<!DOCTYPE html>
<html>
...
</html>
```

</details>

## Rendering

Once the message exchange is successful, we fetch the file (HTML document).

The browser processes the file and displays the DOM (Document Object Model), which includes references to our resources.
