[Table of Contents](README.md)

# Component Composition

## Review, Research and Discussion:

1. Can a parent component access the state of a child component?

    Yes, a parent component can access the state of a child component, but not directly. You can't simply access `child.state` or something like that. Instead, what you can do is have a method in the parent component that is passed to the child component. This method will give the child component the ability to pass state back up to the parent component. 

2. What can be passed along in a prop variable?

    Props can be anything. You can pass object, arrays and even functions. Props are essentially the properties passed into a component when you 'instantiate' that component, to use JS terminology. If a component is a class, when you render that component inside of `App` you are essentially creating a new instance of that class. And as we know from ES6 class, what properties the constructor of the class have are the `props` of the new instance of that class. The same principle applies to React class components.

3. How can a child component “know” the state of another component?

    Since state is something unique to each component, child components can't directly know the state of other components. In fact, a child doen't even know that is might have sibling components. Instead, the way a child can know the state of other components is through props. The parent gives `child1` a method to update the state of the parent. `Child1` does stuff, sends the state to the parent. The parent now does the same thing and sends the new state from `child1` to a new component, `child2`. Since components can't directly access the state of other components, you need to go pass the state up to the parent and then back to another child.

## Vocabulary:

* `Component props` - Props are the properties of a component class that were passed in when the class was rendered, or 'instantiated'.
* `Component state` - An object that contains any information relavent to the component. This is set in the sconstructor of the class component and can be updated within the class and also be sent to the parent or child via accessor methods.
* `Application state` - This is the state of an application as a whole. Unlike component state which is specific to that component, application state is global and can be accessed by any component within the application.

## Preview: 

1. What are some things had you heard about previously and now have better clarity on?

    1. State and accessing state from outside of the component. I knew that state was specific to each component. But I feel like I better understand how to access state from outside each component as also see now that there can be a global state which can be accessed from an component.
    2. Props. This was pretty confusing to wrap my head around at first but once I started to look at it in terms of regular ES6 classes, the "props" are just the properties passed in when "instantiating" a new class component.

2. What are some things are you hoping to learn more about in the upcoming lecture/demo?

    1. Testing! I still haven't dove into testing React yet but I'm interested to see how it is done and if it's different from other testing methods.
    2. Using and accessing global state.

3. What are you most excited about trying to implement or see how it works?

    1. I want to play around more with props and state. I'm interested in seeing more about how state can be passed to other components via callbacks and accessor methods passed in to the props.

## Additional Resources:

* Article: [These are the concepts you should know in React.js (after you learn the basics)](https://www.freecodecamp.org/news/these-are-the-concepts-you-should-know-in-react-js-after-you-learn-the-basics-ee1d2f4b8030/)
* Article: [A quick intro to React’s props.children](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891)
* Documentation: [Composition vs Inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)
* Documentation: [React testing library api example](https://testing-library.com/docs/react-testing-library/example-intro/)