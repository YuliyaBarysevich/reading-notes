# Class 38

**Resources:**

- [Splitting Up Reducer Logic](https://redux.js.org/recipes/structuring-reducers/splitting-reducer-logic)
- [Redux - Store](https://www.tutorialspoint.com/redux/redux_store.htm)
- [Redux FAQ: Actions](https://redux.js.org/faq/actions#should-i-dispatch-multiple-actions-in-a-row-from-one-action-creator)


## Review, Research, and Discussion

1. How granular should your reducers be?
    - For any meaningful application, putting all your update logic into a single reducer function is quickly going to become unmaintainable. _While there's no single rule for how long a function should be, it's generally agreed that functions should be relatively short and ideally only do one specific thing. Because of this, it's good programming practice to take pieces of code that are very long or do many different things, and break them into smaller pieces that are easier to understand._ Since a Redux reducer is just a function, the same concept applies. You can split some of your reducer logic out into another function, and call that new function from the parent function.
2. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched
    - It can be both. There's no specific rule for how you should structure your actions. In general, ask if these actions are related but independent, or should actually be represented as one action.
3. Name a strategy for preventing the above
    - Try to avoid dispatching several times synchronously in a row in the places where you're concerned about performance.
    - Avoiding duplicate naming for actions types

## Vocabulary Terms

1. Store
    - A store is an immutable object tree in Redux. A store is a state container which holds the application’s state. Redux can have only a single store in your application. Whenever a store is created in Redux, you need to specify the reducer.
2. Combined reducers
    - The combineReducers generate a function which returns an object whose values are different reducer functions. You can import all the reducers in index reducer file and combine them together as an object with their respective names.
    - The resulting reducer calls every child reducer, and gathers their results into a single state object.