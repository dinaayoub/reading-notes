# Read 39: Redux - Additional Topics

## Review, Research, and Discussion

1. What’s the best practice for “pre-loading” data into the store (on application start) in a Redux application? Hmm... Not sure, but definitely should do it asynchronously.
2. When using a thunk/async action that dispatches the actual action, which do you export from your reducer? the function that will use thunk via dispatch.

## Vocabulary Terms

* middleware - more generally it's a piece of code that your app executes before whatever thing was requested. In redux, that's thunk to enable async function calls like to APIs
* thunk - a small library that enables async calls in redux

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
Nothing in particular, but now i do have more practice with reducers so they don't seem as crazy.
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
testing.
3. What are you most excited about trying to implement or see how it works?
real tests which adhere to best practices in react. For example, using mock servers.. etc.

## Preparation Materials

* [Redux Toolkit (RTK)](https://redux-toolkit.js.org/)
  * [Tutorial](https://redux-toolkit.js.org/tutorials/intermediate-tutorial)

### Alternative State Managers

* [MobX](https://mobx.js.org/getting-started.html)
* [HookState](https://hookstate.js.org/)
