---
title: "A brief overview of Node.js & Express.js"
seoTitle: "A brief overview of Node.js & Express.js"
datePublished: Thu Sep 21 2023 14:23:23 GMT+0000 (Coordinated Universal Time)
cuid: clmt9ji9m000709mf1k58ckgk
slug: a-brief-overview-of-nodejs-expressjs
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1695301924944/7c79ec05-9efe-488f-820c-9cdfc2c100d0.png
tags: postman, express, http, nodejs, expressjs-cilb5apda0066e053g7td7q24

---

# 1.Node.js & Express, hand in hand?

### What is a runtime environment?

A runtime environment is a **platform that executes software code**, managing system resources like memory and CPU, while **abstracting low-level hardware details**. It ensures code can run efficiently across different systems.

**<mark>Node.js </mark>** <mark>is like the engine in a car. </mark> **<mark>It's the runtime environment</mark>** that executes JavaScript code on a server or computer.

It handles tasks like memory management, file operations, and network communication, **<mark>ensuring JavaScript can run outside web browsers.</mark>**

Node.js was **created by Ryan Dahl** and was **first released in 2009**. It originated from Dahl's desire to **build scalable network applications using JavaScript.**

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695304416006/d0614721-3095-4fe9-abba-ffafb90b84e1.avif align="center")

### What is a framework?

A framework is a s**tructured set of tools and conventions** that simplifies software development by providing a **pre-defined structure** and **ready-made components** for building applications. <mark>Express.js is a</mark> **<mark>framework</mark>** **<mark>on top of Node.js</mark>**<mark>, simplifying server-side web development with JavaScript.</mark>

Express.js is like the **blueprint for building a car on top of the engine** (Node.js).

It provides a **structured set of tools and conventions** for building web applications, simplifying tasks like handling web requests, routing, and middleware management.

Developers use Express.js to build web applications efficiently on the Node.js runtime, just as builders follow a blueprint to construct a car on an engine-powered vehicle.

Express.js was created by T**J Holowaychuk and was first released in 2010.** It was designed to work as a web application framework on top of Node.js, simplifying server-side web development with JavaScript.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695304447558/71e6a5a9-90e6-447c-a738-6706538c877d.avif align="left")

### Node.js and Express.js

**Express simplifies backend development** and is highly regarded among professional developers. <mark>While Node.js provides the runtime environment to run JavaScript on computers, Express is a framework that makes building website backends easier.</mark> **Node.js is versatile, but it's like a basic tool.** Express is a powerful electric screwdriver that makes web development faster and simpler.

**Express code is well-structured, easy to read, and modular, unlike the verbose and complex code required when using Node alone.** Express allows us to add middleware like building with Lego, giving us flexibility.

Among JavaScript backend developers, Express is the go-to choice for creating website backends, as it greatly improves readability and productivity. So, if Node.js is the toolbox, Express.js is the must-have power tool for building web backends.

**Node.js (Regular Screwdriver)**:

* Imagine you're trying to assemble furniture with a regular screwdriver. It gets the job done, but it requires a lot of manual effort and can be quite slow. Just like Node.js, it's versatile and can be used for various tasks, but it might not be the most efficient choice for every situation.
    

