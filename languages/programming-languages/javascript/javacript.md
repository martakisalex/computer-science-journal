# JavaScript

<img src="https://logos-download.com/wp-content/uploads/2019/01/JavaScript_Logo.png" height="100">

## Overview

JavaScript is a versatile and widely-used programming language primarily known for its role in web development. It is an essential part of the modern web, allowing for interactive and dynamic user interfaces.

## Key Features

- **Dynamic Typing**: JavaScript is a loosely typed or a dynamic language, variables can hold any data type.
- **Asynchronous Programming**: Supports asynchronous programming with callbacks, promises, and async/await.
- **First-Class Functions**: Functions are treated as first-class citizens, meaning they can be stored in variables, passed as arguments, or returned from other functions.
- **Prototype-Based Inheritance**: Uses prototypes for inheritance, rather than classical inheritance.
- **Client-Side Scripting**: Originally designed for client-side scripting in web browsers.

## Advantages

- **Highly Versatile**: Used for both client-side and server-side development (Node.js).
- **Large Community**: Extensive community support and a vast ecosystem of libraries and frameworks.
- **Cross-Platform Compatibility**: Runs on any platform that has a JavaScript engine, which includes all modern web browsers.
- **Event-Driven and Reactive Programming**: Ideal for developing interactive web applications.

## Use Cases

- Web development (both front-end and back-end).
- Building interactive websites and web applications.
- Server applications with Node.js.
- Mobile app development with frameworks like React Native.
- Game development and desktop applications.

## Development Environment

- Can be written in any text editor or IDE.
- Primary runtime environment is web browsers, but also server environments like Node.js.

JavaScript's ubiquity and flexibility make it a staple in the field of software development, especially for web-based applications.


## Introduction to JavaScript
JavaScript, often abbreviated JS, is a programming language that is one of the core technologies of the World Wide Web, alongside HTML and CSS. It lets us add interactivity to pages e.g. you might have seen sliders, alerts, click interactions, popups, etc on different websites — all of that is built using JavaScript. Apart from being used in the browser, it is also used in other non-browser environments as well such as Node.js for writing server-side code in JavaScript, Electron for writing desktop applications, React Native for mobile applications, and so on.

### What is JavaScript?
JavaScript, often abbreviated JS, is a programming language that is one of the core technologies of the World Wide Web, alongside HTML and CSS. It lets us add interactivity to pages e.g. you might have seen sliders, alerts, click interactions, popups, etc on different websites — all of that is built using JavaScript. Apart from being used in the browser, it is also used in other non-browser environments as well such as Node.js for writing server-side code in JavaScript, Electron for writing desktop applications, React Native for mobile applications, and so on.

### History of JavaScript
JavaScript was initially created by Brendan Eich of NetScape and was first announced in a press release by Netscape in 1995. It has a bizarre history of naming; initially, it was named Mocha by the creator, which was later renamed LiveScript. In 1996, about a year later after the release, NetScape decided to rename it to JavaScript with hopes of capitalizing on the Java community (although JavaScript did not have any relationship with Java) and released Netscape 2.0 with the official support of JavaScript.

### JavaScript Versions

JavaScript was invented by Brendan Eich, and in 1997 it became an ECMA standard. ECMAScript is the official language name. ECMAScript versions include ES1, ES2, ES3, ES5, and ES6

### How to run JavaScript
JavaScript can be run in the browser by including the external script file using the `script` tag, writing it within the HTML page using the `script` tag again, or running it in the browser console.

### Javascript Variables
Most of the time, a JavaScript application needs to work with information. To store and represent this information in the JavaScript codebase, we use variables. A variable is a container for a value.

### Variable Declarations
To use variables in JavaScript, we first need to create it i.e. declare a variable. To declare variables, we use one of the var, let, or const keywords.

### [var] keyword
The `var` statement declares a function-scoped or globally-scoped variable, optionally initializing it to a value.

### [let] keyword
The `let` declaration declares a block-scoped local variable, optionally initializing it to a value.

### [const] keyword
Constants are block-scoped, much like variables declared using the let keyword. The value of a constant can’t be changed through reassignment (i.e. by using the assignment operator), and it can’t be redeclared (i.e. through a variable declaration). However, if a constant is an object or array its properties or items can be updated or removed.

### Hoisting
JavaScript Hoisting refers to the process whereby the interpreter appears to move the declaration of functions, variables, or classes to the top of their scope, prior to execution of the code.

## Dictionary

### [just-in-time (JIT) compilation](https://en.wikipedia.org/wiki/Just-in-time_compilation)
- **Just-in-time (JIT) compilation**, also referred to as **dynamic translation** or **run-time compilation**, is a process in computing where computer code is compiled during the execution of a program (at run time) rather than before execution.

