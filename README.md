# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the dependency array.

## Description

The `bug.js` file contains a component that increments a counter using `useState`.  The `useEffect` hook logs the count to the console. However, because `count` is not included in the `useEffect`'s dependency array, the effect runs after every render, causing an infinite loop.  This is because the effect is re-run every time the component renders, which triggers another render, leading to an endless cycle.