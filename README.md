# Unhandled Async Error in Express.js Route

This repository demonstrates a common error in Node.js applications using Express.js: unhandled errors within asynchronous route handlers.

## The Problem

Asynchronous operations, such as database queries or external API calls, are frequent in web applications.  If an error occurs within an async operation and isn't properly handled, the server might crash unexpectedly.

The `bug.js` file shows a simple Express.js server with a route that simulates an asynchronous operation which may fail.  The error is not caught, leading to a crash.

## The Solution

The `bugSolution.js` file demonstrates how to handle this error using `try...catch` blocks within asynchronous operations or by using the error-first callback style for asynchronous functions.  Proper error handling prevents server crashes and allows for graceful error reporting.