# Class 37

**Resources:**

- [Understanding How Reducers are Used in Redux](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function,receives%20to%20determine%20this%20change.&text=Redux%20relies%20heavily%20on%20reducer,to%20execute%20the%20next%20state.)
- [Redux - Actions](https://www.tutorialspoint.com/redux/redux_actions.htm#:~:text=Actions%20are%20the%20only%20source,from%20your%20application%20to%20store.&text=const%20ITEMS_REQUEST%20%3D%20'ITEMS_REQUEST'%3B,totally%20up%20to%20the%20developer.)
- [Redux Fundamentals, Part 3: State, Actions, and Reducers](https://redux.js.org/tutorials/fundamentals/part-3-state-actions-reducers)
- [Build time travel debugging in Redux from scratch](https://levelup.gitconnected.com/build-time-travel-debugging-in-redux-from-scratch-665fea8fc6cc)

## Review, Research, and Discussion

1. Why choose Redux instead of the Context API for global state?
    - If we work on a larger, complex endeavor, we choose Redux for global state management.
    - Redux is perfect for large applications where there are high-frequency state updates.

2. What is the purpose of a reducer?
    - A reducer is a function that determines changes to an application’s state. It uses the action it receives to determine this change. 
3. What does an action contain?
    - Actions are plain JavaScript object that must have a type attribute to indicate the type of action performed. Apart from this type attribute, the structure of an action object is totally up to the developer. It is recommended to keep your action object as light as possible and pass only the necessary information.
4. Why do we need to copy the state in a reducer?
    - Based on Redux documentation, reducers are not allowed to modify the existing state. Instead, they must make immutable updates, by copying the existing state and making changes to the copied values.

## Vocabulary Terms

1. Immutable state
    - It's a Redux concept when we are treating values as something that cannot be changed. So every update we make a cope of the state, leaving the old one untouched.
2. Time travel in redux
    - Time travel debugging refers to the ability step forward and backward through the state of you application, empowering the developer understand exactly what is happening at any point in the app’s lifecycle.
3. Action creator
    - An action creator is merely a function that returns an action object.
4. Reducer
    - A reducer is a function that determines changes to an application’s state. It uses the action it receives to determine this change.
5. Dispatch
    - `dispatch` is a function of the Redux store. You call `store.dispatch` to dispatch an action. This is the only way to trigger a state change.