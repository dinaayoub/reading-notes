# Read: 09 - Refactoring

* [Functional Programming Concepts](https://medium.com/the-renaissance-developer/concepts-of-functional-programming-in-javascript-6bc84220d2aa)

  * Pure functions:
    * deterministic - a.k.a referentially transparent. Will always return the same result for the same input
    * discourages mutability, encourages immutability (unable to change or doesn't change over time)
    * have no observable side effects (e.g. changing a global object or a parameter passed by reference)
    * Doesn't use global variables, just the ones you pass in
    * Can't be pure if it read files because the file contents can change
    * Can't use a random number generator
  * Memoization is an optimization technique by storing the results of expensive function calls and returning the cahced result when the same inputs occur again.
  * Functions as first-class entities: treat functions like values and pass them like data. Example:

    ``` javascript
    const sum = (a, b) => a + b;
    const subtraction = (a, b) => a - b;

    const doubleOperator = (f, a, b) => f(a, b) * 2;

    doubleOperator(sum, 3, 1); // 8
    doubleOperator(subtraction, 3, 1); // 4
    ```

  * Higher order functions: take one or more functions as arguments or returns a function as a result
  * Filter is a higher order function as it returns a new array (doesn't modify the old one)
  * Declarative(using higher order functions such as filter) vs Imperative approach (regular loop pushing results into new array)
  * Map transforms a collection by applying a function to all of its elements and building a new collection from the returned values
  * Reduce receives a function and a collection, and returns a value created by combining the items (had trouble understanding this one).

* [Refactoring Javascript for Readability](https://dev.to/healeycodes/refactoring-javascript-for-performance-and-readability-with-examples-1hec)
  * Strategies for easier to read code:
    * Return early from functions
    * Cache variables so functions can be read like sentences
    * Check for Web APIs before implementing your own functionality
