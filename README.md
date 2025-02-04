# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications: an infinite loop caused by incorrectly updating state within the `useEffect` dependency array. The `useEffect` hook is called with an empty dependency array (`[]`), causing it to run only once after the initial render. However, within the `useEffect` function, the state `count` is updated, triggering a re-render and causing the `useEffect` hook to execute again, leading to an infinite loop.

## Bug Description

The provided `MyComponent` function uses `useState` to track a count. The `useEffect` hook attempts to increment the count on every render, creating a continuous loop.  This results in the browser tab becoming unresponsive and eventually crashing, due to excessive rendering.