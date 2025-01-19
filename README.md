# Unhandled Promise Rejection in Express.js Application

This repository demonstrates a common error in Express.js applications where asynchronous operations are not properly handled, leading to crashes and unhelpful error messages. The `bug.js` file showcases the problematic code, while `bugSolution.js` provides a corrected version.

## Problem:

The original code uses promises but lacks robust error handling.  If the asynchronous `someAsyncOperation` function rejects (simulating a database error, network failure, etc.), the error is not caught, causing the server to crash silently with a generic 500 error. This makes debugging difficult.

## Solution:

The solution implements a comprehensive error-handling middleware to catch these unhandled promise rejections and send a more informative error response to the client, ensuring better user experience and easier debugging.