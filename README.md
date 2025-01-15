# React useEffect setInterval memory leak
This example demonstrates a common mistake in React's `useEffect` hook when using `setInterval`.  Forgetting to include a cleanup function to clear the interval leads to memory leaks and unexpected behavior.  The solution shows how to correctly implement the cleanup function to prevent these issues.

## Bug
The `bug.js` file contains a component that uses `setInterval` within a `useEffect` hook. However, it lacks a cleanup function to stop the interval when the component unmounts.  This causes the interval to continue running even after the component is removed from the DOM, leading to a memory leak.

## Solution
The `bugSolution.js` file corrects this by adding a cleanup function that calls `clearInterval` to stop the interval when the component unmounts. This ensures that the interval is properly cleared, preventing memory leaks and other unexpected behavior.