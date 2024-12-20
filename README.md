# React Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop caused by improperly using the `useEffect` hook. The bug is in `bug.js`, and a solution is provided in `bugSolution.js`.

## Bug Description

The `MyComponent` function utilizes the `useEffect` hook to update the `count` state.  However, because the update happens within the `useEffect`'s dependency array (which is empty `[]`, causing it to run only once), the component continuously re-renders, leading to an infinite loop and a potential browser crash.  This is a classic example of an improper usage of the `useEffect` hook.

## Solution

The solution in `bugSolution.js` addresses the problem by removing the dependency that is causing infinite loops. The new useEffect will run only once after the component mounts.