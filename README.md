# React 19 useEffect Cleanup Missing Return Statement

This repository demonstrates a common error in React 19: forgetting to include a return statement in the cleanup function of a useEffect hook. This can lead to memory leaks if not handled properly.  The bug involves a missing `return` statement within the `useEffect` cleanup function, resulting in the `setInterval` function not being properly cleared when the component unmounts.

## Bug
The `bug.js` file contains a component with a `useEffect` hook that uses `setInterval`.  The `setInterval` function is not cleaned up properly, leading to a potential memory leak. 

## Solution
The `bugSolution.js` file shows the correct implementation, demonstrating how to properly clean up the `setInterval` using the return statement.  The correct cleanup function should return a function that will clear the `setInterval` when the component unmounts. This prevents the unnecessary execution of the `setInterval` after the component is no longer in use.