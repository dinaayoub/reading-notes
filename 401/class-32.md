# Read 32 - Custom Hooks

## Review, Research, and Discussion

1. What does a component’s lifecycle refer to? it refers to what state the component is in, for example: componentDidMount or componentWillUnmount [src](https://reactjs.org/docs/state-and-lifecycle.html)
2. Why do you sometimes need to “wrap” functions in useCallback when called from within useEffect? useCallback will help in avoiding regeneration of functions when the functional component re-renders. It should be used when passing the function on to a child component as props and the child component doesn't often need re-rendering except when a certain prop changes, so using useCallback will prevent certain re-renders.  [src](https://stackoverflow.com/questions/57156582/should-i-wrap-all-functions-that-defined-in-component-in-usecallback)
3. Why are functional components preferred over class components? It's easier to read and test, less code. It's also the newer technology and the direction React is going in.
4. What is wrong with the following code? use effect on a constant such as [count] (which isn't changing during the loop) means that use effect would only run once, i think.

```JSX
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

## Vocabulary Terms

* state hook: allows us to use state within a functional component without writing a class
* effect hook: allows us to write code that will run every time we mount, or once, or on every render, for example. It's to replace class methods we no longer have access to such as componentDidMount
* reducer hook: It accepts a reducer function with the application initial state, returns the current application state, then dispatches a function. Here is an example of how it is used: const [state, dispatch] = useReducer(reducer, initialState); This is useful in any situation where having the first loaded state of the application is needed, such as a calculator app when you press "C"  [src](https://css-tricks.com/getting-to-know-the-usereducer-react-hook/#:~:text=useReducer%20is%20one%20of%20a,state%2C%20then%20dispatches%20a%20function.&text=Maybe%20it's%20an%20app%20that,options%20from%20a%20default%20model.)

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
hooks, and how  to use them
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
more of the built in hooks like use reducer
3. What are you most excited about trying to implement or see how it works?
the wrapping mentioned in question 2

## Preparation Materials

### Authoring

* [custom hooks - all you need to know](https://www.telerik.com/blogs/everything-you-need-to-create-a-custom-react-hook)
* [async hooks](https://dev.to/vinodchauhan7/react-hooks-with-async-await-1n9g)
* [useReducer Hook](https://reactjs.org/docs/hooks-reference.html#usereducer)
* [react custom hooks](https://reactjs.org/docs/hooks-custom.html)

### Hooks Lists/Collections

* [use hooks](https://usehooks.com/)
* [hooks list](https://github.com/rehooks/awesome-react-hooks)
* [10 essential react hooks](https://blog.bitsrc.io/10-react-custom-hooks-you-should-have-in-your-toolbox-aa27d3f5564d)
