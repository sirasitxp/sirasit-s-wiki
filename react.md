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
## Props
## State
