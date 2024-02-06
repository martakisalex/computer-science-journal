# [React: Element vs Component](https://www.robinwieruch.de/react-element-component/)

```javascript
const App = () => {
  return <p>Hello React</p>;
};
```
A React component is literally the declaration of a component as we see it in the previous code snippet. In our case, it's a function component but it could be any other kind of React component (e.g. React Class Component) too.

We can extract a component from another component and render it the following way. Rendering a component happens whenever we use this component as a React element with angle brackets (e.g. `<Greeting />`) in another component:

```javascript
const Greeting = ({ text }) => {
  return <p>{text}</p>;
};

const App = () => {
  return <Greeting text="Hello React" />;
};
```

We can render a component as React element multiple times too. Whenever a component gets rendered as element, we create an instance of this component:

```javascript
const Greeting = ({ text }) => {
  return <p>{text}</p>;
};

const App = () => {
  return (
    <>
      <Greeting text="Hello Instance 1 of Greeting" />
      <Greeting text="Hello Instance 2 of Greeting" />
    </>
  );
};
```

While a React component is declared once, it can be used multiple times as a React element in JSX. When it is used, it becomes an instance of the component and lives in React's component tree. Essentially that's the explanation of React components, element, and instance in a nutshell. However, in order to understand everything on a deeper level, we need to understand how React displays HTML with JSX.

## React Element in Depth

Let's take one step back and start with a simple example again:
```javascript
const App = () => {
  return <p>Hello React</p>;
};
```

Whenever a React component gets called (rendering), React calls its React.createElement() method internally which returns the following object:

```javascript
console.log(App());

// {
//   $$typeof: Symbol(react.element)
//   "type": "p",
//   "key": null,
//   "ref": null,
//   "props": {
//     "children": "Hello React"
//   },
//   "_owner": null,
//   "_store": {}
// }
```
Focus your attention on the type and props properties of this object: While the type represents the actual HTML element, the props are all HTML attributes (plus the inner content, read: children) which are passed to this HTML element.

When looking at the paragraph HTML element from above, you can see that no attributes are passed to it. However, React treats children as pseudo HTML attribute whereas children represents everything that's rendered between the HTML tag. This fact becomes clearer when adding an attribute to the paragraph HTML element:

```javascript
const App = () => {
  return <p className="danger">Hello React</p>;
};

console.log(App());

// {
//   $$typeof: Symbol(react.element)
//   "type": "p",
//   "key": null,
//   "ref": null,
//   "props": {
//     "children": "Hello React",
//     "className": "danger"
//   },
//   "_owner": null,
//   "_store": {}
// }
```