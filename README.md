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

cost data = [
  {id: 1, name: 'A'},
  {id: 2, name: 'B'},
  {id: 3, name: 'C'}
];

const server = http.createServer((req, res) => {
  const { headers, url, method } = req;
  console.log(headers, url, method);
  
  res.setHeader('Content-Type', 'application/json');
  res.setHeader('X-Powered-By', 'Node.js');
  res.end(JSON.stringify({
    success: true,
    data: data
  }));
});

const PORT = 5000;

server.listen(PORT, => console.log('Server running on port $(PORT)'));
```


### IMPORTANT HTTP STATUS CODES
* 1.xx Informational
* 2.xx Success
  * 200 Success
  * 201 Created
  * 204 No Content
* 3.xx Redirection
  * 304 Not Modified
* 4.xx Client Error
  * 400 Bad Request
  * 401 Unauthorized
  * 404 Not Found
* 5.xx Server Error
  * 500 Internal Server Error

- *[ALL CODES](https://developer.mozilla.org/en-US/docs/web/http/status)*

### HTTP REQUEST METHODS
| REQUEST METHOD | What is it for?         |
|----------------|-------------------------|
| GET            | Retrieve Resource       |
| POST           | Submit Resource         |
| PUT / PATCH    | Update Resource         |
| DELETE         | Delete/Destroy Resource |

### RESTFUL API STANDARDS
| REQUEST METHOD | Standard                 |
|----------------|--------------------------|
| GET /data      | Get data                 |
| GET /data/1    | Get data with ID of 1    |
| POST /data     | Add data                 |
| PUT /data/1    | Update data with ID of 1 |
| DELETE /data/1 | Delete data with ID of 1 |

- *[ALL METHODS](https://developer.mozilla.org/en-US/docs/web/http/methods)*