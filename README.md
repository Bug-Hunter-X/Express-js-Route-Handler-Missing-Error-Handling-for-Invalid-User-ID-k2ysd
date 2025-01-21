# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  the lack of proper error handling for invalid input.  Specifically, the `/users/:id` route attempts to parse the `id` parameter as an integer without any validation.  If the `id` is not a number, this will lead to an error.

The `bug.js` file contains the buggy code. The `bugSolution.js` file shows how to fix the issue by adding input validation and robust error handling.

## Bug

The bug lies in the absence of error handling for a non-numeric `userId`.  Attempting to parse a non-numeric string as an integer will throw an error and crash the application.

## Solution

The solution involves adding error handling.  This can be achieved by checking if `userId` is a number before attempting to parse it.  If it's not a number, a proper error response should be sent to the client.  Also, additional checks can be implemented to handle other potential errors, such as database lookup failures.