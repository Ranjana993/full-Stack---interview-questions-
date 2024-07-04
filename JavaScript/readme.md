# JavaScript Interview Questions

### 1. What is JavaScript?
**Answer** : JavaScript is a high-level, interpreted programming language that is primarily used for creating and enhancing web pages. It is an essential part of web applications, enabling interactive features and dynamic content.


### 2. What are the different data types present in JavaScript?
**Answer** : JavaScript has the following primitive data types:
- `Number`: Represents both integer and floating-point numbers.
- `String`: Represents sequences of characters.
- `Boolean`: Represents true or false.
- `Null`: Represents the intentional absence of any object value.
- `Undefined`: Represents a variable that has been declared but not assigned a value.
- `Symbol`: Represents a unique and immutable value.

### 3. How do you declare a variable in JavaScript?
**Answer** : Variables in JavaScript can be declared using var, let, or const keywords.
```
var name = 'John';
let age = 30;
const isMarried = false;
```

### 4. What is the difference between let and const?
**Answer** : In JavaScript, let and const are both used to declare variables, but they serve different purposes and have distinct behaviors. The let keyword allows for the declaration of variables that can be reassigned, making it useful when the value of the variable needs to change. It is block-scoped, meaning the variable is only accessible within the block (enclosed in curly braces {}) where it is defined, and it is not hoisted, so it cannot be used before its declaration. On the other hand, const is used to declare variables with immutable bindings, which means that once a value is assigned to a const variable, it cannot be reassigned. Like let, const is also block-scoped and not hoisted. However, while the binding of const variables is immutable, the content of objects or arrays assigned to them can still be modified.

### 5. How do you create a function in JavaScript?
**Answer**: Functions can be created using the function declaration or function expression syntax.
```
// Function declaration
function greet(name) {
    return `Hello, ${name}!`;
}

// Function expression
const greet = function(name) {
    return `Hello, ${name}!`;
};
```

### Function Declaration vs Function Expression:
**Explanation**: JavaScript functions can be defined using either a function declaration or a function expression. Function declarations are hoisted, meaning they're available throughout the scope before the actual execution.

```
// Function Declaration
function greet(name) {
    return `Hello, ${name}!`;
}

// Function Expression
const greet = function(name) {
    return `Hello, ${name}!`;
};

```

### Arrow Function: 
Arrow function {()=> } is concise way of writing JavaScript functions in shorter way. Arrow functions were introduced in the ES6 version. They make our code more structured and readable.
- Arrow functions are anonymous functions i.e. functions without a name but they are often assigned to any variable. They are also called ` Lambda Functions ` .

### 7. What are template literals?
**Answer** : Template literals, also known as template strings, are a feature in JavaScript that allow for easier and more flexible string formatting and interpolation. They are enclosed by backticks (`) instead of single or double quotes.

### JavaScript this Keyword
**Answer** : In JavaScript, this keyword refers to the current context or scope within which code is executing. Its value is determined by how a function is called, and it can dynamically change depending on the invocation context


#### The this keyword refers to different objects depending upon how it is used:
- When used within a method of an object, this points to that object.
- When used by itself, this points to the global object.
- Within a function, this typically points to the global object.
- In a function under strict mode, this becomes undefined.
- During an event, this points to the element that triggered the event.
- Methods such as call(), apply(), and bind() can reassign this to any desired object.