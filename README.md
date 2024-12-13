# Unresponsive Node.js Server

This repository demonstrates a common issue in Node.js where a long-running synchronous operation in the request handler can make the server unresponsive. The `server.js` file contains the problematic code, while `server-solution.js` provides a corrected version using asynchronous operations.

## Problem

The original `server.js` uses a `while` loop to simulate a task that takes 5 seconds.  During this time, the event loop is blocked, meaning no other requests can be handled.  This leads to an unresponsive server.

## Solution

The `server-solution.js` demonstrates how to solve this by using asynchronous operations. This allows other requests to be processed while the long-running task executes in the background.