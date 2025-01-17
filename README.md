# React Basics Syllabus:

[Short Video](https://www.youtube.com/watch?v=wIyHSOugGGw)

| ReactJS Basic Concepts                                                       | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ---------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Introduction to JSX                                                          | JSX (JavaScript XML) is a syntax extension for React.js that allows developers to write HTML elements.                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| Rendering Elements                                                           | Rendering Elements in React involves efficiently updating the user interface by creating and updating virtual representations of the UI components.                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Components                                                                   | Components in React are modular, reusable building blocks for UI elements.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Fragments                                                                    | We may render a single element or multiple elements, though rendering multiple elements will require a ‘div’ tag called Fragment                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| Props                                                                        | React allows us to pass information to a Component using something called props.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| PropTypes                                                                    | use the propType for validating any data we are receiving from props.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| States                                                                       | React JS State is a way to store and manage the information or data while creating a React Application.                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Conditional Rendering                                                        | Rendering based on the conditions called conditional rendering in React.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| React JS Lists/ React JS Keys/ React JS Refs/ React JS forms/ React JS Hooks | 1. React Lists are very useful when it comes to developing the UI of any website <br/>2. React JS keys are a way of providing a unique identity to each item while creating the React JS Lists so that React can identify the element to be processed.<br/>3. React JS Refs are used to access and modify the DOM elements in the React Application.<br/>4. In React Forms, All the form data is stored in the React’s component state<br/>5. Hooks are used to give functional components an access to use the states and are used to manage side-effects in React. |
| Router                                                                       | In React mostly SPA are developed so Navigation is complex.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| ReactDOM                                                                     | React provides the developers with a package react-dom to access and modify the DOM.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| EventHandling                                                                | Modern webpages rely on user interactions, triggering events like clicks or keypresses.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Synthetic Events                                                             | Synthetic events in React are cross-browser wrappers around the browser’s original event.                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| ContextAPI                                                                   | Context API is used to pass global variables anywhere in the code.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Controlled Components                                                        | React’s Controlled Components manage form data via component state, receiving values through props and updating through callbacks like onChange.                                                                                                                                                                                                                                                                                                                                                                                                                     |

## Features of React:

1. Component-Based Architecture.
2. JSX (JavaScript Syntax Extension).
3. Virtual DOM.
4. One-way Data Binding (Top to bottom).
5. Performance.
6. Components.
7. Single-Page Applications (SPAs).

## ReactJS Lifecycle:

1. Initialization.
2. Mounting Phase.
3. Updating Phase.
4. Unmounting Phase.

## JSX :

### What is JSX?

1. JSX stands for JavaScript XML. JSX is basically a syntax extension of JavaScript.
2. React JSX helps us to write HTML in JavaScript and forms the basis of React Development.
3. JSX creates an element in React that gets rendered in the UI. It is transformed into JavaScript functions by the compiler at runtime. Error handling and warnings become easier to handle when using JSX.

### Why JSX ?

1. It is faster than normal JavaScript as it performs optimizations while translating to regular JavaScript.
2. It makes it easier for us to create templates.
3. Instead of separating the markup and logic in separate files, React uses components for this purpose. We will learn about components in detail in further articles.
4. As JSX is an expression, we can use it inside of if statements and for loops, assign it to variables, accept it as arguments, or return it from functions.

### How is it used?

1. **Expressions in JSX** :
   In React we are allowed to use normal JavaScript expressions with JSX. To embed any JavaScript expression in a piece of code written in JSX we will have to wrap that expression in curly braces {}. The below example specifies a basic use of JavaScript Expression in React.
2. **Attributes in JSX**:
   _JSX allows us to use attributes with the HTML elements just like we do with normal HTML. But instead of the normal naming convention of HTML, JSX uses the camelcase convention for attributes._
   - **The change of class attribute to className**:The class in HTML becomes className in JSX. The main reason behind this is that some attribute names in HTML like ‘class‘ are reserved keywords in JavaScript. So, in order to avoid this problem, JSX uses the camel case naming convention for attributes.
   - **Creation of custom attributes**:We can also use custom attributes in JSX. For custom attributes, the names of such attributes should be prefixed by `data-\*` attribute.

## Babel:

### Using Babel with React

We use Babel with React to transpile the JSX code into simple React functions that can be understood by browsers. Using this way we can assure that our JSX code can work in almost any browser. This combination is widely used in modern-day web development.

### Why do we need Babel?

The main reason we need Babel is that it gives us the privilege to make use of the latest things JavaScript has to offer without worrying about whether it will work in the browser or not.

### Features of Babel:

1. Babel-Plugins: The Plugins are configuration details for Babel to transpile the code that supports a number of plugins, which could be used individually, provided the environment is known.
2. Babel-Presets: Babel presets have a set of plugins that instruct Babel to transpile in a specific mode. provided the environment is known.
3. Babel-Polyfills: During instances when methods and objects, cannot be transpiled, We can make use of babel-polyfill to facilitate the use of features in any browser.
4. Babel-CLI: The Command-line interface of Babel has a lot of commands where the code can be easily compiled on the command line. It also has features like plugins and presets to be used along with the command making it easy to transpile the code at once.

## Virtual DOM

In React, everything is treated as a component be it a functional component or class component. A component can contain a state. Whenever the state of any component is changed react updates its Virtual DOM tree. Though it may sound like it is ineffective the cost is not much significant as updating the virtual DOM doesn’t take much time.

React maintains two Virtual DOM at each time, one contains the updated Virtual DOM and one which is just the pre-update version of this updated Virtual DOM. Now it compares the pre-update version with the updated Virtual DOM and figures out what exactly has changed in the DOM like which components have been changed. This process of comparing the current Virtual DOM tree with the previous one is known as `‘diffing’`. Once React finds out what exactly has changed then it updates those objects only, on real DOM.

React uses something called batch updates to update the real DOM. It just means that the changes to the real DOM are sent in batches instead of sending any update for a single change in the state of a component.

We have seen that the re-rendering of the UI is the most expensive part and React manages to do this most efficiently by ensuring that the Real DOM receives batch updates to re-render the UI. This entire process of transforming changes to the real DOM is called `Reconciliation`.

This significantly improves the performance and is the main reason why React and its Virtual DOM are much loved by developers all around.

### ReactDOM

#### Important functions provided by ReactDOM

1. render(): This is one of the most important methods of ReactDOM. This function is used to render a single React Component or several Components wrapped together in a Component or a div element.
2. findDOMNode(): This function is generally used to get the DOM node where a particular React component was rendered. This method is very less used like the following can be done by adding a ref attribute to each component itself.
3. unmountComponentAtNode(): This function is used to unmount or remove the React Component that was rendered to a particular container.
4. hydrate(): This method is equivalent to the render() method but is implemented while using server-side rendering.
5. createPortal(): It allow us to render a component into a DOM node that resides outside the current DOM hierarchy of the parent component.

#### Key features of ReactDOM :

1. ReactDOM.render() replaces the child of the given container if any. It uses a highly efficient diff algorithm and can modify any subtree of the DOM.
2. React findDOMNode() function can only be implemented upon mounted components thus Functional components can not be used in findDOMNode() method.
3. ReactDOM uses observables thus provides an efficient way of DOM handling.
4. ReactDOM can be used on both the client-side and server-side.

## React Lists

```jsx
import React from "react";
import ReactDOM from "react-dom";
function Navmenu(props) {
  const list = props.menuitems;

  const updatedList = list.map((listItems) => {
    return <li key={listItems.toString()}>{listItems}</li>;
  });

  return <ul>{updatedList}</ul>;
}

const menuItems = [1, 2, 3, 4, 5];

ReactDOM.render(
  <Navmenu menuitems={menuItems} />,
  document.getElementById("root")
);
```

### Conclusion

In summary, React lists are arrays with values. To render the elements of an array we iterate over each element and create a JSX element for each item. We use keys to label list elements, and when the changes are made to the list we don’t need to re-render the entire list.
