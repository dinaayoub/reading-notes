# Read: Class 01 - Node Ecosystem, TDD, CI/CD

## Array.map()

Array.map() creates a new array based on some criteria that we set and send in to the .map as a function. It basically iterates over every item in the array and runs the function we give it, returning the result of that function into the new array. So for example, if I say:

```javascript
array.map((arrayItem) => {
    return arrayItem%2;
});
```

then I'm creating a new array with 1 for odd numbers and 0 for even numbers from the original array.

## Array.reduce()

Array.reduce runs the function you give it on each element of the array to create one single accumulated value. So for example, if we want to get the multiplication of all items in an array, we can:

```javascript
array.reduce((accumulator,currentValue) => {
    return accumulator * currentValue;
},1);
```

the parameter 1 at the end specifies what value of accumulator we want to start with (and is optional).

Reference: [MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Reduce)

## code snippets of how to use superagent()

### With normal Promise .then() syntax

```javascript
superagent.get('https://pokeapi.co/api/v2/')
    .then(data => {
        //do something with the data here
    })
    .catch(error => {
        //do something with the error here
    });
```

### With async / await syntax

```javascript
async function getData() {
    try {
        let data = await superagent.get('https://pokeapi.co/api/v2/');
        //handle data here
        console.log(data);
    }
    catch (error) {
        console.error(error);
    }
}
```

Reference: [superagent docs](https://www.npmjs.com/package/superagent)

## Promises

A promise is like saying "i promise you something, but i don;t know what it is right now. It might succeed (resolve) or fail (reject), and then (.then()) you can deal with what i've returned to you.  So it's an object that has both the code to determine whether the promise succeeded or failed (resolve, reject), and is .thenable so that you can synchronously wait for its return and do something with the returned data, or catch errors when it is rejected.

References:
[MDN web docs](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Promise)
[W3 Schools](https://www.w3schools.com/js/js_promise.asp)
[Medium: Master the JavaScript Interview: What is a Promise?](https://medium.com/javascript-scene/master-the-javascript-interview-what-is-a-promise-27fc71e77261)

## Are all callback functions considered to be Asynchronous? Why or why not?

No, taking a callback doesn't mean a function has to be asyncrhonous. if that were the case, then functions like array.forEach or .map() or .reduce() ... etc would not work because it would just move on before any of the work happens, and leave you with a 0 result. It's only asynchronous callback if the function performs an asynchonous operation, such as superagent.get().