[![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695299133670/f6692c4a-4c36-4771-9451-f61509aa516f.png align="center")](https://nodejs.org/api/documentation.html)

**Express.js (Electric Screwdriver)**:

* Now, picture yourself using an electric screwdriver to put together the same furniture. It's much faster and easier, making the task a breeze. Express.js is like the electric screwdriver—it's a specialized tool built on top of Node.js that simplifies and accelerates web development, particularly for creating website backends. It takes the power of Node.js and adds a layer of convenience and efficiency, making the development process smoother and faster. Just as you'd choose an electric screwdriver for assembling furniture quickly, developers often choose Express.js for building web backends efficiently.
    
    [![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695299110595/763b8088-222f-49d5-8077-39c73a8ab860.png align="center")](https://expressjs.com/en/starter/installing.html)
    

# 2.What is NPM?

NPM <mark>(Node Package Manager</mark>) is a **tool used** in the Node.js ecosystem **to manage and distribute JavaScript packages or libraries.** It allows developers to easily install, update, and share code packages with others.

In the car and engine analogy:

* **NPM (Node Package Manager)** can be likened to the **fuel station or gas station** where you go to refuel your car. It's the place where you can **easily access and obtain the necessary resources** (JavaScript packages or libraries) that your **Node.js engine** (server) needs to run efficiently. Just as you visit a gas station to power your car, **<mark>developers use NPM to acquire and manage essential code packages for their Node.js applications</mark>**, keeping them running smoothly.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695304494331/7a151f12-590e-4c5f-9bb3-eb3baa8290ca.avif align="center")

# 3.Creating our Express server.

Creating an Express server involves six key steps:

1. **Directory Setup**: Start by creating a **<mark>dedicated project directory</mark>** to organize your files.
    
2. **Index.js File**: Inside the directory, **<mark>create an "Index.js" JavaScript file</mark>**. This file will be your server's main entry point.
    
3. **Initialize NPM**: Initialize NPM to manage project dependencies and configuration. Use the following command to initialize npm `npm init -y`
    
4. **Install Express**: Use NPM to install the Express package using `node i express`, which simplifies web server development.
    
5. **Write Code**: In "Index.js," write the code that defines your server's behavior, including handling requests.
    

```javascript
// 1  import the express module
import express from "express";
// 2  create a constant for using express module in the followung server code {in this case "app" is the constant}
const app = express();
// server code

// server code

// 3 initialize a port {in this case 3000} for the serve to listen and respond to requests

app.listen(3000, () => {
    // this is the callback function that is going to be triggered when our server is triggered.
  console.log("The server is running on port 3000.");
});
```

1. **Start the Server**: Execute " `node index.js`" in your terminal to start your Express server. It will now listen for and respond to incoming requests.
    

Go to the following URL : - [http://localhost:3000/](http://localhost:3000/) on your computer.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695303035953/3c1ee678-9605-49b1-89a7-0886f6f6a67c.png align="center")

This is the output you must get in your terminal

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1695303145974/ddc1087c-c7b2-4e77-a704-53969bb5133e.png align="center")

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">Use <code>Ctrl + C</code> to stop the server.</div>
</div>

### What is LocalHost 3000?

"[Localhost](http://Localhost)" is like **your computer** playing the role of a **server for your website**, but only within your computer. It's like your **computer becoming the host for your website's back end**, and this is the "local" part of hosting.

<mark>When you type "</mark>[<mark>https://localhost</mark>](https://localhost)<mark>"</mark> into your browser, you're basically <mark>telling your computer to look into itself.</mark> Then, if you <mark>add a colon and specify a port number (like 3000), it's like telling your computer to look for a specific door (port) on itself.</mark>

**Think of ports as doors on your computer.** Each door has an address, and your server can listen behind a particular door, like Port 3000. So, <mark>when you access "</mark>[<mark>localhost:3000</mark>](http://localhost:3000)<mark>," it's like knocking on that specific door of your computer, and your server, </mark> which is waiting behind that door, responds to your request. It can send back things like HTML, CSS, or JavaScript files to display your website.

These doors (ports) help different services, like your printer or remote control for a presentation, access your computer without interfering with each other. You can even check which doors are open on your computer using commands like 'netstat' on Windows or 'lsof' on Mac. This way, you can see which doors (ports) are actively listening for requests from the outside world.

<div data-node-type="callout">
<div data-node-type="callout-emoji">💡</div>
<div data-node-type="callout-text">IP address + Port number = Socket</div>
</div>

So, **when you encounte**r an error message like "`cannot get /`," it means your **server couldn't find the specific thing you requested**.

# 4.HTTP Requests

HTTP request verbs, also known as HTTP methods, are actions or commands used by clients (e.g., web browsers) to communicate with web servers. These verbs specify the desired operation to be performed on a resource identified by a URL. Here are some common HTTP request verbs:

1. **GET**: Used to retrieve data from the server. When you visit a web page in your browser, it typically sends a GET request to the server to **<mark>fetch the page's content.</mark> H**ence the above error "[Cannot GET](https://cdn.hashnode.com/res/hashnode/image/upload/v1695303035953/3c1ee678-9605-49b1-89a7-0886f6f6a67c.png)" means
    
    ```javascript
    app.get("/", (req, res) =>
     {   res.send("hellooooo shahima !!!"); 
    });
    ```
    
2. **POST**: Used to send data to the server to **<mark>create a new resource.</mark>** It is commonly used when submitting forms on websites, where data like user input is sent to the server for processing.
    
3. **PUT**: Used to **<mark>update or replace an existing resource</mark>** on the server. It sends data to completely replace the identified resource or create it if it doesn't exist.
    
4. **PATCH**: Similar to PUT, but used to apply **<mark>partial modifications to an existing resource. </mark>** It's often used when you want to update only specific fields of a resource.
    
5. **DELETE**: Used to **<mark>request the removal of a resource</mark>** on the server.
    

These HTTP request verbs allow clients to interact with web servers in various ways, enabling actions like retrieving data, submitting data, updating resources, and more. Each verb serves a specific purpose and is used in specific contexts when building web applications and APIs.

### What is the difference between **<mark>put</mark>** and **<mark>patch</mark>?**

The main difference between the HTTP methods PUT and PATCH lies in how they handle updates to resources:

**PUT**:

* **Analogous to Replacing**: Think of PUT as similar to completely replacing an object with a new one. When you use PUT to update a resource, you send the entire updated object, and it replaces the existing resource on the server.
    
* **Idempotent**: PUT requests are idempotent, meaning that **<mark>multiple identical PUT requests will have the same result as a single request. </mark>** If you send the same update multiple times, it **<mark>won't change the outcome.</mark>**
    

**PATCH**:

* **Analogous to Modifying**: PATCH is like making specific modifications or changes to an object without replacing it entirely. When you use PATCH, you send only the changes you want to apply to the resource, leaving the rest of the resource intact.
    
* **Not Necessarily Idempotent**: PATCH requests are not inherently idempotent. **<mark>The same PATCH request applied multiple times might yield different results</mark>** if the initial state of the resource changes between requests.
    

**Analogy**: Imagine you have a car, and you want to update its colour:

* Using **PUT** is like taking the car to the shop and completely <mark> replacing it with a new car of the desired colour.</mark> You get a brand-new car, but it's a complete replacement.
    
* Using **PATCH** is like <mark>painting the car in the desired colour</mark> without changing the entire vehicle. You modify a specific part (the colour) while leaving the rest of the car as it is.
    

In summary, PUT replaces the entire resource, while PATCH makes partial modifications to the resource, much like getting a new car vs. painting an existing one.

### HTTP Response Status Code.

HTTP response status codes are three-digit numbers that the server sends to the client's browser to provide information about the outcome of an HTTP request. These status codes convey whether the request was successful, encountered an error, or requires further action. Here are some common HTTP response status codes:

**1xx (Informational):** These are informational responses and are not typically seen in everyday web browsing.

* **100 Continue:** The **<mark>initial part of the request was received,</mark>** <mark> and the </mark> **<mark>client should proceed</mark>** with sending the remainder of the request.
    

**2xx (Successful):** These indicate that the **<mark>request was received, understood, and successfully processed.</mark>**

* 200 OK: The **request was successful,** and the server is sending back the requested data.
    
* 201 Created: The **request has been fulfilled,** and a **new resource has been created.**
    
* 204 No Content: The **request was successful, but there is no content to send back.**
    

**3xx (Redirection):** These codes indicate that further action needs to be taken to complete the request.

* 301 Moved Permanently: The requested resource has been permanently moved to a new URL.
    
* 302 Found (or 303 See Other): The resource is temporarily located at a different URL.
    
* 304 Not Modified: The client's cached version of the resource is still valid.
    

**4xx (Client Error):** These indicate that the client has made an error in the request.

* 400 Bad Request: The server did not understand the request due to invalid syntax or other client-side issues.
    
* 401 Unauthorized: Authentication is required to access the requested resource.
    
* 403 Forbidden: The server understands the request but refuses to fulfil it.
    

**5xx (Server Error):** These indicate that the server failed to fulfil a valid request.

* 500 Internal Server Error: A generic error message indicating a problem on the server.
    
* 502 Bad Gateway: The server, while acting as a gateway or proxy, received an invalid response from the upstream server.
    

These status codes help developers and web servers communicate issues with HTTP requests and responses. They provide valuable information for debugging and understanding the outcome of web requests.

> ***HTTP status code cheat sheet according to Sander Hoogendoorn***
> 
> * **1xx (Informational)**: "Hold on, something's happening or I'm giving you some info."
>     
> * **2xx (Successful)**: "Here you go, success, here's what you wanted."
>     
> * **3xx (Redirection)**: "Go away, I'm redirecting you to this URL."
>     
> * **4xx (Client Error)**: "You screwed up, the request is invalid."
>     
> * **5xx (Server Error)**: "I screwed up, there's a problem on my end."
>