# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The `useEffect` hook, when used incorrectly, can lead to an infinite loop, rendering the application unresponsive.  This example shows the issue and provides a corrected solution.

## Bug

The bug lies in the `MyComponent` function.  The `useEffect` hook attempts to update the `count` state within its own callback, causing a continuous loop of state updates.

## Solution

The solution involves understanding the dependency array in `useEffect`. The dependency array is essential for controlling when the effect runs.  In this case, an empty dependency array `[]` signifies the effect should only run once after the component mounts. However, modifying the state within the effect creates a loop. The solution is to use a different approach to update the state or adjust the dependencies to avoid creating an infinite loop. 