<details>
<summary> <h2>Q1: What is React.js and why do we use it?</h2> </summary>
 <small>React.js is a JavaScript library for building user interfaces, particularly single-page applications (SPAs). Developed by Facebook in 2011, it was first deployed on Facebook's News Feed and later open-sourced in 2013. React enables developers to create large web applications that can update and render efficiently in response to data changes. It emphasizes a component-based architecture, allowing for reusable UI components, and utilizes a virtual DOM to enhance performance by minimizing direct manipulations of the actual DOM.</small>
</details>


<details>
<summary> <h2>  Q2: What are the key features of React.js? </h2> </summary>
 <small>
 There are 7 key features in React JS: 1. virtual dom, 2. component-based architecture, and 3. JSX. 4. Declarative syntax, 5. Reusability & composition, 6. community & ecosystem 7. React Hooks.
 React.js offers several key features that make it a popular choice for building dynamic user interfaces:

- **Declarative Syntax:** React follows a declarative programming paradigm, enabling developers to design views for each state in the application, and React efficiently updates and renders components as data changes. This approach enhances code readability and maintenance. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **Component-Based Architecture:** Applications in React are built using encapsulated components that manage their own state. This modularity promotes code reuse and simplifies both development and maintenance. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **Virtual DOM:** React utilizes a virtual DOM, an in-memory representation of the real DOM. When the state of an object changes, the virtual DOM updates only that specific object in the real DOM, leading to improved performance and a smoother user experience. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **JSX (JavaScript Syntax Extension):** JSX allows developers to write HTML-like syntax within JavaScript code, making the code more readable and easier to write. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **One-way Data Binding:** React uses unidirectional data flow, meaning data flows in a single direction, which makes it easier to understand and debug applications. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **Performance:** React enhances performance by using techniques like virtual DOM and efficient diff algorithms to minimize direct DOM manipulations. [Source](https://legacy.reactjs.org/docs/design-principles.html)

- **Flexibility and Modularity:** React's component-based architecture allows developers to build modular and maintainable code, making it flexible to use in various projects. [Source](https://legacy.reactjs.org/docs/design-principles.html)

These features collectively contribute to React's efficiency and popularity in building dynamic and responsive web applications.
</small>
</details>

 


<details>
<summary> <h2> Q3: What are React Hooks and why are they used?  </h2> </summary>
<small>
**Answer:** React Hooks are functions that allow you to "hook into" React state and lifecycle features from function components. Introduced in React version 16.8, Hooks enables the use of state and other React features without writing class components. They simplify code and promote the reuse of stateful logic across components. Commonly used Hooks include `useState` for state management and `useEffect` for handling side effects.
</small>
</details>



<details>
<summary> <h2> Q4: What are the differences between functional and class components in React? </h2> </summary>

**Answer:**
 <small>
In React, components can be created as either functional or class components.

- **Functional Components:** These are simple JavaScript functions that accept props as arguments and return React elements. They do not have their own state or lifecycle methods.

- **Class Components:** These are ES6 classes that extend from `React.Component`. They can have their own state and lifecycle methods, allowing for more complex logic and interactions.
 
**Class vs Function Component**  

### Syntax:
- Class components are defined using ES6 class syntax, extending the `React.Component` class.
- Functional components are simple JavaScript functions that return JSX.

### State Management:
- Class components have local component state, managed using `this.state` and `this.setState()`.
- Functional components can manage state using hooks like `useState`.

### Lifecycle Methods:
- Class components have lifecycle methods like `componentDidMount`, `componentDidUpdate`, etc., for managing component lifecycle.
- Functional components can use hooks like `useEffect` to perform side effects similar to lifecycle methods.

### Complexity:
- Class components tend to be more verbose and have a steeper learning curve due to the class-based syntax.
- Functional components are simpler and more lightweight, promoting a functional programming style.

### Performance:
- Functional components are generally considered more performant due to their simpler nature and better optimization by React.

These points highlight the main differences between class and functional components in React, with functional components being the preferred choice in modern React development, especially with the introduction of hooks.
 

With the introduction of Hooks in React 16.8, functional components can now manage state and side effects, reducing the need for class components.
 </small>
</details>

 
 
<details>
 <summary> <h2> Q5: What are the props, states, and differences between props and states in React? </h2></summary>
 <small>
In React, **props** (short for "properties") and **state** are both used to manage data within components, but they serve different purposes and have distinct characteristics.

- **Props:** Props are read-only attributes passed from a parent component to a child component. They allow data to flow down the component hierarchy and are immutable, meaning a child component cannot modify its own props. This ensures a unidirectional data flow, making the application predictable and easier to debug.

- **State:** State is a mutable data structure that holds information about the component's current situation. It is managed within the component itself and can change over time, usually in response to user actions or network responses. When a component's state changes, React re-renders the component to reflect the updated state.

**Key Differences:**

- **Mutability:** Props are immutable; state is mutable.

- **Ownership:** Props are controlled by the parent component; the state is managed within the element.

- **Purpose:** Props allow data to be passed to child components; the state is used to manage dynamic data within a component.
</small>
</details>
 
 
<details>
 <summary> <h2> Q6 : What is  State Lifting in react js </h2> </summary>
 <small>
in React a child component sends data to its parent component using a callback function.
</small>

</details>


 
<details>
 <summary>  <h2>  Q7:  Shadow dom and virtual dom are the same thing/difference between? </h2> </summary>

 
<small>

**## 1️⃣ Shadow DOM (Secret Room 🏠)**  
Shadow DOM is a **mini isolated DOM** inside an element that keeps its styles and structure separate from the rest of the page.  

✔ **Used in:** Web Components (like `<video>`, `<input type="date">`)  
✔ **Benefit:** Prevents CSS and JS conflicts with the main page  

**🔹 Example:**  
``` 
<div id="shadow-host"></div>

<script>
  let host = document.getElementById("shadow-host");
  let shadow = host.attachShadow({ mode: "open" });

  shadow.innerHTML = `
    <style>
      .box { color: red; }
    </style>
    <div class="box">Inside Shadow DOM</div>
  `;
</script>
```
✅ **CSS inside shadow DOM will not affect the main page.**  

---  

**## 2️⃣ Virtual DOM (React’s Smart Copy 🧠)**  
Virtual DOM is a **lightweight copy of the actual DOM** that React uses to improve performance. Instead of updating the entire page, React updates only the changed parts.  

✔ **Used in:** React.js  
✔ **Benefit:** Faster updates, better performance  

**🔹 How it Works in React?**  
1️⃣ React creates a **Virtual DOM copy**.  
2️⃣ It **compares** the new and old Virtual DOM (diffing).  
3️⃣ It updates **only the changed part** in the real DOM (reconciliation).  

**🔹 Example in React:**  
```
import { useState } from "react";

function App() {
  const [count, setCount] = useState(0);

  return (
    <div>
      <h1>Count: {count}</h1>
      <button onClick={() => setCount(count + 1)}>Increment</button>
    </div>
  );
}
```
✅ **Only the count updates, not the entire page!**  

---  

**## 3️⃣ Key Differences**  

| Feature | Shadow DOM | Virtual DOM |
|---------|------------|-------------|
| **Purpose** | Isolates styles & structure | Improves performance |
| **Used In** | Web Components | React.js |
| **CSS Isolation** | ✅ Yes | ❌ No |
| **Performance Impact** | ⚡ Faster rendering | 🚀 Optimized updates |
| **Updates** | Only inside the component | Compares & updates changed parts |

---  

**## 4️⃣ Easy Way to Remember**  
👉 **Shadow DOM = Secret Room** 🏠 (Keeps styles and structure separate)  
👉 **Virtual DOM = Smart Copy** 🧠 (Makes React updates faster)  

💡 **In React.js, we use Virtual DOM, not Shadow DOM!**  

</small>

</details>


<details>
 <summary> <h2>  Q8:  Higher-Order Component (HOC) in React?</h2> </summary>
 <small>
 
**Definition:**
A Higher-Order Component (HOC) is a function that takes a component as input and returns a new component with added functionality. It helps in reusing logic across multiple components.

**Example:**
``` 
import React from 'react';

// HOC that adds a loading spinner feature
const withLoading = (WrappedComponent) => {
  return (props) => (
    props.isLoading ? <p>Loading...</p> : <WrappedComponent {...props} />
  );
};

// Normal component
const DataComponent = ({ data }) => <p>Data: {data}</p>;

// Enhanced component using HOC
const EnhancedComponent = withLoading(DataComponent);

// Usage
export default function App() {
  return <EnhancedComponent isLoading={false} data="React HOC Example" />;
}
```

**Key Points:**
- HOCs help in **code reusability** by wrapping components.
- Commonly used for **authentication, logging, or adding styles**.
- They follow the pattern **HOC(Component) → EnhancedComponent**.
- Do not modify the original component; instead, they return a new one.


Higher-Order Component (HOC) - : It's a function that takes a component as input and returns a new component with extra features, helping to reuse code and enhance functionality.
 &
A Higher Order Component (HOC) in React is a function that takes a component as input and returns a new component. It helps share common functionality across multiple components without duplicating code.
</small>
</details>



<details>
 <summary> <h2> Q9 : useMemo vs useCallback </h2> </summary>
 <small> 
#### **useCallback:**
- Returns a **memoized function**.
- Useful when passing **callback functions** to child components.
- Prevents unnecessary function recreation on re-renders.
- **Example:**
  
  ```jsx
  import React, { useState, useCallback } from 'react';

  const Button = React.memo(({ handleClick }) => {
    console.log('Button rendered');
    return <button onClick={handleClick}>Click Me</button>;
  });

  function App() {
    const [count, setCount] = useState(0);

    const increment = useCallback(() => {
      setCount(prev => prev + 1);
    }, []);

    return (
      <div>
        <p>Count: {count}</p>
        <Button handleClick={increment} />
      </div>
    );
  }

  export default App;
  ```

#### **useMemo:**
- Returns a **memoized value**.
- Optimizes expensive calculations by storing the computed result.
- **Example:**
  
  ``` 
  import React, { useState, useMemo } from 'react';

  function App() {
    const [count, setCount] = useState(0);
    const [number, setNumber] = useState(5);

    const factorial = useMemo(() => {
      console.log('Calculating factorial...');
      return number <= 1 ? 1 : number * factorial;
    }, [number]);

    return (
      <div>
        <p>Factorial: {factorial}</p>
        <button onClick={() => setNumber(number + 1)}>Increase Number</button>
        <button onClick={() => setCount(count + 1)}>Increase Count</button>
      </div>
    );
  }

  export default App;
  ```

#### **Key Differences:**
| Feature     | useCallback | useMemo |
|------------|------------|---------|
| Returns    | Memoized **function** | Memoized **value** |
| Usage      | Optimizes **functions** passed as props | Optimizes **expensive calculations** |
| Dependency | Reacts to dependency array | Reacts to dependency array |
| Purpose    | Prevents function recreation on re-renders | Avoids re-executing costly computations |

</small>
</details>







###################

##################


1) what is a component in React JS? - a component in React is a small code snippet that you can reuse in different parts of your app to make UI elements.


