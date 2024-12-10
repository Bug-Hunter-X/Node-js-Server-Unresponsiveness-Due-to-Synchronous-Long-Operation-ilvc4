# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in a request handler causes the server to hang or become unresponsive.  The solution shows how to address this using asynchronous operations or worker threads.

## Bug

The `server.js` file contains a simple HTTP server.  The request handler includes a loop that simulates a long-running task.  This blocks the event loop, preventing other requests from being processed.

## Solution

The `server-async.js` file demonstrates using asynchronous operations or worker threads to prevent blocking.  Asynchronous operations allow the event loop to continue processing requests while long tasks are running.