# Readings: Express REST API

## Preparation Materials

* [Review: ES6 Classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
  * can be declared using class expression or class declaration
  * class declaration:

    ``` javascript
    class Food {
        constructor(name,calories) {
            this.name = name;
            this.calories = calories;
        }
    }
    ```

  * class expression:
    * can be unnamed or named
    * named:

      ```javascript
      let FoodItem = class Food {
          constructor(name,calories) {
            this.name = name;
            this.calories = calories;
          }
      }
      ```

    * unnamed:

      ```javascript
      let Food = class {
          constructor(name,calories) {
          this.name = name;
          this.calories = calories;
        }
      }
      ```

  * Class body and method definitions:
    * stricter than usual to maintain performance
    * constructor reserved word to define the class constructor
    * can have getters and setters (e.g. get area() {})
    * static methods and properties can be used without instantiating the class. Can't be used on an instance.
    * using return this in a method returns undefined.
    * "Static (class-side) data properties and prototype data properties must be defined outside of the ClassBody declaration:" --> I didn't understand this one.
    * can use public field declarations before the constructor to make sure those fields are always present and self-documenting. Can be declared with or without a default value. They don't need the "var" or "let" before them this way. Just "height = 0; weight;"
    * to declare private variables, use # at the start. e.g. "#height=0; #weight;"
  * Subclasses with extends
    * can use super() to call the constructor of the class we're extending. Must be called before using "this".
    * If the extending class doesn't have a constructor, super is called by default on its own.
    * "Note that classes cannot extend regular (non-constructible) objects. If you want to inherit from a regular object, you can instead use Object.setPrototypeOf():" ---> don't understand this
  * Symbol.species - can use this to return an object of the type that we're extending. For example:
  * Mix-ins make no sense!

    ```javascript
    class MyArray extends Array {
    // Overwrite species to the parent Array constructor
    static get [Symbol.species]() { return Array; }
    }

    let a = new MyArray(1,2,3);
    let mapped = a.map(x => x * x);

    console.log(mapped instanceof MyArray); // false
    console.log(mapped instanceof Array);  // true
    ```

* [Using Express Routing](https://expressjs.com/en/guide/routing.html)
  - this is mostly basic information about routes and paths and parameters - things we've been already using.
  - new things: response methods:
  - app.route(): create chainable route handlers for a route path. For example app.route('/foo'). get () .post() .put()... etc all chained together. 
  - express router to create modular mountable route handlers (whatever that means)

* [Express Routing](https://scotch.io/tutorials/learn-to-use-the-new-router-in-expressjs-4)
  * here's an example of a basic express router being used:

  ``` javascript
  // server.js
  // we'll create our routes here

  // get an instance of router
  var router = express.Router();

  // home page route (http://localhost:8080)
  router.get('/', function(req, res) {
      res.send('im the home page!');  
  });

  // about page route (http://localhost:8080/about)
  router.get('/about', function(req, res) {
      res.send('im the about page!'); 
  });

  // apply the routes to our application
  app.use('/', router);
  ```

  * route middleware can be run using router.use()
  * route with params looks the same as the app.get equivalent.
  * router.param() creates middleware that will run for a certain route parameter, for example "name" in the /person route, to do validation or whatever else we want. 
  * another example of app.route('/blah', ...) chainging with a.get () .post()... etc

## Questions

1. Name 3 real world use cases where you’d want to change the request with custom middleware
  * to do some logging
  * to validate that the request has some required attribute
  * to add attributes to the request that will be used in other places
2. True or false: The route handler is middleware?
  * false, it's a mini version of express that lets us use middleware?
3. In what ways can a middleware function end the process and send data to the browser?
  * next() which will allow our route to continue on to the next middleware or to the function in the route;
  * throwing an error that stops the request from continuing and sending info back to the user
4. At what point in the request lifecycle can you “inject” middleware?
  * between the request creation on client and its resolution (with a function executed) on the server.
5. What can cause express to error with “Request headers sent twice, cannot start a second response”
  * If you try to send the same response twice. for example, res.send in one function then res.send in another function. I think? Something similar happened to me with error handling when i've already tried to res.send the response then an error happens during that, and i catch the error and try to send the error on the same response. it doesn't work. 

## Document the following Vocabulary Terms

* Middleware: functions that can run on the requests before they hit their final destination on the server. Usually meant to modify the request in some way, or do some logging/error handling... etc.
* Request Object: the object sent from the client to the server over http
* Response Object: the object that the server modifies to send responses to the client.
* Application Middleware: Middleware used with app routes?
* Routing Middleware: Middleware used with express.Router
* Test Driven Development: where you write the test first before you write the code, then write just enough code to get the test working, then you can write your code. Minimizes bugs later on.
* Behavioral Testing

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
  - how to declare and use classes in javascript
  - some of express's route handling
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - I'd like to get to a point where we use classes. Really get into the OOP & learning good engineering practices
  - express router
3. What are you most excited about trying to implement or see how it works?
  - more OOP concepts and implementation.