2) Pure Component - A pure component in React is one that only re-renders when its props or state changes. It helps optimize performance by preventing unnecessary renders when the component's data hasn't changed.

3) Impure Component - in React.js is a component that re-renders whenever its parent component re-renders.


4) Functional Component - functional component in React is like a simple JavaScript function that takes some information and shows it on the screen. It's straightforward and mainly used for displaying things on web pages.


5) Class Component - A class component in React is a special type of component that's like a detailed plan for creating different parts of a website. It's used for adding extra features and handling more complex tasks compared to simpler components.

 
6) React Fiber -   React Fiber is like a behind-the-scenes worker in React that manages how components are rendered and updated. It makes things faster and smoother, even allowing for things like rendering multiple components at once.



7) key -The key attribute in React is used to uniquely identify and efficiently update elements in lists.



8) Conditional routing - in React is about displaying different pages or parts of a website depending on factors like whether a user is logged in or not. This is usually done using React Router, where you set up routes and decide which page to show based on things like if a user is signed in or not.



9) React hooks - are functions that allow you to use state and other React features in functional components, replacing class-based components, making it easier to manage state and side effects in your application.
functional components manage state, perform side effects, and access React features without using classes. They simplify code and enable easier reuse of logic. Common hooks like useState for state management and useEffect for side effects are widely used in React development.


