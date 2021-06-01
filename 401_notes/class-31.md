# Class 31

**Resources:**

- [A Complete Guide To props.children In React](https://codeburst.io/a-complete-guide-to-props-children-in-react-c315fab74e7c)
- [Thinking in React: Component Composition](https://dev.to/bouhm/thinking-in-react-component-composition-fp5#:~:text=In%20React%2C%20composition%20is%20a,in%20building%20many%20other%20components.)
- [How to use props.children in React](https://javascript.plainenglish.io/how-to-use-props-children-in-react-7d6ab5836c9d#:~:text=What%20are%20children%3F,tags%20while%20invoking%20the%20component.)
- [Understanding The Fundamentals of Routing in React](https://medium.com/the-andela-way/understanding-the-fundamentals-of-routing-in-react-b29f806b157e)

## Review, Research, and Discussion

1. Why do we not need more .html pages in a multi-page React app?
    - With React we can build a single-page app, Because we don't need to render different html pages, we can render different components. 
2. If we wanted a component to show up on every page, where would we put it and why?
    - Inside the <BrowserRouter />, outside a <Route />
    - BrowserRouter is used for doing client side routing with URL segments. We can load a top level component for each route. This helps separate concerns in app and makes the logic/data flow more clear.
3. What does props.children contain?
    - Essentially, `props.children` is a special prop, automatically passed to every component, that can be used to render the content included between the opening and closing tags when invoking a component. 

## Vocabulary Terms

1. Composition
    - In React, composition is a natural pattern of the component model. It's how we build components from other components, of varying complexity and specialization through props. Depending on how generalized these components are, they can be used in building many other components.
2. Children / Child Components
    - The children, in React, refer to the generic box whose contents are unknown until they’re passed from the parent component.
    - It simply means that the component will display whatever is included in between the opening and closing tags while invoking the component. The component would usually be invoked from App component.
3. Hash Routing
    - HashRouter is used for static websites with a server that only responds to requests for files that it knows about.
4. Link Routing
    - The react-router package also contains a <Link/> component that is used to navigate the different parts of an application by way of hyperlinks. It is similar to HTML’s anchor element but the main difference is that using the Link component does not reload the page but rather, changes the UI.
