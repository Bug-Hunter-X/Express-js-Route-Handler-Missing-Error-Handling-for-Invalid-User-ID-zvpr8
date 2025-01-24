# Express.js Route Handler Missing Error Handling for Invalid User ID

This repository demonstrates a common error in Express.js route handlers:  the lack of error handling for invalid input. Specifically, the code attempts to parse a user ID as an integer without checking for non-numeric values.

## Bug

The `bug.js` file contains a route handler that fetches a user by ID. If the ID is not a valid integer, the `parseInt` function will return `NaN`, leading to the `users.find` method failing to find the user, even if a user with that ID exists.  There is no error handling for this case.

## Solution

The `bugSolution.js` file shows the corrected code.  It includes checks to ensure the `userId` is a number before attempting to parse it and uses error handling to catch instances where the user is not found or the ID is invalid. 