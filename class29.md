[Table of Contents](README.md)

# React Routing

## Review, Research and Discussion:

1. Do child components have direct access to props/state from the parent?

    Child components do not have direct access to the props or state of the parent component. In order for the child component to read or update the state of the parent, the child either needs to be passed a method for accessing the state from the parent or have the parent's state passed in as props to the child. The former will allow the child to update the state of the parent component. The latter will just give the child component read access. 

2. When a component “wraps” another component, how does the child component’s output get rendered?

    When a component is wrapped in another component, the children of the component getting wrapped are rendered in the wrapper.

3. Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application?

    All components in React can be considered standalone components. Thus, any child component that was created and rendered in a parent component can also be imported and used elsewhere. The only consideration would need to be if the child component has props from the parent required to make it work. But ideally, all components should be created in such a way that they can be reused anywhere in an application that makes sense.

4. What trick can a parent use to share all props with it’s children

    Inside of the render of the parent component, you can simply send props.children to the child component. Props.children are whatever is inside the JSX tags when rendering out a component.

## Vocabulary:

* `props.children` - these are used to display whatever is put inside if the opening/closing tags of a component when rendering it.
* `composition` - the practice of building components from other components.

## Preview: 

1. What are some things had you heard about previously and now have better clarity on?

    1. Using `this.props.children`. I've seen it referenced and used in lots of tutorials and examples, and now I am finally starting to grasp what it is and how it's used.
    2. ReactRouter and how it is used to help with browser routing in a single page application.

2. What are some things are you hoping to learn more about in the upcoming lecture/demo?

    1. I'd like to learn more about using the ReactRouter.
    2. Learnign more about and how to better use `props.children`.

3. What are you most excited about trying to implement or see how it works?

    1. ReactRouter!

## Additional Resources:

* Documentation: [React Router](https://reactrouter.com/web/api)
* Documentation: [React-If](https://www.npmjs.com/package/react-if)
* Documentation: [React Testing Library: Queries](https://testing-library.com/docs/dom-testing-library/api-queries/)
* Documentation: [ARIA in HTML](https://www.w3.org/TR/html-aria/)
<!-- * Article: []() -->

