# Advantages of using React
- building complex and reusable user interface components
- React works by constructing the screen on a component-by-component basis, triggering a re-render when a component's state changes, comparing the previous re-render to the current re-render via the Virtual DOM, and only reflecting the changes in the DOM.

# Pros and Cons of SPA

### Pros
1. **Speed and Responsiveness -> Enhanced user experience**
   
SPA loads content dynamically, which means that when a user interacts with the application, only the required resources are fetched from the server. This reduces loading times and results in a smoother user experience.
   
2. **Reduced Server Load**

SPA shifts a lot of processing from the server to the client side. This reduction in server load can result in cost savings.

3. **Cross-platform compatibility**

By using JavaScript frameworks like React, Angular, or Vue.js, you can create a single codebase that runs on various platforms, including web browsers, mobile devices, and even desktop applications.

4. **Offline functionality**

Service workers and caching techniques can be implemented in SPAs to enable offline functionality.

### Cons
1. **SEO(Search Engine Optimization) challenges**
Since most of the content is loaded dynamically via JavaScript, search engines may have difficulty indexing the content.

2. **Initial Loading Time**
While SPAs excel in providing a fast and responsive user experience once they are loaded, their initial loading time can be longer than that of traditional websites. This is because the entire application must be loaded initially.

3. **Browser History and bookmark**
SPAs use client-side routing, which means that browser history and bookmarks may not work as expected. Users might find it challenging to share links

4. **Security Concerns**
SPAs can be vulnerable to certain security issues, such as Cross-Site Scripting (XSS) attacks if not properly secured. Developers need to pay extra attention to security measures when building SPAs to protect against potential threats.


https://medium.com/@VAISHAK_CP/the-pros-and-cons-of-single-page-applications-spas-06d8a662a149

# Keys in React

### Importances
- help react identify which elements were added, changed, or removed. -> Without keys, React does not understand the order or uniqueness of each element.
- Keys should be given to array elements to provide a unique identity for each element.

# Functional and class components

||Functional|Class|
|-|---|---|
|Hooks|use| not use|
|Declaration|using an arrow function or the function keyword|using the ES6 class|
|Handling props|props provided as an argument|using `this` keyword to get props|
|Handling state|use React hooks|variable in class|

# Virtual DOM

### Definition
Virtual DOM is a concept where a virtual representation of the real DOM is kept inside the memory and is synced with the real DOM by a library such as ReactDOM.

### Why was Virtual DOM introduced?
DOM manipulation is quite slow when compared to other operations in JavaScript. Most JavaScript frameworks update the entire DOM even when a small part of the DOM changes. To address the problem of inefficient updating, the react team introduced the concept of virtual DOM.

### How does it work?
<img width="832" alt="image" src="https://github.com/OHSOHYEON00/TIL/assets/132743799/5ff94e53-eb52-4038-b789-2c26928e292e">

React uses two virtual DOMs to render the user interface. 
-  to store the current state of the objects
-  to store the previous state of the objects

Whenever the virtual DOM gets updated -> React compares the two virtual DOMs and gets to know which virtual DOM objects were updated -> React renders only those objects inside the real DOM instead of rendering the complete real DOM

# Side Effects

### Definition
Any operations or behaviors that occur in a component after rendering, and that don't directly impact the current component render cycle.

### Types
data fetching, subscriptions, manually changing the DOM

# Props drilling

<img width="993" alt="image" src="https://github.com/OHSOHYEON00/TIL/assets/132743799/b341df49-12f5-4124-a4d0-b1598f44cbe8">
Components are in the hierarchy. To pass data between components, we pass props from a source component and keep passing the prop to the next component in the hierarchy.

**Disadvantage**: the components that should otherwise be not aware of the data have access to the data

# React hooks

---------------------------------

# How to prevent re-renders

# Techniques to optimiza React app

# Higher Order Components

### Definition
Higher-Order Component(HOC) is a function that takes in a component and returns a new component.

<img width="428" alt="image" src="https://github.com/OHSOHYEON00/TIL/assets/132743799/907d9ad1-17cd-42fd-b89f-6e04248145d5">

# Component Lifecycle



https://www.interviewbit.com/react-interview-questions