12) React fragment - acts like an invisible wrapper, allowing you to group elements without adding extra containers to the HTML output.



13) useMemo - in React caches the result of a function and returns it, preventing unnecessary recalculations, particularly helpful for expensive computations, and re-executes only when the dependencies change.



14) React lifecycle - consists of three main phases: mounting, updating, and unmounting. During mounting, a component is created and inserted into the DOM. During updating, a component can re-render due to changes in props or state. During unmounting, a component is removed from the DOM.
 

16)  Redux component and container - Components are for displaying UI elements, while containers are connected to Redux for managing state.
 
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
 

1) What is the React? and what is the role of react in software development?
2) What are the key features of React Js?
3) useCallBack function
4) instance method

5) Event Handling
6) container and component in redux
7) auth gurad
8) middleware - saga,thunk, slice
9) redux toolkit
10) reducer, saga, action, store
11)  React JS directory - ## React.js Default Directory Structure (Short Interview View)

When you create a React project using **Create React App (CRA)**, the default structure is:

```
my-app/
├── node_modules/
├── public/
│   └── index.html
├── src/
│   ├── App.js
│   └── index.js
├── package.json
├── .gitignore
└── README.md
```

### 📁 Key Folders

#### `public/`

* Static files.
* `index.html` is the root HTML file.

#### `src/`

* Main React code.
* `index.js`: Entry point.
* `App.js`: Root component.

#### `node_modules/`

* Auto-managed npm packages.

#### `package.json`

* Project dependencies and scripts.

---

### 📦 Real-World `src/` Structure (Optional)

```
src/
├── components/
├── pages/
├── assets/
├── hooks/
├── utils/
├── context/
├── App.js
└── index.js
```

---

### ✅ Interview Summary

> "React apps use a simple structure. `src/` and `public/` are core. Real-world apps often include `components/`, `pages/`, and `hooks/` for better organization."





12) What is React 18’s Concurrent Mode? How does it improve performance?
13) 








 
