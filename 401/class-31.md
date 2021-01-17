# Read 31: Hooks API

## Review, Research, and Discussion

1. Why do we not need more .html pages in a multi-page React app?
2. If we wanted a component to show up on every page, where would we put it and why?
  Outside the <BrowserRouter/>
  Inside the <BrowserRouter />, outside a <Route />
  Inside a <Route />
3. What does props.children contain?

## Vocabulary Terms

* Composition: a way to build complex functionality by combining smaller components [src](https://flaviocopes.com/react-composition/)
* Children / Child Components: the components placed in the outer (parent) container. For example, if we have App which includes header, main and footer components, then App is the parent and header, main and footer are the child components
* Hash Routing: using the anchor part of the URL to simulate different content. For example <http://site.com/#/products/list> leads to displaying a list of products, which all happens on the client side. [src](https://krasimirtsonev.com/blog/article/deep-dive-into-client-side-routing-navigo-pushstate-hash#:~:text=Hash%2Dbased%20routing,never%20sent%20to%20the%20server.)
* Link Routing: using a path in the URL to simulate different content. For example, <http://blah.com/products/lists> could lead to displaying products but it happens only on the client side as we are still on the same React page (say, App), but we should a different "link" in the browser.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
  hash tables. I thought there would be more complex or standardized algorithms for hashing but I guess not?
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  hooks! it seems like they might fix an issue i'm having in the lab.
3. What are you most excited about trying to implement or see how it works?
  hooks :) also maybe some real world uses for hash tables.

## Preparation Materials

1. [making sense of hooks](https://medium.com/@dan_abramov/making-sense-of-react-hooks-fdbde8803889)

* hooks let us organize the logic inside a component into reusable isolated units by applying the react philosophy of explicit data flow and composition inside a component rather than just between the components, without introducing unnecessary nesting.
* Hooks let you use React features (like state) from a function — by doing a single function call. React provides a few built-in Hooks exposing the “building blocks” of React: state, lifecycle, and context.
* can combine built in hooks with your own custom hooks
* Hooks are fully encapsulated — each time you call a Hook, it gets isolated local state within the currently executing component
* built in hooks documentation: <https://reactjs.org/docs/hooks-overview.html>
* Can replace classes with them but classes will still be supported
* here's an example:

```JSX
function MyResponsiveComponent() {
  const width = useWindowWidth(); // Our custom Hook
  return (
    <p>Window width is {width}</p>
  );
}

//in another file
function useWindowWidth() {
  const [width, setWidth] = useState(window.innerWidth);
  
  useEffect(() => {
    const handleResize = () => setWidth(window.innerWidth);
    window.addEventListener('resize', handleResize);
    return () => {
      window.removeEventListener('resize', handleResize);
    };
  });
  
  return width;
}
```

2. [the state hook](https://reactjs.org/docs/hooks-state.html)

* HOOK example:

```JSX
import React, { useState } from 'react';

function Example() {
  // Declare a new state variable, which we'll call "count"
  const [count, setCount] = useState(0);

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

* CLASS example:

```JSX
class Example extends React.Component {
  constructor(props) {
    super(props);
    this.state = {
      count: 0
    };
  }

  render() {
    return (
      <div>
        <p>You clicked {this.state.count} times</p>
        <button onClick={() => this.setState({ count: this.state.count + 1 })}>
          Click me
        </button>
      </div>
    );
  }
}
```

* regular functions are stateless components
* function components are the new thing where we have access to state
* hooks don't work inside classes but can be used instead of writing classes
* we use square brackets when dealing with useState because this:

```JSX
  const [fruit, setFruit] = useState('banana');
```

is the equivalent of this:

```JSX
  var fruitStateVariable = useState('banana'); // Returns a pair
  var fruit = fruitStateVariable[0]; // First item in a pair
  var setFruit = fruitStateVariable[1]; // Second item in a pair
```

* to use multiple state variables, we do this:

```JSX
function ExampleWithManyStates() {
  // Declare multiple state variables!
  const [age, setAge] = useState(42);
  const [fruit, setFruit] = useState('banana');
  const [todos, setTodos] = useState([{ text: 'Learn Hooks' }]);
```

* In the above component, we have age, fruit, and todos as local variables, and we can update them individually, for example:

```JSX
function handleOrangeClick() {
    // Similar to this.setState({ fruit: 'orange' })
    setFruit('orange');
  }
```

3. [hooks api](https://reactjs.org/docs/hooks-overview.html)
4. [hooks api reference](https://reactjs.org/docs/hooks-reference.html)
5. [effects hook](https://reactjs.org/docs/hooks-effect.html)
