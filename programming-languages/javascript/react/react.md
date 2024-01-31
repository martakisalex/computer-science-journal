# React

<img src="https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-1024.png" width="100" height="100">

## Overview

React is a declarative, efficient, and flexible JavaScript library for building user interfaces. It's maintained by Facebook and a community of individual developers and companies. React has gained immense popularity in the web development community for its simplicity and functionality.

## Key Features

- **Component-Based Architecture**: Build encapsulated components that manage their own state, then compose them to make complex UIs.
- **Declarative Views**: Design views for each state in your application, and React will efficiently update and render the right components when data changes.
- **Virtual DOM**: Provides a virtual representation of the UI, enabling efficient updates and rendering.
- **JSX**: Syntax extension for JavaScript, which allows you to write HTML structures in the same file as JavaScript code.

## Advantages

- **Efficiency**: React's efficient update and rendering system (using Virtual DOM) improves performance.
- **Flexibility**: Can be used with a variety of other libraries or frameworks, such as Redux for state management.
- **Strong Community Support**: Large community and ecosystem, with numerous third-party plugins, extensions, and tools.
- **Reusable Components**: Components can be reused across different parts of the application or even in different projects.

## Use Cases

- Single Page Applications (SPAs).
- Interactive web interfaces.
- Complex enterprise-level front-end applications.
- Mobile applications using React Native.

## Development Environment

- **Create React App**: Officially supported way to create single-page React applications.
- **Next.js**: Framework for server-rendered or statically exported React applications.
- **React Developer Tools**: Browser extensions for debugging React applications.
- **Popular IDEs**: Visual Studio Code, Sublime Text, Atom.

## Getting Started

```jsx
import React from 'react';
import ReactDOM from 'react-dom';

function Hello() {
  return <h1>Hello, world!</h1>;
}

ReactDOM.render(<Hello />, document.getElementById('root'));
```

This simple example demonstrates creating a React component and rendering it to the DOM. React's component-based approach and powerful features make it a go-to solution for building dynamic and responsive web interfaces.

This Markdown text provides an introductory overview of React, its key features, advantages, use cases, and a basic example to get started. It's suitable for educational materials or documentation related to web development using React.

## CLI Tools
Here is the list of most common CLI tools for React development:
- [create-react-app](https://create-react-app.dev/)
- [vite](https://vitejs.dev/)

## Create React App
Create React App is the CLI based tool and is the best way to start building a new single-page application in React.

It sets up your development environment so that you can use the latest JavaScript features, provides a nice developer experience, and optimizes your app for production. You’ll need to have Node >= 14.0.0 and npm >= 5.6 on your machine.

Visit the following resources to learn more:
- [Official Docs](https://react.dev/learn/start-a-new-react-project)
- [Advanced: Custom Setup with Webpack](https://www.robinwieruch.de/minimal-react-webpack-babel-setup/)

## Components
Components are the building blocks of React applications. They let us split the UI into independent, reusable pieces, and think about each piece in isolation.

Visit the following resources to learn more:
- [Creating and nesting components](https://react.dev/learn#components)
- [Explore the different types of components in React](https://www.robinwieruch.de/react-component-types/)
- [What is the difference between components, elements, and instatnces?](https://www.robinwieruch.de/react-element-component/)

### Creating and nesting components
React apps are made out of components. A component is a piece of the UI (user interface) that has its own logic and appearance. A component can be as small as a button, or as large as an entire page.

React components are JavaScript functions that return markup:
```jsx
function MyButton() {
  return (
    <button>I'm a button</button>
  );
}
```

Now that you’ve declared `MyButton`, you can nest it into another component:

```jsx
export default function MyApp() {
  return (
    <div>
      <h1>Welcome to my app</h1>
      <MyButton />
    </div>
  );
}
```

Notice that `<MyButton />` starts with a capital letter. That’s how you know it’s a React component. React component names must always start with a capital letter, while HTML tags must be lowercase.

## Helpful Links
- [explain like I'm five](https://dev.to/bartzalewski/explain-like-im-5-front-end-developer-interview-questions-2024-92n)
- [bunderler](https://snipcart.com/blog/javascript-module-bundler)