# What is TypeScript
TypeScript is a programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript and adds optional static typing to the language. It is designed for the development of large applications and transpiles to JavaScript.

# Commmands
## Install
```node
npm install -g typescript
```
## Check Version
```node
tsc -v
```

# Things to know
## Transpile file before execution
Because browser can't understand typescipt. 

## tsconfig.json
Configuration file

## var vs let vs const
### var
Variables in TypeScript can be declared using var keyword, same as in JavaScript. The scoping rules remains the same as in JavaScript.   
### let 
To solve problems with var declarations, ES6 introduced two new types of variable declarations in JavaScript, using the keywords let and const.   
###  const 
Variables can be declared using const similar to var or let declarations. The const makes a variable a constant where its value cannot be changed. Const variables have the same scoping rules as let variables.   

## Type Assertion
Type assertion allows you to set the type of a value and tell the compiler not to infer it. This is when you, as a programmer, might have a better understanding of the type of a variable than what TypeScript can infer on its own.
### There are two ways to do type assertion in TypeScript:
### 1. Using the angular bracket <> syntax. So far in this section, we have used angular brackets to show type assertion.(More common)
```typescript
let code: any = 123; 
let employeeCode = <number> code; 
```
### 2. Using as keyword
```typescript
let code: any = 123; 
let employeeCode = code as number;
```
