# Unnecessary Re-renders in useEffect Hook

This example demonstrates a common mistake in React's `useEffect` hook: omitting the dependency array, leading to unnecessary re-renders.

## Bug

The `useEffect` hook in `bug.js` logs the current count to the console on every render, even if the count hasn't changed. This is inefficient and may cause performance problems in larger applications.

## Solution

The solution in `bugSolution.js` adds the `count` variable to the dependency array `[count]`.  This ensures the effect only runs when the `count` value changes.