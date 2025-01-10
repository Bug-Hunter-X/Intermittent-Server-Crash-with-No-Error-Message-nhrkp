# Node.js Server Crash Bug

This repository demonstrates a bug in a Node.js server that causes intermittent crashes under heavy load. The server appears to crash without providing any helpful error messages in the console.

## Bug Description

The server handles requests and responds with an empty JSON object.  Under normal load, it functions correctly. However, when subjected to a large number of concurrent requests, it crashes without any apparent reason. This makes debugging exceptionally difficult.

## Solution

The solution involves adding robust error handling to prevent the server from crashing.  This includes a more comprehensive try-catch block and logging of errors for easier debugging.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies (none in this case).
3. Run `node server.js` to start the server.
4. Use a load testing tool (like k6 or Apache Bench) to simulate a high number of concurrent requests to the server.  The server will likely crash after some time.
5. Examine `server-fixed.js` for a robust solution that prevents these crashes.