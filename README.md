# Node.js Server Hang Issue

This repository demonstrates a common issue in Node.js where the server hangs when processing long-running requests.  The problem stems from Node.js's single-threaded event loop.  When a request blocks the event loop (as in the example with a long `while` loop), no other requests can be processed.  This leads to a unresponsive server.

The solution involves using asynchronous operations (like promises or async/await) or offloading long tasks to worker threads or a message queue.