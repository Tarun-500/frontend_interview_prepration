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


 ## Q6 : State Lifting - 
<small>
in React means a child component sending data to its parent component using a callback function.
</small>










###################

##################


1) what is component in react js ? - a component in React is a small code snippet that you can reuse in different parts of your app to make UI elements.


2) shadow dom and virtual dom are the same thing / difference between / ?


3) Pure Component - A pure component in React is one that only re-renders when its props or state change. It helps optimize performance by preventing unnecessary renders when the component's data hasn't changed.




4) Functional Component - functional component in React is like a simple JavaScript function that takes some information and shows it on the screen. It's straightforward and mainly used for displaying things on web pages.


5) Class Component - A class component in React is a special type of component that's like a detailed plan for creating different parts of a website. It's used for adding extra features and handling more complex tasks compared to simpler components.


6) class vs function component - Syntax:
Class components are defined using ES6 class syntax, extending the React.Component class.
Functional components are simple JavaScript functions that return JSX.
State Management:-
Class components have local component state, managed using this.state and this.setState().
Functional components can manage state using hooks like useState.
Lifecycle Methods:-
Class components have lifecycle methods like componentDidMount, componentDidUpdate, etc., for managing component lifecycle.
Functional components can use hooks like useEffect to perform side effects similar to lifecycle methods.
Complexity:-
Class components tend to be more verbose and have a steeper learning curve due to the class-based syntax.
Functional components are simpler and more lightweight, promoting a functional programming style.
Performance:-
Functional components are generally considered more performant due to their simpler nature and better optimization by React.
These points highlight the main differences between class and functional components in React, with functional components being the preferred choice in modern React development, especially with the introduction of hooks.



7)  Higher-Order Component (HOC) - : It's a function that takes a component as input and returns a new component with extra features, helping to reuse code and enhance functionality.

 &

 A Higher Order Component (HOC) in React is a function that takes a component as input and returns a new component. It helps share common functionality across multiple components without duplicating code.



8) React Fiber -   React Fiber is like a behind-the-scenes worker in React that manages how components are rendered and updated. It makes things faster and smoother, even allowing for things like rendering multiple components at once.



9) key -The key attribute in React is used to uniquely identify and efficiently update elements in lists.



10) Conditional routing - in React is about displaying different pages or parts of a website depending on factors like whether a user is logged in or not. This is usually done using React Router, where you set up routes and decide which page to show based on things like if a user is signed in or not.



11) React hooks - are functions that allow you to use state and other React features in functional components, replacing class-based components, making it easier to manage state and side effects in your application.
functional components manage state, perform side effects, and access React features without using classes. They simplify code and enable easier reuse of logic. Common hooks like useState for state management and useEffect for side effects are widely used in React development.


12) React fragment - acts like an invisible wrapper, allowing you to group elements without adding extra containers to the HTML output.



13) useMemo - in React caches the result of a function and returns it, preventing unnecessary recalculations, particularly helpful for expensive computations, and re-executes only when the dependencies change.



14) React lifecycle - consists of three main phases: mounting, updating, and unmounting. During mounting, a component is created and inserted into the DOM. During updating, a component can re-render due to changes in props or state. During unmounting, a component is removed from the DOM.


15) Impure Component - in React.js is a component that re-renders whenever its parent component re-renders.



16)  Redux component and container - Components are for displaying UI elements, while containers are connected to Redux for managing state.



17) UseMemo vs useCallback - 

useCallback: Keeps a function from changing unnecessarily, good for preventing unnecessary re-renders.
useCallback: Keeps a function stable to avoid extra rendering in React components.

useMemo: Stores a value to avoid doing the same calculation again, helps make components faster.
useMemo: Stores the result of a function to save time on repeated calculations. Helps speed up React components.



18)
 const [Count, setCount] = React.useState(0) 
    function btnClick() {
        setCount(Count + 2);
        setCount(Count + 2);
        setCount(Count + 2);
    }
    // output 2 
    
    
    function btnClick2() {
        setCount((val) => val + 2);
        setCount((val) => val + 2);
        setCount((val) => val + 2);
    }
    // output 6 



19) what are the key features of react js - 
 there are 7 key features in react js  - 1. virtual dom, 2. component based architecture, 3. JSX. 4.Declarative syntax, 5. Reusability & composition, 6. community & ecosystem 7. React Hooks.
 


1) What is the React? and what is the role of react in software development?
2) What are the key features of React Js?
3) useCallBack function
4) instance method

5) Event Handling





 
