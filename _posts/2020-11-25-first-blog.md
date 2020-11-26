---
layout: post
title: "Class vs Functional Components"
description: Explains the differences between Class and Functional React Components
---

**If you have started learning React recently , you would have come across these two terms - Class and Functional Components**, I will try and explain the differences between Class and functional Components and when to use which component in this article.But Let me brief you about the both components first.
<br>

# Functional Components in React

The simplest way to define a component in React is to write a plain JavaScript function with props as an argument, returns a element and export the function

![functional](/assets/img/functional.png)

<center>Functional Component</center>

# Class Components in React

Class Component in React extends a React.Component and render a html element.

![classComponent](/assets/img/classComponent.png)

Both components look similar and gives us the same output but you must be thiniking what is the main difference in both components and when to use functional and class component. Let's see the main differences.

# Differences between functional and class components

# Syntax

You can checkout the above images for syntax reference.

The obvious difference is the syntax. A functional component is just a plain JavaScript function which accepts props as an argument and returns a React element.

A class component requires you to extend from React.Component and create a render function which returns a React element. This requires more code but will also give you some benefits which we will discuss later on.

But the transpiled code from babel looks differenct.

# State

A functional component is just a plain JavaScript function, you cannot use setState() in your component. That’s the reason why they also get called functional stateless components. So everytime you see a functional component you can be sure that this particular component doesn’t have its own state.

If you need a state in your component you will either need to create a class component or you lift the state up to the parent component and pass it down the functional component via props.

**This changed with the React 16.8 Hooks update! You can now use the useState hook to use state in your functional components. You can check out React document for more information how to use useState.**

# Lifecycle Hooks

Another feature which you cannot use in functional components are lifecycle hooks. The reason is the same like for state, all lifecycle hooks are coming from the React.Component which you extend from in class components.
So if you need lifecycle hooks you should probably use a class component.

**This changed with the React 16.8 Hooks update!You can now use the useEffect hook to use lifecycle events in your functional components.You can check out React document for more information how to use useState.**

**why use functional components at all?**

=> Functional component are much easier to read and test because they are plain JavaScript functions without state or lifecycle-hooks.

=> You end up with less code.

=> They help you to use best practices. It will get easier to separate container and presentational components because you need to think more about your component’s state if you don’t have access to setState() in your component.

=> The React team mentioned that there may be a performance boost for functional component in future React versions. You can checkout React Documentation for the reference.
