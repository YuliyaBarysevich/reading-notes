# Class 27

**Resources:**

- [Testing React — an overview](https://medium.com/dailyjs/testing-react-an-overview-56204839cbad#:~:text=When%20it%20comes%20to%20React,render%20our%20components%20within%20Jest.)
- [Create React App](https://create-react-app.dev/docs/deployment/)
- [Behavior Driven Development Tutorial](https://www.tutorialspoint.com/behavior_driven_development/index.htm)
- [How to understand a component’s lifecycle methods in ReactJS](https://www.freecodecamp.org/news/how-to-understand-a-components-lifecycle-methods-in-reactjs-e1a609840630/#:~:text=Mounting%20is%20the%20phase%20in,and%20inserted%20into%20the%20DOM).&text=This%20method%20is%20called%20just,method%2C%20the%20component%20gets%20mounted.)

## Review, Research, and Discussion

1. Does a deployed React application require a server?
    - We don’t necessarily need a static server in order to run a Create React App project in production. It also works well when integrated into an existing server side app. When it comes to React components we want to check how a component is rendered and if all props we pass to the component influence the behavior of the component as expected.
2. Why do we prefer to test a React application at the behavior rather than the unit level?
    - Unit tests don’t give us that much confidence that our app behaves exactly as we want it too
3. What does npm run build do?
    - creates a `build` directory with a **production build** of an app.
4. Describe the actual composition / architecture of a React application


## Vocabulary Terms

1. BDD
    - Behavior Driven Development (BDD) is a branch of Test Driven Development (TDD). BDD uses human-readable descriptions of software user requirements as the basis for software tests. BDD uses examples to illustrate the behavior of the system that are written in a readable and understandable language for everyone involved in the development.
2. Acceptance Tests
    - Type of testing done by users, customers, or other authorised entities to determine application/software needs and business processes. Acceptance testing is the most important phase of testing as this decides whether the client approves the application/software or not. It may involve functionality, usability, performance, and U.I of the application. 
3. mounting
    -  Mounting is the phase in which React component mounts on the DOM (i.e., is created and inserted into the DOM). This phase comes onto the scene after the initialization phase is completed. In this phase, component renders the first time. 
4. build
    - Builds the app for production to the build folder. It correctly bundles React in production mode and optimizes the build for the best performance.