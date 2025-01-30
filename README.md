# React Native FlatList: Duplicate Keys in keyExtractor

This repository demonstrates a common error in React Native's FlatList component: using a `keyExtractor` function that does not provide unique keys for each item.  This results in unpredictable rendering behavior and performance issues.

## Problem

The `keyExtractor` function in FlatList is crucial for React Native to efficiently update and render the list items. If the `keyExtractor` returns duplicate keys, React Native may reuse existing list items or fail to update them correctly.

## Solution

The solution is to ensure your `keyExtractor` function always returns unique keys for each item in your data array.  This usually involves using a unique identifier present in your data, or generating a unique key using a library such as `uuid`.

## How to Reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app. You will observe incorrect rendering.
4. Examine the solution file (bugSolution.js) to see the corrected implementation.

## License

MIT