[Table of Contents](README.md)

# Custom React Hooks

## Review, Research and Discussion:

1. What does a component’s lifecycle refer to?

    The answer to the review question. 

2. Why do you sometimes need to “wrap” functions in `useCallback` when called from within `useEffect`?

    The answer to the review question.

3. Why are functional components preferred over class components?


    The answer to the review question.

4. What is wrong with the following code?

    The answer to the review question.


Here's an example!
```
import React, {useState, useEffect} from 'react';

function MyComponent(props) {
  const [count, setCount] = useState(0);

  function changeCount(e) {
    setCount(e.target.value);
  }

  let renderedItems = []

  for (let i = 0; i < count; i++) {
    useEffect( () => {
      console.log('component mount/update');
    }, [count]);

    renderedItems.push(<div key={i}>Item</div>);
  }

  return (<div>
     <input type='number' value={count} onChange={changeCount}/>
      {renderedItems}
    </div>);
}
```

## Vocabulary:

* `state hook` -  
* `effect hook` -
* `reducer hook` -

## Preview: 

1. What are some things had you heard about previously and now have better clarity on?

    1. .
    2. .
    3. .

2. What are some things are you hoping to learn more about in the upcoming lecture/demo?

    1. .
    2. .
    3. .

3. What are you most excited about trying to implement or see how it works?

    1. .
    2. .
    3. .

## Additional Resources:

* Article: [The Guide to Learning React Hooks](https://www.telerik.com/kendo-react-ui/react-hooks-guide/#toc-custom-react-hooks)
* Article: [React Hooks with Async-Await](https://dev.to/vinodchauhan7/react-hooks-with-async-await-1n9g)
* Documentation: [Hooks API Reference: useReducer](https://reactjs.org/docs/hooks-reference.html#usereducer)
* Documentation: [Building Your Own Hooks](https://reactjs.org/docs/hooks-custom.html)

### 3rd Party React Hook Collections:
* [useHooks.com](https://usehooks.com/)
* [rehooks/awesome-react-hooks](https://github.com/rehooks/awesome-react-hooks)
* [10 React Hooks you Should Have in Your Toolbox](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d)