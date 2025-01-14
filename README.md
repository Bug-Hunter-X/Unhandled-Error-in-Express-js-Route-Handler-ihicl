# Unhandled Error in Express.js Route Handler

This repository demonstrates a common error in Express.js route handlers:  failure to handle invalid input and missing users.

The `bug.js` file shows the problematic code. The `bugSolution.js` file provides a corrected version.

## Problem

The original code attempts to find a user by ID. However, it lacks proper error handling:

1. **Type Error:** If the `userId` from the URL parameter isn't a valid number, `parseInt(userId)` will return `NaN`, leading to a potential error when comparing it to user IDs (which should be numbers).
2. **404 Not Found:**  The route should explicitly handle the case where no user with the given ID is found.