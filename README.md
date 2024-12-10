# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug involving the `useEffect` hook and its dependency array.  The `MyComponent` initially suffers from an infinite render loop due to an incorrect dependency array in the `useEffect` hook.

The `bug.js` file contains the buggy code.  The `bugSolution.js` file provides the corrected code.

## Bug Description

The `useEffect` hook is used to perform side effects after a component renders.  If a component's state changes, the `useEffect` should rerun. However, if the dependency array is missing or incomplete, this will trigger unnecessary renders, leading to performance issues or crashes.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository directory in your terminal.
3. Run `npm install` to install the necessary dependencies.
4. Run `npm start` to start the development server.
5. Observe the console logs - you'll see 'Count updated' being logged many times each click causing a potentially infinite loop.

## Solution

The solution is to include the `count` variable in the dependency array to trigger the effect only when `count` changes. View `bugSolution.js` for the fix.