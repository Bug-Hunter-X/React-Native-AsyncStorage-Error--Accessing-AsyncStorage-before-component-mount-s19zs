# React Native AsyncStorage Bug: Access Before Mount

This repository demonstrates a common bug in React Native applications involving AsyncStorage and how to effectively solve it using the useEffect hook.

## The Problem

When using AsyncStorage, it's essential to ensure that the AsyncStorage methods (like getItem, setItem, etc.) are accessed only after the component has successfully mounted. Accessing these methods before mount can lead to unexpected errors or undefined behavior.

## The Solution

The most reliable way to address this is by leveraging the useEffect hook in React. This hook executes code after the component renders for the first time and ensures AsyncStorage is ready before accessing its methods.

## How to reproduce

1. Clone the repository.
2. Run `npm install` to install dependencies.
3. Run `npx react-native run-android` or `npx react-native run-ios` to start the app.
4. Observe the initial errors and the corrected behavior after applying the solution. 