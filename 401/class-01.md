# Read: Class 01 - Node Ecosystem, TDD, CI/CD

## Array.map()

Array.map() creates a new array based on some criteria that we set and send in to the .map as a function. It basically iterates over every item in the array and runs the function we give it, returning the result of that function into the new array. So for example, if I say array.map((arrayItem) => {
    return arrayItem%2;
}) then I'm creating a new array with 1 for odd numbers and 0 for even numbers from the original array.

## Array.reduce()

Array.reduce runs the function you give it on each element of the array to create one single accumulated value. So for example, if we want to get the multiplication of all items in an array, we can:
array.reduce((accumulator,currentValue) => {
    return accumulator * currentValue;
},1);
the ,1 at the end specifies what value of accumulator we want to start with (and is optional).

Source: [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

## code snippets of how to use superagent()

### With normal Promise .then() syntax

superagent.get('https://pokeapi.co/api/v2/')
          .then(data => {
              //do something with the data here
          })
          .catch(error => {
              //do something with the error here
          });

### With async / await syntax

## Promises

## Are all callback functions considered to be Asynchronous? Why or why not?