### [Lightweight programming language](https://en.wikipedia.org/wiki/Lightweight_programming_language)
- **Lightweight programming languages** are designed to have small memory footprint, are easy to implement (important when porting a language to different computer systems), and/or have minimalist syntax and features.

### [First-class Function](https://developer.mozilla.org/en-US/docs/Glossary/First-class_Function)
- A programming language is said to have **First-class functions** when functions in that language are treated like any other variable. For example, in such a language, a function can be passed as an argument to other functions, can be returned by another function and can be assigned as a value to a variable.

### [Prototype-based programming](https://developer.mozilla.org/en-US/docs/Glossary/Prototype-based_programming)
- **Prototype-based programming** is a style of object-oriented programming in which classes are not explicitly defined, but rather derived by adding properties and methods to an instance of another class or, less frequently, adding them to an empty object. In simple words: this type of style allows the creation of an object without first defining its class.

### [Object](https://developer.mozilla.org/en-US/docs/Glossary/Object)
- An **Object** is a special type of value in JavaScript that can have connections with other values. Objects can be seen as a collection of properties. With the object literal syntax, a limited set of properties are initialized; then properties can be added and removed. Property values can be values of any type, including other objects, which enables building complex data structures. Properties are identified using key values. A key value is either a String value or a Symbol value. There are two types of object properties: The **data property** and the **accessor property**.

### [Object Literal](https://techstacker.com/what-is-object-literal-javascript/)
- An **Object Literal** is an object value that you *literally* write in your program/app. An Object Literal usually consists of a list of comma-separated name-value pairs (`property:value`), wrapped inside curly braces `{}`.

### [Programming paradigms](https://en.wikipedia.org/wiki/Programming_paradigm)
- **Programming paradigms** are a way to classify programming languages based on their features. Languages can be classified into multiple paradigms.

Some paradigms are concerned mainly with implications for the execution model of the language, such as allowing side effects, or whether the sequence of operations is defined by the execution model. Other paradigms are concerned mainly with the way that code is organized, such as grouping a code into units along with the state that is modified by the code. Yet others are concerned mainly with the style of syntax and grammar.

Some common programming paradigms include:

- Imperative in which the programmer instructs the machine how to change its state,
  - procedural which groups instructions into procedures,
  - object-oriented which groups instructions with the part of the state they operate on,
- Declarative in which the programmer merely declares properties of the desired result, but not how to compute it
functional in which the desired result is declared as the value of a series of function applications,
logic in which the desired result is declared as the answer to a question about a system of facts and rules,
reactive in which the desired result is declared with data streams and the propagation of change

### [Object-Oriented Programming (OOP)](https://developer.mozilla.org/en-US/docs/Glossary/OOP)
- **Object-Oriented Programming** is an approach in programming in which data is encapsulated within objects and the object itself is operated on, rather than its component parts.

### [Imperative programming](https://en.wikipedia.org/wiki/Imperative_programming)
- In computer science, **imperative programming** is a programming paradigm of software that uses statements that change a program's state. In much the same way that the imperative mood in natural languages expresses commands, an imperative program consists of commands for the computer to perform. Imperative programming focuses on describing how a program operates step by step,[1] rather than on high-level descriptions of its expected results.

### [Object-Oriented Programming (OOP)](https://developer.mozilla.org/en-US/docs/Glossary/OOP)
- **Object-Oriented Programming** is an approach in programming in which data is encapsulated within objects and the object itself is operated on, rather than its component parts.

### [Class](https://developer.mozilla.org/en-US/docs/Glossary/Class)
- In object-oriented programming, a **class** defines an object's characteristics. Class is a template definition of an object's properties and methods, the "blueprint" from which other *more specific* instances of the object are drawn.

### [Thread](https://developer.mozilla.org/en-US/docs/Glossary/Thread)
- **Thread** in computer science is the execution of running multiple tasks or programs at the same time. Each unit capable of executing code is called a thread.

### [Main thread](https://developer.mozilla.org/en-US/docs/Glossary/Main_thread)
- The **main thread** is where a browser processes user events and paints. By default, the browser uses a single thread to run all the JavaScript in your page, as well as to perform layout, reflows, and garbage collection. This means that long-running JavaScript functions can block the thread, leading to an unresponsive page and a bad user experience. Unless intentionally using a web worker, such as a service worker, JavaScript runs on the main thread, so it's easy for a script to cause delays in event processing or painting. The less work required of the main thread, the more that thread can respond to user events, paint, and generally be responsive to the user.

### [Dynamic typing](https://developer.mozilla.org/en-US/docs/Glossary/Dynamic_typing)
- **Dynamically-typed languages** are those (like JavaScript) where the interpreter assigns variables a type at runtime based on the variable's value at the time.