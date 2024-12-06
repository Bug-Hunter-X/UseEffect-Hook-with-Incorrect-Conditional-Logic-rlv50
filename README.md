# React useEffect Hook Bug

This repository demonstrates a common but subtle bug in React's `useEffect` hook. The issue arises from incorrect conditional logic within the `useEffect`'s callback function, leading to unexpected behavior, specifically on the initial render.

## Bug Description
The provided `MyComponent` uses `useEffect` to log a message when the `count` state variable is greater than 0. However, the conditional check (`if (count > 0)`) is flawed because it will always be false during the initial render where `count` starts at 0. This results in the message never being logged during the first render, even if the `count` is subsequently incremented. This can cause hidden problems in the application.