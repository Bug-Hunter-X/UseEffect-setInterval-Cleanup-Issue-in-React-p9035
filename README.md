# React useEffect setInterval Cleanup Issue

This repository demonstrates a common error in React applications: using `setInterval` within the `useEffect` hook without proper cleanup.  This leads to memory leaks and unexpected behavior.

The `bug.js` file shows the problematic code.  The `bugSolution.js` file provides the corrected version.

**Problem:**  The `setInterval` function continues to run even after the component unmounts, resulting in memory leaks and potential performance issues.

**Solution:**  The `useEffect` hook's return value is used to define a cleanup function. This function is executed before the component unmounts, allowing us to clear the interval and prevent memory leaks.