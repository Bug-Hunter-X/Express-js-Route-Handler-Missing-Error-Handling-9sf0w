# Express.js Route Handler Missing Error Handling

This repository demonstrates a common error in Express.js route handlers: the lack of proper error handling when dealing with user inputs.

## Bug Description
The `bug.js` file shows a route handler that retrieves a user by their ID.  It attempts to parse the ID from the request parameter as an integer and uses it to find a user in a `users` array.  However, it does not handle cases where the `userId` is not a valid number, resulting in a potential crash or unexpected behavior. 

## Solution
The `bugSolution.js` file provides a corrected version of the route handler.  It includes error handling that checks if `parseInt(userId)` successfully returns a number, and if not, it returns a 400 Bad Request error.  Additionally, it handles the case where no user is found with the given ID by returning a 404 Not Found error.

## How to run
1. Clone the repository: `git clone <repository_url>`
2. Navigate to the repository: `cd express-error-handling`
3. Install dependencies: `npm install`
4. Run the application: `node bug.js` (for the buggy code) or `node bugSolution.js` (for the corrected code)