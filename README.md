# React useEffect Hook Missing Cleanup Function

This repository demonstrates a common error in React applications involving the `useEffect` hook: forgetting to include a cleanup function.  This can lead to memory leaks and unexpected side effects.

The `bug.js` file showcases the problematic code.  The `bugSolution.js` file provides the corrected version.

## Bug Description

The `useEffect` hook in `bug.js` is missing a return function. This means that when the component unmounts, any cleanup actions (such as event listeners, timers, or subscriptions) will not be properly removed, potentially causing issues.

## Solution

The `bugSolution.js` file demonstrates the correct implementation.  A return function is added to the `useEffect` hook to handle cleanup.

This return function is responsible for removing any resources, event listeners, etc., preventing memory leaks and unexpected behavior when the component is no longer needed.