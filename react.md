# Commands
## Start 
```react
npm start
```
## Build(For Production)
```react
npm build
```

# React Core Concepts

## JSX 
You may use quotes to specify string literals as attributes:
```JSX
const element = <a href="https://www.reactjs.org"> link </a>;
```
You may also use curly braces to embed a JavaScript expression in an attribute:
```JSX
const element = <img src={user.avatarUrl}></img>;
```
Don’t put quotes around curly braces when embedding a JavaScript expression in an attribute. You should either use quotes (for string values) or curly braces (for expressions), but not both in the same attribute.
Babel compiles JSX down to React.createElement() calls.

### These two examples are identical:
```JSX
const element = (
  <h1 className="greeting">
    Hello, world!
  </h1>
);
```
```JSX
const element = React.createElement(
  'h1',
  {className: 'greeting'},
  'Hello, world!'
);
```

React.createElement() performs a few checks to help you write bug-free code but essentially it creates an object like this:
```JSX
// Note: this structure is simplified
const element = {
  type: 'h1',
  props: {
    className: 'greeting',
    children: 'Hello, world!'
  }
};
```
These objects are called “React elements”. You can think of them as descriptions of what you want to see on the screen. React reads these objects and uses them to construct the DOM and keep it up to date.
## Elements
An element describes what you want to see on the screen:
```JSX
const element = <h1>Hello, world</h1>;
```
Unlike browser DOM elements, React elements are plain objects, and are cheap to create. React DOM takes care of updating the DOM to match the React elements.

## Components
Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

### Function and Class Components

The simplest way to define a component is to write a JavaScript function:
```JSX
function Welcome(props) {
  return <h1>Hello, {props.name}</h1>;
}
```
You can also use an ES6 class to define a component:
```JSX
class Welcome extends React.Component {
  render() {
    return <h1>Hello, {this.props.name}</h1>;
  }
}
```

## JSX.Element vs ReactElement vs ReactNode
A ReactElement is an object with a type and props.
```typescript
 type Key = string | number

 interface ReactElement<P = any, T extends string | JSXElementConstructor<any> = string | JSXElementConstructor<any>> {
    type: T;
    props: P;
    key: Key | null;
}
```
A ReactNode is a ReactElement, a ReactFragment, a string, a number or an array of ReactNodes, or null, or undefined, or a boolean:
```typescript
type ReactText = string | number;
type ReactChild = ReactElement | ReactText;

interface ReactNodeArray extends Array<ReactNode> {}
type ReactFragment = {} | ReactNodeArray;

type ReactNode = ReactChild | ReactFragment | ReactPortal | boolean | null | undefined;
```

JSX.Element is a ReactElement, with the generic type for props and type being any. It exists, as various libraries can implement JSX in their own way, therefore JSX is a global namespace that then gets set by the library, React sets it like this:
```typescript
declare global {
  namespace JSX {
    interface Element extends React.ReactElement<any, any> { }
  }
}
```
## Props
## State
