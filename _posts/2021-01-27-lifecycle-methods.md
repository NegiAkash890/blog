---
title:  "Lifecycle Methods"
layout: post
categories: react
---

Let gets started with react lifecycle methods



## Lifecycle Methods
Each component in react has a lifecycle.<br/>
We can either monitor or manipulate it during :
- Mouting
- Updating
- Unmounting

What is mouting ?

Putting elements into the DOM (Document Object Model)
There are 4 methods that get called in this order when mouting a component:

```bash
1. constructor()
2. getDerivedStateFromProps()
3. render()
4. componentDidMount()
```
Note : render() method is the only required methods rest are optional

### constructor(props)

- This is called before anything else
- Used as : Natural place to intialise state
- It's called with props as argument

Before doing anything in constructor call [super(props)](https://overreacted.io/why-do-we-write-super-props/).
Why ? So we can inherit parent methods from React.Component.

### getDerivedStateFromProps

- This method is called right before rendering the element(s) in the DOM.
- Used as : Natural place to set the state based on the intial props.
- Why we need : It enables a component to update its internal state as a result of change in props
- This lifecycle is called any time a parent component rerenders, regardless of whether the props are “different” from before

### render

- This is required
- Usage: Output HTML to DOM

### componentDidMount

- Called after the component is rendered
- Used as : Place to call APIs
