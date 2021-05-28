# Class 29

**Resources:**

- [A Complete Guide To props.children In React](https://codeburst.io/a-complete-guide-to-props-children-in-react-c315fab74e7c)
- [Thinking in React: Component Composition](https://dev.to/bouhm/thinking-in-react-component-composition-fp5#:~:text=In%20React%2C%20composition%20is%20a,in%20building%20many%20other%20components.)
- []()
- []()

## Review, Research, and Discussion

1. Do child components have direct access to props/state from the parent?
    - Yes. When we need to pass data from a parent to child class component, you do this by using props.
2. When a component “wraps” another component, how does the child component’s output get rendered?
    - Child component's output will get rendered when paraent component get rendered
3. Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?
    - Yes. We can reuse components anywhere
4. What trick can a parent use to share all props with it’s children
    - we can spread the props attributes to pass it in JSX using the Spread operator `(three dots syntax (...))` which passes the whole props object.

## Vocabulary Terms

1. Props.children
    - It is a special prop, automatically passed to every component, that can be used to render the content included between the opening and closing tags when invoking a component. These kinds of components are identified by the official documentation as “boxes”.
2. Composition
    - It is a natural pattern of the component model. It's how we build components from other components, of varying complexity and specialization through props. Depending on how generalized these components are, they can be used in building many other components.