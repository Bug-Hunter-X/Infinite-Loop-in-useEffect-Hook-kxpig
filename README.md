# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by a missing dependency in the effect's dependency array.

## Bug Description

The `useEffect` hook in `bug.js` causes an infinite loop because it lacks the `count` variable in its dependency array.  Every render causes the effect to run, updating the count and triggering a re-render, leading to an infinite loop. 

## Solution

The solution (`bugSolution.js`) adds `count` to the dependency array, ensuring the effect only runs when `count` changes. This resolves the infinite loop.