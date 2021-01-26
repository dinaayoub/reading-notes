# Read 37: Redux - Combined Reducers

## Review, Research, and Discussion

1. Why choose Redux instead of the Context API for global state? you can access the state in any of the components, not only the children of the component
2. What is the purpose of a reducer? take the current state, run some code on it, and return a result.
3. What does an action contain? I'm not sure i understand this question. An action is when you pass some kind of string action to a reducer to tell it what changes to make to the state. We use a switch statement in the reducer to determine which action to take and hence which bits of code to run. 
4. Why do we need to copy the state in a reducer? because the state is immutable (or should be) and we don't want to change the initial state

## Vocabulary Terms

* immutable state: state that can't be changed
* time travel in redux: he Redux DevTools records dispatched actions and the state of the Redux store at every point in time. ... This makes it possible to inspect the state and travel back in time to a previous application state without reloading the page or restarting the app. [src](https://medium.com/the-web-tub/time-travel-in-react-redux-apps-using-the-redux-devtools-5e94eba5e7c0#:~:text=The%20Redux%20DevTools%20records%20dispatched,page%20or%20restarting%20the%20app.)
* action creator: An action creator is merely a function that returns an action object. Redux includes a utility function called bindActionCreators for binding one or more action creators to the store's dispatch() function. [src](https://read.reduxbook.com/markdown/part1/04-action-creators.html#:~:text=Chapter%20recap,the%20store's%20dispatch()%20function.)
* reducer: A reducer is a function that determines changes to an application's state. It uses the action it receives to determine this change. [src](https://css-tricks.com/understanding-how-reducers-are-used-in-redux/#:~:text=A%20reducer%20is%20a%20function,so%20that%20they%20behave%20consistently.)
* dispatch: The Redux store has a method called dispatch. The only way to update the state is to call store.dispatch() and pass in an action object. The store will run its reducer function and save the new state value inside, and we can call getState() to retrieve the updated value [src](https://redux.js.org/tutorials/fundamentals/part-2-concepts-data-flow)

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
how to use redux, i guess. can't say i'm super clear on it yet, though.
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
more about dispatch
3. What are you most excited about trying to implement or see how it works?
using multiple reducers

## Preparation Materials

* [Multiple Reducers Example](https://www.youtube.com/watch?v=gBER4Or86hE)
  * it's recommended to break up your reducers into separate files so that each file can only manage some bits, and you don't end up with one gigantic file
  * never directly mutate the state. you want to return a new object every time.
* [Redux Docs: Using Combined Reducers](https://redux.js.org/recipes/structuring-reducers/using-combinereducers/)
* [Redux Docs: Combined Reducer Syntax](https://redux.js.org/api/combinereducers/)
