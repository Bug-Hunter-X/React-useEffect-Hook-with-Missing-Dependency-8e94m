# React useEffect Hook with Missing Dependency

This repository demonstrates a common error in React applications involving the `useEffect` hook: a missing or incorrect dependency array.  The `useEffect` hook is used to perform side effects in functional components.  If the dependency array is missing or incomplete, the effect may run unexpectedly often, potentially leading to infinite loops or incorrect state updates.

## Bug Description

The `bug.js` file contains a React component that uses the `useEffect` hook to log a message to the console after every render. However, the dependency array is missing, causing the effect to run after every render, including state updates. This can lead to performance issues or unexpected behavior.

## Solution

The `bugSolution.js` file demonstrates the correct usage of `useEffect`.  By including `count` in the dependency array, the effect now runs only when the `count` variable changes, resulting in the expected behavior.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console logs and the behavior of the component.

## Learning Points

* Understand the purpose and functionality of the `useEffect` hook in React.
* Correctly use the dependency array in `useEffect` to control when the effect should run.
* Understand that omitting the dependency array means it will run after every render.