# Read 41: React Native

## Review, Research, and Discussion

1. Compare and Contrast Redux Toolkit with Redux “Ducks”. This question didn't make any sense to me. I have tried to search online for something about this but I can't find anything relevent. The closest thing i found was this article describing why ducks might be useful [src](https://medium.com/swlh/the-good-the-bad-of-react-redux-and-why-ducks-might-be-the-solution-1567d5bdc698)
2. What is the principle advantage of Redux Toolkit? it makes it easy to write good redux applications and speeds up development by using best practices recommended by the creators of redux. [src](https://redux.js.org/redux-toolkit/overview#:~:text=Redux%20Toolkit%20is%20our%20official,toolset%20for%20efficient%20Redux%20development.&text=It%20also%20includes%20the%20most,can%20use%20them%20right%20away.)

## Vocabulary Terms

* redux toolkit slices: A createSlice() function that accepts a set of reducer functions, a slice name, and an initial state value, and automatically generates a slice reducer with corresponding action creators and action types. [src](https://redux.js.org/redux-toolkit/overview#:~:text=Redux%20Toolkit%20is%20our%20official,toolset%20for%20efficient%20Redux%20development.&text=It%20also%20includes%20the%20most,can%20use%20them%20right%20away.) 
Here's another source discussing what a slice is:
Right now, the todos code is split into two parts. The reducer logic is in reducers/todos.js, while the action creators are in actions/index.js. In a larger app, we might even see the action type constants in their own file, like constants/todos.js, so they can be reused in both places.

We could replace those using RTK's createReducer and createAction functions. However, the RTK createSlice function allows us to consolidate that logic in one place. It uses createReducer and createAction internally, so in most apps, you won't need to use them yourself - createSlice is all you need. [src](https://redux-toolkit.js.org/tutorials/intermediate-tutorial)

* namespace: a set of names used to identify and refer to objects. a namespace ensures that all of the given set of objects have unique names so they can be easily identified [src](https://en.wikipedia.org/wiki/Namespace)

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
none of these things.
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
expo!
3. What are you most excited about trying to implement or see how it works?
can't wait to make a react native app!

## Preparation Materials

* [getting started with react native](https://facebook.github.io/react-native/docs/getting-started)
* [react native basics (Tutorial)](https://facebook.github.io/react-native/docs/tutorial)

There are some differences between react and react native, look like this:

  * React:

```JSX
// ReactJS Counter Example using Hooks!

import React, { useState } from 'react';



const App = () => {
  const [count, setCount] = useState(0);

  return (
    <div className="container">
      <p>You clicked {count} times</p>
      <button
        onClick={() => setCount(count + 1)}>
        Click me!
      </button>
    </div>
  );
};


// CSS
.container {
  display: flex;
  justify-content: center;
  align-items: center;
}
```

  * React Native:

```JSX
// React Native Counter Example using Hooks!

import React, { useState } from 'react';
import { View, Text, Button, StyleSheet } from 'react-native';

const App = () => {
  const [count, setCount] = useState(0);

  return (
    <View style={styles.container}>
      <Text>You clicked {count} times</Text>
      <Button
        onPress={() => setCount(count + 1)}
        title="Click me!"
      />
    </View>
  );
};

// React Native Styles
const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center'
  }
});
```

* [react native](https://facebook.github.io/react-native/)
* [expo](https://expo.io/)
  * to install:  npm install --global expo-cli
  * to initialize: expo init my-project
* [expo snack](https://snack.expo.io/)
* [ejecting](https://docs.expo.io/versions/latest/expokit/eject)
