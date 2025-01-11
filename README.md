# React setInterval Memory Leak

This repository demonstrates a common mistake in React applications: using `setInterval` within a `useEffect` hook without proper cleanup. This can lead to memory leaks and unexpected behavior.

## The Bug
The `bug.js` file shows a React component that increments a counter every second using `setInterval`. However, it fails to clear the interval when the component unmounts, resulting in a memory leak.

## The Solution
The `bugSolution.js` file demonstrates the correct way to handle `setInterval` within `useEffect`. By returning a cleanup function from the `useEffect` hook, the interval is cleared when the component unmounts, preventing memory leaks.