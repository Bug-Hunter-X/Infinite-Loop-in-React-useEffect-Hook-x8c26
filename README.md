# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook.  The bug causes an infinite rendering loop due to a missing dependency.

## Bug Description

The `useEffect` hook is used to perform side effects in functional components.  If a dependency array is not correctly specified, the effect can run more frequently than intended, leading to performance issues or even crashes.

In this example, the effect's callback function logs the current count to the console. Without the `count` variable in the dependency array, the effect runs after every render. The log causes a re-render, triggering the effect again, resulting in an infinite loop.

## Solution

The solution involves properly specifying the dependencies for the `useEffect` hook. The `count` variable needs to be included in the array to ensure the effect only runs when the count changes.

## How to reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Open your browser and observe the infinite loop in the console.
5. Check the solution file to see how the bug can be resolved.