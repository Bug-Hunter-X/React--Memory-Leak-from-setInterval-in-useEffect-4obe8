# React: Memory Leak from setInterval in useEffect

This repository demonstrates a common mistake in React applications: using `setInterval` within `useEffect` without proper cleanup. This leads to memory leaks and unexpected behavior.

## Bug
The `bug.js` file shows a React component that uses `setInterval` to update a count every second. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct way to use `setInterval` within `useEffect`. It uses the return value of `useEffect` to clear the interval when the component unmounts, preventing memory leaks.