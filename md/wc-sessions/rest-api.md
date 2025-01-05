# REST API

_Duration: ~20 mins_

## REpresentational State Transfer

Is basically a standard for building these HTTP services (RESTful Services).

## Client-Server Architecture

Most applications follow this architecture. The app itself acts as the client or the front-end part. Behind the scenes, it needs to communicate with a server or backend to retrieve or save data.

![clientserver-arch](images/clientserver-arch.png)

This communication occurs using the HTTP protocol, which powers the web. On the server, we expose a set of services accessible via HTTP. The client can then directly interact with these services by sending HTTP requests.

## CRUD Operations

We use the basic principles of the HTTP protocol to enable creating, reading, updating, and deleting data, collectively known as this operations.

## HTTP Methods

Here are the commonly used HTTP methods:

_(Starting with commonly used verb)_

1. **GET**: To get data.
2. **POST**: To create data.
3. **PUT**: To update or create data.
4. **DELETE**: To delete data.
5. **PATCH**: To partially update data.

#### Examples

...

_(And ending with uncommonly used noun)_

6. **HEAD**: To get header data without a body.
7. **OPTIONS**: To get supported communication methods.
8. **TRACE**: To get sensitive data like headers that was sent to the server.
9. **CONNECT**: To set up a secure link to the server or HTTPS.

## REST Convention

...
