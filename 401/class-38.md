# Read 37: Redux - Asynchronous Actions

## Review, Research, and Discussion

1. How granular should your reducers be? probably as granular as we make our classes such that each reducer only deals with one main concept.
2. Pro or Con – multiple reducers can “fire” when a commonly named action is dispatched?
Pros: good because then each reducer can control its own limited scope based on the change
Cons: could cause an infinite loop? could cause conflicts because different developers working on different parts of the code might do unexpected things that break other people's code.
3. Name a strategy for preventing the above - make each reducer self contained and does not impact anything except displays? i'm really not sure.

## Vocabulary Terms

* store: an immutable object tree that stores state for the application. there can only be one per app. [src](https://www.tutorialspoint.com/redux/redux_store.htm#:~:text=A%20store%20is%20an%20immutable,need%20to%20specify%20the%20reducer.&text=A%20preloadedState%20is%20an%20optional,initial%20state%20of%20your%20app.)
* combined reducers: a way to make all of the state from reducers available as one so you can access them all as if they were in one object.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
using multiple reducers
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
I'm hoping we get to learn some testing... eventually. I feel very ill-prepared for it
3. What are you most excited about trying to implement or see how it works?
Testing testing testing.... really need to learn some testing :)

## Preparation Materials

* [dan abramov on suspense](https://redux.js.org/advanced/asyncactions)
* [async actions](https://redux.js.org/advanced/asyncactions)
* [thunk middleware](https://github.com/reduxjs/redux-thunk)
* [redux thunk](https://alligator.io/redux/redux-thunk/)
