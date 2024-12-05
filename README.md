# Unhandled Exception in Node.js HTTP Server

This repository demonstrates a common error in Node.js: unhandled exceptions in an HTTP server.  The `bug.js` file shows a server without proper exception handling, which can lead to unexpected crashes.  The `bugSolution.js` file provides a corrected version with improved error handling.

## Problem

The original `bug.js` lacks a mechanism to gracefully handle exceptions that might occur during request processing.  If an unexpected error arises within the `requestListener` function, the server will crash without any warning or logging.

## Solution

The `bugSolution.js` demonstrates the proper approach: wrapping the request processing logic in a `try...catch` block.  This ensures that even if an error occurs, the server will continue running, and the error will be logged.

This example underscores the importance of robust error handling in Node.js applications to ensure stability and reliability.