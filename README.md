# React Native: Unhandled JS Exception: Cannot read properties of undefined (reading 'name')

This repository demonstrates a common error in React Native applications where an undefined state variable is accessed before it has been initialized. This typically occurs when asynchronous operations, such as API calls, update the state, but the component attempts to render before the state is updated.

## Problem
The provided `bug.js` file showcases a component that fetches data from an API.  The component attempts to render and display this data immediately, even before the API call has completed. Consequently, `data.name` causes an error because `data` is initially `null` before being updated.

## Solution
The `bugSolution.js` file addresses this issue by using optional chaining (?.) and nullish coalescing (??) operators. These operators provide a safe way to handle the case where `data` might be undefined or null.  Conditional rendering is also used to only render the content once `data` is available, providing a more robust solution.

## How to Run
1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npx react-native run-android` (or `npx react-native run-ios`) to run the app on your device or emulator.

## License
MIT