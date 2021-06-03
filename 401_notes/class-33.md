# Class 33

**Resources:**

- [The ultimate guide to the React useReducer Hook](https://blog.logrocket.com/guide-to-react-usereducer-hook/)
- [Building Your Own Hooks](https://reactjs.org/docs/hooks-custom.html)
- [10 React Hooks you Should Have in Your Toolbox](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d)
- [Understanding How Reducers are Used](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/)

## Review, Research, and Discussion

1. Describe use cases for useMemo() and useReducer()
    - `useMemo()` is used to memoize values. `useMemo()` can help the performance of an application by “remembering” expensive functions and preventing a re-render every time there is a change in the application.
    - `useReducer()` helps to manage complex state logic in React applications. `useReducer()` is used to store and update states, just like the useState() Hook. It accepts a reducer function as its first parameter and the initial state as the second. `useReducer()` returns an array that holds the current state value and a `dispatch` function, to which you can pass an action and later invoke. 
2. Why do custom hooks need the use prefix?
    - This convention is very important. Without it, we wouldn’t be able to automatically check for violations of rules of Hooks because we couldn’t tell if a certain function contains calls to Hooks inside of it.
3. What do custom hooks usually do?
    - Building your own Hooks lets you extract component logic into reusable functions.
    - Custom hooks allow us to have cleaner functional components, remove logic from the UI layer, and prevent code duplication by bringing common use cases to reusable hooks.
4. Using any list of custom hooks, research and name one that you think will be useful in your applications
    - `useFetch` from `react-fetch-hook`
5. Describe how a hook that fetches API data might work
    - We can use `useEffect()` hook with axios or superagent to fetch data from API

## Vocabulary Terms

1. Reducer
    - A reducer is a function that determines changes to an application’s state. It uses the action it receives to determine this change.
