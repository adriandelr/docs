# The Web

Duration: 30 mins

## WWW (World Wide Web)

A system of linked documents or information in the internet through hypertext links.

## Web Development

#### Front-End / UI-UX

The visual aspect where you see in the browser and what you interact with.

#### Back-End / Database

The part that stores data that powers the Front-End.

#### Full-Stack / End-to-End

Both Frontend and Backend.

## Web Architecture

TBA

## Languages

#### HTML (Hyper Text Markup Language Standard)

The building blocks of our web pages.

#### CSS (Cascading Style Sheets)

For styling web pages and making them beautiful.

#### JavaScript

To add interactive components to our web pages.

## Browsing the Web

What happens when you browse the internet?

`URL` Uniform Resource Location

A way to locate a resource in the internet.

#### Resources

-   Weg pages (HTML documents)
-   Images
-   Video files
-   Fonts

#### Client and Server

The client(browser) request a service, then the server provides a service.

#### HTTP (Hypertext Transfer Protocol)

A plain text language that the client and server use to communicate.

#### HTTPS (Secure)

Transfered messages are encrypted.

Structured HTTP Protocol

<details>
  <summary>Request</summary>

```
GET /index.html HTTP/2.0
Host: https://delrosarioa.bitbucket.io/
Accept-Language: en-us
```

</details>

## Request and Response

We sent and receive these messages using the protocol.

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

After a successful excahnge of message, we retrieve the file(HTML Document). The browser reads it and renders the DOM(Document Object Model) that contains references to our resources.
