## Q1: What is React.js and why do we use it?

<small>React.js is a JavaScript library for building user interfaces, particularly single-page applications (SPAs). Developed by Facebook in 2011, it was first deployed on Facebook's News Feed and later open-sourced in 2013. React enables developers to create large web applications that can update and render efficiently in response to data changes. It emphasizes a component-based architecture, allowing for reusable UI components, and utilizes a virtual DOM to enhance performance by minimizing direct manipulations of the actual DOM.</small>

## Q2: What are the key features of React.js?

<small>React.js offers several key features that make it a popular choice for building dynamic user interfaces:

- **Declarative Syntax:** React follows a declarative programming paradigm, enabling developers to design views for each state in the application, and React efficiently updates and renders components as data changes. This approach enhances code readability and maintenance. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **Component-Based Architecture:** Applications in React are built using encapsulated components that manage their own state. This modularity promotes code reuse and simplifies both development and maintenance. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **Virtual DOM:** React utilizes a virtual DOM, an in-memory representation of the real DOM. When the state of an object changes, the virtual DOM updates only that specific object in the real DOM, leading to improved performance and a smoother user experience. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **JSX (JavaScript Syntax Extension):** JSX allows developers to write HTML-like syntax within JavaScript code, making the code more readable and easier to write. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **One-way Data Binding:** React uses unidirectional data flow, meaning data flows in a single direction, which makes it easier to understand and debug applications. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **Performance:** React enhances performance by using techniques like virtual DOM and efficient diff algorithms to minimize direct DOM manipulations. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **Flexibility and Modularity:** React's component-based architecture allows developers to build modular and maintainable code, making it flexible to use in various projects. [Source](https://legacy.reactjs.org/docs/design-principles.html)

These features collectively contribute to React's efficiency and popularity in building dynamic and responsive web applications.</small>

## Q3: What are React Hooks and why are they used?

<small>**Answer:** React Hooks are functions that allow you to "hook into" React state and lifecycle features from function components. Introduced in React version 16.8, Hooks enable the use of state and other React features without writing class components. They simplify code and promote the reuse of stateful logic across components. Commonly used Hooks include `useState` for state management and `useEffect` for handling side effects.</small>


## Q4: What are the differences between functional and class components in React?

**Answer:**
 <small>
In React, components can be created as either functional or class components.

- **Functional Components:** These are simple JavaScript functions that accept props as arguments and return React elements. They do not have their own state or lifecycle methods.

- **Class Components:** These are ES6 classes that extend from `React.Component`. They can have their own state and lifecycle methods, allowing for more complex logic and interactions.

With the introduction of Hooks in React 16.8, functional components can now manage state and side effects, reducing the need for class components.
 </small>


 ## Q5: What are the props, states, and differences between props and state in React?
<small>
In React, **props** (short for "properties") and **state** are both used to manage data within components, but they serve different purposes and have distinct characteristics.

- **Props:** Props are read-only attributes passed from a parent component to a child component. They allow data to flow down the component hierarchy and are immutable, meaning a child component cannot modify its own props. This ensures a unidirectional data flow, making the application predictable and easier to debug.

- **State:** State is a mutable data structure that holds information about the component's current situation. It is managed within the component itself and can change over time, usually in response to user actions or network responses. When a component's state changes, React re-renders the component to reflect the updated state.

**Key Differences:**

- **Mutability:** Props are immutable; state is mutable.

- **Ownership:** Props are controlled by the parent component; state is managed within the component.

- **Purpose:** Props allow data to be passed to child components; state is used to manage dynamic data within a component.
</small>
 
