# ES6 Overview
- let & const vs var
- Arrow function , implicit return inside one line arrow function
- Callbacks 
- Array and object destructuring 
- object.assign()
- module import/export
- array iteration using for..of
- Default parameters
- method definition short-hand , function word can be ommited when defining inside an object or a class
- key/property shorthand , inside object where the key and value have the same name 
- template literals
- spread syntax
- classes/constructor
- inheritance / super


# REACT
### Get started
1. Create react app : npx create-react-app name
2. work on App.js inside src , you can delete any other things, also you can add JSX
3. Get into work!



### Hello World
- The smallest react example looks like:

        ReactDOM.render(
        <h1>Hello, world!</h1>,
        document.getElementById('root')
        );



### Rendering an Element into the DOM
Let’s say there is a <div> somewhere in your HTML file:

    <div id="root"></div>
We call this a “root” DOM node because everything inside it will be managed by React DOM.

Applications built with just React usually have a single root DOM node. If you are integrating React into an existing app, you may have as many isolated root DOM nodes as you like.

To render a React element into a root DOM node, pass both to ReactDOM.render():

    const element = <h1>Hello, world</h1>;
    ReactDOM.render(element, document.getElementById('root'));  

It displays “Hello, world” on the page.


### Components and Props
- Components let you split the UI into independent, reusable pieces, and think about each piece in isolation. This page provides an introduction to the idea of components. You can find a detailed component API reference here.

Conceptually, components are like JavaScript functions. They accept arbitrary inputs (called “props”) and return React elements describing what should appear on the screen.

Function and Class Components
The simplest way to define a component is to write a JavaScript function:

        function Welcome(props) {
        return <h1>Hello, {props.name}</h1>;
        }

This function is a valid React component because it accepts a single “props” (which stands for properties) object argument with data and returns a React element. We call such components “function components” because they are literally JavaScript functions.

You can also use an ES6 class to define a component:

        class Welcome extends React.Component {
        render() {
            return <h1>Hello, {this.props.name}</h1>;
        }
        }

The above two components are equivalent from React’s point of view.

Function and Class components both have some additional features that we will discuss in the next sections.



# TAILWIND CSS

    <div class="chat-notification">
    <div class="chat-notification-logo-wrapper">
        <img class="chat-notification-logo" src="/img/logo.svg" alt="ChitChat Logo">
    </div>
    <div class="chat-notification-content">
        <h4 class="chat-notification-title">ChitChat</h4>
        <p class="chat-notification-message">You have a new message!</p>
    </div>
    </div>

    <style>
    .chat-notification {
        display: flex;
        max-width: 24rem;
        margin: 0 auto;
        padding: 1.5rem;
        border-radius: 0.5rem;
        background-color: #fff;
        box-shadow: 0 20px 25px -5px rgba(0, 0, 0, 0.1), 0 10px 10px -5px rgba(0, 0, 0, 0.04);
    }
    .chat-notification-logo-wrapper {
        flex-shrink: 0;
    }
    .chat-notification-logo {
        height: 3rem;
        width: 3rem;
    }
    .chat-notification-content {
        margin-left: 1.5rem;
        padding-top: 0.25rem;
    }
    .chat-notification-title {
        color: #1a202c;
        font-size: 1.25rem;
        line-height: 1.25;
    }
    .chat-notification-message {
        color: #718096;
        font-size: 1rem;
        line-height: 1.5;
    }
    </style>

- With Tailwind, you style elements by applying pre-existing classes directly in your HTML.



# Next.Js

- To build a complete web application with React from scratch, there are many important details you need to consider:

Code has to be bundled using a bundler like webpack and transformed using a compiler like Babel.
You need to do production optimizations such as code splitting.
You might want to statically pre-render some pages for performance and SEO. You might also want to use server-side rendering or client-side rendering.
You might have to write some server-side code to connect your React app to your data store.
A framework can solve these problems. But such a framework must have the right level of abstraction — otherwise it won’t be very useful. It also needs to have great "Developer Experience", ensuring you and your team have an amazing experience while writing code.

### Next.js: The React Framework
Enter Next.js, the React Framework. Next.js provides a solution to all of the above problems. But more importantly, it puts you and your team in the pit of success when building React applications.

Next.js has the best-in-class "Developer Experience" and many built-in features; a sample of them are:

. An intuitive page-based routing system (with support for dynamic routes)
Pre-rendering, both static generation (SSG) and server-side rendering (SSR) are supported on a per-page basis
- Automatic code splitting for faster page loads
- Client-side routing with optimized prefetching
- Built-in CSS and Sass support, and support for any CSS-in-JS library
- Development environment with Fast Refresh support
- API routes to build API endpoints with Serverless Functions
Fully extendable
- Next.js is used in tens of thousands of production-facing websites and web applications, including many of the world's largest brands.