# React useEffect Hook Infinite Loop

This repository demonstrates a common error in React applications: an infinite loop caused by a missing dependency in the `useEffect` hook.

## The Bug

The `bug.js` file contains a component that uses the `useEffect` hook to log a message to the console whenever the component renders. However, the dependency array for the `useEffect` hook is empty (`[]`), which means that the effect runs on every render. This causes an infinite loop, as each render triggers the effect, which triggers another render, and so on.

## The Solution

The `bugSolution.js` file shows the correct way to fix the bug. By adding `count` to the dependency array, the effect runs only when the value of `count` changes.