# Read: 10 - The Call Stack and Debugging

* [The Call Stack defined on MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack)
Basic explanation of what a call stack is, which i'm already familiar with - functions go in one by one and are popped last in first out.
* [Understanding the JavaScript Call Stack](https://www.freecodecamp.org/news/understanding-the-javascript-call-stack-861e41ae61d4/)
The call stack is syncronous, single threaded. LIFO. Stack overflow is caused by putting too many function calls in the stack.
* [JavaScript error messages](https://codeburst.io/javascript-error-messages-debugging-d23f84f0ae7c?gi=4d9a6fb5a24b)
Types of errors:
  * Reference errors: something isn't defined
  * Syntax errors: like missing quotes or so
  * Range errors: like trying to access something that isn't there (like an array index that doesn't exist)
  * Type errors: like trying to access an object property on something that isn't an object
* Debugging:
  * console.log stuff
  * use vs code run the debugger (f5) and add breakpoints
  * look at the stack trace using console.trace() where you want to log it.
  
## Additional Resources

* [JavaScript errors reference on MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Errors)
