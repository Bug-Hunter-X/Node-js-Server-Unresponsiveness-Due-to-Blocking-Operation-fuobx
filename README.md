# Node.js Server Unresponsiveness

This repository demonstrates a common issue in Node.js applications where a long-running synchronous operation in the request handler can cause the server to hang or become unresponsive.  The `bug.js` file contains the problematic code, while `bugSolution.js` provides a solution using asynchronous operations.

## Problem

The `bug.js` file uses a `while` loop to simulate a long-running task that blocks the event loop, preventing the server from responding to other requests.  This is a classic example of a blocking operation that makes Node.js single-threaded nature problematic.

## Solution

The `bugSolution.js` file demonstrates how to avoid blocking by using asynchronous techniques. Node.js's asynchronous programming model (using events, promises, or async/await) is ideal to prevent the blocking of the event loop.