# React useEffect Dependency Array Bug

This repository demonstrates a common bug in React's `useEffect` hook related to its dependency array.  The issue arises when the effect's logic conditionally depends on a state variable's value, but the dependency array doesn't include all possible relevant values.

Specifically, the provided `MyComponent` example only updates the document title when the `count` state variable is greater than 0. This leads to the title remaining unchanged when the count is 0, even though the component re-renders.  The correct solution involves always setting the title, regardless of whether `count` is above 0.

## Solution

The provided `bugSolution.js` file demonstrates the fix which updates the title regardless of the `count` value. This ensures proper synchronization between the component's state and the document title.