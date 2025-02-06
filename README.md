# React setInterval Memory Leak

This example demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook: forgetting to include a cleanup function to clear the interval when the component unmounts.  This leads to a memory leak and potential performance issues.

The `bug.js` file shows the problematic code, and `bugSolution.js` provides the corrected version.

## How to Reproduce

1. Clone this repository.
2. Navigate to the `bug` directory.
3. Run `npm install` to install dependencies (if needed).
4. Run the app. Observe the count increasing.  Close the tab; the interval will continue running in the background.

## Solution

The corrected code uses `clearInterval` in the cleanup function to prevent the memory leak.