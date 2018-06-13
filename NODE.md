# Node

Node.js is a lean, fast, cross-platform JavaScript runtime environment that is useful for both servers and desktop applications

It is a JavaScript runtime environment that achieves low latency and high throughput by taking a “non-blocking” approach to serving requests.

In other words, Node.js wastes no time or resources on waiting for I/O requests to return.

It runs a single-threaded event loop registered with the system to handle connections, and each new connection causes a JavaScript callback function to fire.

The callback function can handle requests with non-blocking I/O calls, and if necessary can spawn threads from a pool to execute blocking or CPU-intensive operations and to load-balance across CPU cores.

Node’s approach to scaling with callback functions requires less memory to handle more connections than most competitive architectures that scale with threads, including Apache HTTP Server, the various Java application servers, IIS and ASP.NET, and Ruby on Rails.

Node.js turns out to be quite useful for desktop applications in addition to servers. Also note that Node applications aren’t limited to pure JavaScript. You can use any language that transpiles to JavaScript, for example TypeScript and CoffeeScript.

Node.js incorporates the Google Chrome V8 JavaScript engine, which supports ECMAScript 2015 (ES6) syntax without any need for an ES6-to-ES5 transpiler such as Babel.


## History

The JavaScript-based Node.js platform was introduced in 2009, by Ryan Dahl, for Linux and MacOS, as a more scalable alternative to the Apache HTTP Server.

## Features of Node.js
Following are some of the important features that make Node.js the first choice of software architects.

Asynchronous and Event Driven − All APIs of Node.js library are asynchronous, that is, non-blocking. It essentially means a Node.js based server never waits for an API to return data. The server moves to the next API after calling it and a notification mechanism of Events of Node.js helps the server to get a response from the previous API call.

Very Fast − Being built on Google Chrome's V8 JavaScript Engine, Node.js library is very fast in code execution.

Single Threaded but Highly Scalable − Node.js uses a single threaded model with event looping. Event mechanism helps the server to respond in a non-blocking way and makes the server highly scalable as opposed to traditional servers which create limited threads to handle requests. Node.js uses a single threaded program and the same program can provide service to a much larger number of requests than traditional servers like Apache HTTP Server.

No Buffering − Node.js applications never buffer any data. These applications simply output the data in chunks.

License − Node.js is released under the MIT license.
