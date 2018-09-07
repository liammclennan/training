Hello World
===========

React is a JavaScript library for building user interfaces. 

A react application is built from a set of __components__ arranged in a hierarchy. 

A __component__ is a template for generating a chunk of __DOM__ from some data. This is a component:

```jsx
const HelloWorld = (props) =>
  <div>Hello {props.name}</div>;
```

Note that component identifiers must start with an uppercase letter.

A __component__ combined with its data is called an __element__. This is an element:

```html
<HelloWorld name="Ernesto" />
```

See how it is a component (`HelloWorld`) combined with some data (`name="Ernesto"`)?

This xml-like syntax is called JSX. It helps us to combine components in a way that is easy to read and assimilate. Since JSX is not valid JavaScript scripts containing JSX syntax must be compiled to JavaScript using Babel or Typescript. We will investigate JSX later, for now just trust me that it is a __good thing__. 

Rendering
---------

To start (render) a React application we use the `ReactDOM.render` function. 

```javascript 
ReactDOM.render(<HelloWorld name="Ernesto" />, document.getElementById("app"));
```

Exercise: [HelloWorld](https://codepen.io/liammclennan/pen/jvVqLY?editors=0010)