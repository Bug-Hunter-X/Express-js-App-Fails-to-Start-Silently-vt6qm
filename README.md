# Express.js Silent Startup Failure

This repository demonstrates a common yet subtle issue in Express.js applications: a failure to start without providing a clear error message.  The application might appear to start without errors, but it may not be listening on the expected port. This is often caused by a port conflict (another application is already using the specified port) or insufficient privileges.

## Bug

The `bug.js` file contains a simple Express.js application attempting to listen on port 3000. If port 3000 is already in use, the application will fail to start gracefully, providing no obvious indication of the problem.

## Solution

The `bugSolution.js` file demonstrates a more robust approach.  It incorporates error handling to catch port binding failures and provide informative error messages to the developer, aiding in debugging.
