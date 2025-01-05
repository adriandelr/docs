# DevTools

_Duration: ~20 mins_

## Chrome Developer Tools

Is a powerful suite of tools used by front-end developers for debugging, testing, and optimizing websites and web applications.

Shortcuts for accessing on both Mac and Windows:

- Mac: `Cmd + Option + I`
- Windows: `Ctrl + Shift + I`
- Both: `F12`

You can also access it through the browser menu or by right-clicking anywhere on the page and selecting “Inspect.”

## Docking

By default, it is docked to the bottom of the screen. However, you can dock it to the left, right, or even undock it as a separate window.

![docking](images/docking.png)

Many developers prefer docking it on the left side, with the website displayed on the right side.

## Network

Go to google.com and open the **Network** tab in DevTools, then refresh. These show the HTTP requests sent from your browser to Google.

![devtools-network](images/devtools-network-1.png)

You’ll see multiple requests and the amount of data transferred over the network.

Look at the first item in the list. This represents the first HTTP request sent by our browser to Google.

With this request, the browser requested a ‘document’, and the status of the request is 200, which means ‘OK’.

You can also see the amount of data transferred for this request and the time it took to receive the response.

## Headers

If you click on this request, you’ll see more details. In the **Headers** tab, you can view all the request and response headers.

![devtools-network](images/devtools-network-2.png)

Here are some general headers:

- Request URL
- Request Method (GET)
- Status Code
- Remote address (Numeric representation of google.com)

Below, we have the **Response Headers**. There are many headers here, but you don’t need to worry about all of them.

For example, the _Content-Type_ header indicates the type of the response, which is ‘text/html’. You can also see the Date header, showing the time when the response was sent.

## Preview

In the **Preview** tab, you can see a preview of the HTML document returned from the server, which is the homepage of Google. This HTML document includes references to other resources, such as images, fonts, and more.

All these subsequent requests are sent to download the resources. Right below the first request, you’ll see a request for downloading a PNG or an image file. There is another request for getting a different image, and we also have requests for two different fonts.

## Filter

We can easily filter this list. Click on the **Filter** icon. By default, all requests are shown, but we can filter by request type. For example, selecting “Doc” will show requests for downloading HTML documents, while selecting “Font” will display the requests sent to download fonts.
