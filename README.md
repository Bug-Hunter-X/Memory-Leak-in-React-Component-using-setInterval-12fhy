# React setInterval Memory Leak

This repository demonstrates a common error in React: using `setInterval` within a `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## The Bug

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.

## The Solution

The `bugSolution.js` file shows the corrected component. It uses the return value of `useEffect` to clear the interval when the component unmounts, preventing memory leaks.