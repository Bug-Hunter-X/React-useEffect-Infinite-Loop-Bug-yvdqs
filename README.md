# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by an incorrectly specified dependency array.

## The Bug
The `bug.js` file contains a `MyComponent` that uses `useEffect` to log the current count.  However, the initial implementation omits `count` from the dependency array. This causes the effect to run after every render, triggering another re-render, leading to an infinite loop and potential crashes.

## The Solution
The `bugSolution.js` file provides a corrected version. By including `count` in the dependency array, the effect only runs when `count` changes, resolving the infinite loop issue.

## How to Reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npm start`.
4. Observe the infinite loop in the console and browser behaviour of the original buggy code.