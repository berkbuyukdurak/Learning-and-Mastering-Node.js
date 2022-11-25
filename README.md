# Learning and Mastering Node.js

A Repository for Those Who Want to Master Node.js and related Frameworks

## What is Node.js?

* It is a JavaScript runtime. It is not a language it is not a framework. The language is JavaScript.
* Built on the V8 JavaScript engine.
* Written in C++ language.
* Essentially allows you to run JavaScript code on the server.

### Why is it a good choice for server side technology?
* It is extremely fast, highly efficient, and highly scalable.
* It is event driven, non-blocking I/O model.
  * Non-Blocking I/O model
    * Works on a single thread using non-blocking I/O calls.
    * Supports tens of thousands of concurrent connections.
    * Optimizes throughput & scalability in apps with many I/O operations.
    * All of the above makes Node.js apps fast & efficient.
* Same language on the front and back end.


## HTTP Intro - Headers, Body, Status Codes

### What is HTTP?
* Hyper Text Transfer Protocol
* Communication between web servers & clients
* HTTP Requests / Responses
* Includes header & body


### Core Node Module
```
const http = require('http');

const server = http.createServer((req, res) => {
  const { headers, url, method } = req;
  console.log(headers, url, method);
});

const PORT = 5000;

server.listen(PORT, => console.log('Server running on port $(PORT)'));
```
