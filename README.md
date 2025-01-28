# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving an infinite loop within a `useEffect` hook.  The bug arises from an incorrect or missing dependency array, leading to the effect running repeatedly and unnecessarily. 

## Bug Description
The `MyComponent` component uses `useState` to manage a count. The `useEffect` hook attempts to log the count to the console. However, because `count` is not included in the dependency array of `useEffect`, the effect runs on every render, creating an infinite loop. This leads to excessive console logging and potentially performance issues.

## Solution
The solution involves correctly specifying the dependency array for the `useEffect` hook. By including `count` in the dependency array, the effect only runs when the value of `count` changes.