# Class 32

**Resources:**

- [Functional vs Class-Components in React](https://djoech.medium.com/functional-vs-class-components-in-react-231e3fbd7108#:~:text=Functional%20component%20are%20much%20easier,you%20to%20use%20best%20practices.)
- [useState in React: A complete guide](https://blog.logrocket.com/a-guide-to-usestate-in-react-ecb9952e406c/)
- [The Guide to Learning React Hooks / Examples & Tutorials](https://www.telerik.com/kendo-react-ui/react-hooks-guide/)
- [The last guide to the useEffect Hook you’ll ever need](https://blog.logrocket.com/guide-to-react-useeffect-hook/)
- [How to useReducer in React](https://www.robinwieruch.de/react-usereducer-hook)

## Review, Research, and Discussion

1. What does a component’s lifecycle refer to?
    - Every React Component has a lifecycle of its own, lifecycle of a component can be defined as the series of methods that are invoked in different stages of the component’s existence.
    - A React Component can go through four stages of its life as follows. 
      - **Initialization:** This is the stage where the component is constructed with the given Props and default state. This is done in the constructor of a Component Class.
      - **Mounting:** Mounting is the stage of rendering the JSX returned by the render method itself.
      - **Updating:** Updating is the stage when the state of a component is updated and the application is repainted.
      - **Unmounting:** As the name suggests Unmounting is the final step of the component lifecycle where the component is removed from the page.
2. Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect
    - To prevent infinite loop. The useEffect hook in React by default runs on every re-render, so we need to use useCallback to ensure that the function in not recreated on every render.
3. Why are functional components preferred over class components?
    - Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks
    - Less code
    - They help to use best practices. It will get easier to separate container and presentational components because you need to think more about your component’s state if you don’t have access to setState() in your component
4. What is wrong with the following code?
    - I guess we don't need to use `useEffect` hook insisde `for loop`

```javascript 
    import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
``` 

## Vocabulary Terms

1. State hook
    - It is a Hook that allows to have state variables in functional components. Passing the initial state to this function and it returns a variable with the current state value (not necessarily the initial state) and another function to update this value.
2. Effect hook
    - With `useEffect`, we can invoke side effects from within functional components
    - **Side effects:** Fetching data, Reading from local storage, Registering and deregistering event listeners
3. Reducer hook
    - It allows functional components in React access to reducer functions from state management.
    - The `useReducer` hook is used for complex state and state transitions. It takes a reducer function and an initial state as input and returns the current state and a dispatch function as output with array destructuring.