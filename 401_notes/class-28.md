# Class 28

**Resources:**

- [How to access child’s state in React?](https://www.geeksforgeeks.org/how-to-access-childs-state-in-react/#:~:text=In%20React%20we%20can%20access,component%20in%20the%20parent%20component.)
- [How to pass props to components in React](https://www.robinwieruch.de/react-pass-props-to-component#what-are-props-in-react)
- [What is “Props” and how to use it in React?](https://itnext.io/what-is-props-and-how-to-use-it-in-react-da307f500da0)
- [What is State and Why Does it Matter?](https://thedaylightstudio.com/)

## Review, Research, and Discussion

1. Can a parent component access the state of a child component?
    - In React we can access the child’s state using Refs. We will assign a Refs for the child component in the parent component, then using Refs we can access the child’s state.
    - Refs are created using React.createRef() and attached to React elements via the ref attribute.
2. What can be passed along in a prop variable?
    - Props allows to send any data you can think of. Props can be anything from integers over objects to arrays. 
3. How can a child component “know” the state of another component?
    - If we pass state as props to the child

## Vocabulary Terms

1. Component props
    - “Props” is a special keyword in React, which stands for properties and is being used for passing data from one component to another. (data with props are being passed in a uni-directional flow / one way from parent to child)
    - Props are arguments passed into React components.
      - React Props are like function arguments in JavaScript and attributes in HTML.
2. Component state
    - The state is an instance of React Component Class can be defined as an object of a set of observable properties that control the behavior of the component. 
    - In other words, the State of a component is an object that holds some information that may change over the lifetime of the component. 
3. Application state
    - Application State (also known as Program State) represents the totality of everything necessary to keep an application running.  When we refer to application state we are normally referring to the state of the program as it exists in the contents of its memory.  