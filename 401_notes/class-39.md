# Class 39

**Resources:**

- [Redux Thunk](https://www.npmjs.com/package/redux-thunk)
- [Async actions in Redux with Thunk or custom middleware](https://blog.logrocket.com/managing-asynchronous-actions-in-redux-1bc7d28a00c6/)



## Review, Research, and Discussion

1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application?
    - The best practice for “pre-loading” data will be to make an async call to load data before component renders. In our component we can use `useEffect()` hook to reneder remote data.
2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer?
    - We have to export action creator from our reducer

## Vocabulary Terms

1. Middleware
    - Middleware is some code you can put between the framework receiving a request, and the framework generating a response. 
    - Redux middleware provides a third-party extension point between dispatching an action, and the moment it reaches the reducer. People use Redux middleware for logging, crash reporting, talking to an asynchronous API, routing, and more.
2. Thunk middleware 
    - Redux Thunk middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. The inner function receives the store methods dispatch and getState as parameters.