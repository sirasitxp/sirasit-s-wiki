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
```
const element = <a href="https://www.reactjs.org"> link </a>;
```
You may also use curly braces to embed a JavaScript expression in an attribute:
```
const element = <img src={user.avatarUrl}></img>;
```
Don’t put quotes around curly braces when embedding a JavaScript expression in an attribute. You should either use quotes (for string values) or curly braces (for expressions), but not both in the same attribute.

## Components
Components allow you to build self-contained, reusable snippets of code. If you think of components as LEGO bricks, you can take these individual bricks and combine them together to form larger structures. If you need to update a piece of the UI, you can update the specific component or brick.
A component is a function that returns UI elements. 
## Props
## State
