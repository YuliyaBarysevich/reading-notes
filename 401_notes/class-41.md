# Class 41

**Resources:**

- [What is Redux Toolkit?](https://redux.js.org/redux-toolkit/overview#:~:text=Redux%20Toolkit%20makes%20it%20easier,you%20to%20write%20simpler%20code.)
- [Namespace](https://techterms.com/definition/namespace)

## Review, Research, and Discussion

1. Compare and Contrast Redux Toolkit with Redux “Ducks”
    - **Redux Toolkit** is official, opinionated, batteries-included toolset for efficient Redux development. It is intended to be the standard way to write Redux logic. It includes several utility functions that simplify the most common Redux use cases, including store setup, defining reducers, immutable update logic, and even creating entire "slices" of state at once without writing any action creators or action types by hand. It also includes the most widely used Redux addons, like Redux Thunk for async logic and Reselect for writing selector functions.
    - **Redux Ducks** is a modular pattern that collocates actions, action types and reducers.
2. What is the principle advantage of Redux Toolkit
    - Redux Toolkit makes it easier to write good Redux applications and speeds up development, by baking in recommended best practices, providing good default behaviors, catching mistakes, and allowing to write simpler code.


## Vocabulary Terms

1. Redux toolkit slices
    - A function that accepts an initial state, an object full of reducer functions, and a "slice name", and automatically generates action creators and action types that correspond to the reducers and state
2. Namespace
    - A namespace is a group of related elements that each have a unique name or identifier. There are several different types of namespaces, and each one has a specific syntax used to define the corresponding elements. Each element within a namespace has a "local name" that serves as a unique identifier.
