# Unhandled Promise Rejection in Node.js HTTP Server

This repository demonstrates a common error in Node.js: unhandled promise rejections in HTTP servers.  The example shows a server that performs an asynchronous operation.  If the operation fails, the promise rejection is not handled, leading to potential crashes or silent failures.

## Bug

The `bug.js` file contains a Node.js HTTP server that uses a promise for an asynchronous operation. If this operation rejects (fails), the rejection is not caught, causing a warning (or crash in stricter environments). 

## Solution

The `bugSolution.js` file demonstrates the correct way to handle promise rejections in an asynchronous operation within a Node.js HTTP Server.  It utilizes a `.catch` block to gracefully handle the error and respond appropriately.

## How to reproduce the bug

1. Clone the repository.
2. Run `node bug.js`.
3. The server will run. Refresh the page in the browser a few times until the async operation fails. 
4. Observe the warning or crash. 

## How to fix the bug

1. Review the `bugSolution.js` file for the correct implementation. 
2. Implement the same error handling mechanism in your own code to prevent unhandled promise rejections.