# React setInterval Memory Leak
This example demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook.  Without proper cleanup, this leads to a memory leak and can cause unexpected behavior.

## Problem
The `setInterval` function, when used without cleanup, continues to run even after the component unmounts. This results in memory leaks and potential performance issues. The provided code snippet illustrates this problem. 

## Solution
The solution involves using the return value of `useEffect` to provide a cleanup function. This function clears the interval when the component unmounts or when the dependencies change. The improved code is shown in the `bugSolution.js` file.  