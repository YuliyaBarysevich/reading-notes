# Class 34

**Resources:**

- [Understanding React Context API](https://hashinteractive.com/blog/understanding-react-context-api/)
- [Using Context API in React (Hooks and Classes)](https://www.taniarascia.com/using-context-api-in-react/)
- [The React Context hell](https://dev.to/alfredosalzillo/the-react-context-hell-7p4)
- [Context / React Docs](https://reactjs.org/docs/context.html#contextconsumer)

## Review, Research, and Discussion

1. Why is the Context API useful?
    - The Context API was created to solve a specific problem in React, sharing state down a component tree. Similar to the solution that Redux and React-Redux libraries solve, this solution prevents prop drilling. Prop drilling is when you have to continuously pass props down through a component tree in order for a component “way down” in the application to use that prop.
2. Can a component outside of a provider get its context?
    - The most common way to access `Context` from a class component is via the `static contextType`.
    - The traditional way to retrieve `Context` values was by wrapping the child component in the `Consumer`.
3. What are some common use cases for using the Context API?
    - Context is designed to share data that can be considered “global” for a tree of React components, such as: **the current authenticated user, theme, or preferred language.** 
4. Describe “Context Hell”
    - React Context hell is the nasty code you get taking advantage of the React `Context API`.

## Vocabulary Terms

1. Global state
    - data that we can access at any level of React App Tree
2. Global context
    - Context provides a way to pass data through the component tree without having to pass props down manually at every level.
3. Provider
    - Provider is the container for all React components. It may be used to define the theme, locale, and other application level settings, and can also be used to provide common properties to a group of components.
4. Consumer
    - A React component that subscribes to context changes. Using this component lets you subscribe to a context within a function component.