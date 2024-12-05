# Incorrect Conditional Rendering in useEffect Hook

This repository demonstrates a common error in React's `useEffect` hook: incorrect conditional rendering logic based on state.

## Bug Description

The provided code includes a `useEffect` hook that uses an `if-else if` block to log messages to the console based on the value of the `count` state variable.  The logic is flawed because the condition `count > 0` will always be checked before `count === 0`. This leads to unexpected behavior, as when `count` is `0`, the condition `count > 0` is false but `count === 0` is true and should be the case to execute, but because the first condition is already false the second one will not be evaluated and no message will be logged. The code demonstrates how this can lead to unexpected behavior and how to correct it.

## Solution

The solution involves restructuring the conditional logic to ensure that the correct message is logged for each state value. We simply move the evaluation order by changing the order in the conditional statements.

## How to reproduce

1. Clone the repository.
2. Navigate to the project directory and run `npm install`.
3. Run `npm start` to start the development server.
4. Observe the console output and the component's behavior.