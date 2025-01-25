# React Native useEffect Async Cleanup Issue

This repository demonstrates a common issue in React Native applications involving the `useEffect` hook and asynchronous operations.  The problem arises when the asynchronous operation within `useEffect` isn't properly handled during component unmounting, potentially resulting in unexpected state updates or crashes.

## Problem

The provided `bug.js` file shows an example of an asynchronous operation within `useEffect` that lacks a proper cleanup mechanism.  If the component unmounts before the asynchronous operation completes, the subsequent state update may still execute, leading to errors.

## Solution

The `bugSolution.js` file presents a corrected version of the code that addresses the issue. The cleanup function now ensures that any ongoing asynchronous operations are cancelled upon unmounting, preventing unexpected behavior.

## How to reproduce

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install` to install dependencies.
4. Run the app using your preferred React Native method.
5. Observe the behavior with both `bug.js` and `bugSolution.js` to understand the difference.