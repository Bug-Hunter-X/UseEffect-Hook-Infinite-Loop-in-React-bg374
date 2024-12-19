# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The issue arises when the `useEffect` hook is used without a dependency array, causing it to run after every render, leading to an infinite loop and potentially crashing the application.

## Bug Description
The provided `MyComponent` uses `useEffect` without a dependency array.  This causes the `console.log` statement and any side effects within the `useEffect` to execute on every render, creating a cycle where each render triggers another render, resulting in an infinite loop.

## Solution
The solution involves providing an empty dependency array `[]` to the `useEffect` hook. This ensures the effect only runs once after the initial render. If you need the effect to run based on changes to specific variables, those variables should be listed in the dependency array.