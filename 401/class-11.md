# Read: Class 11 - Event Driven Applications

## Review, Research, and Discussion

1. Why is access control important? Security - to make sure only people who are authorized can do certain actions.
2. Describe an application that would need access control. A governmental website would need access control to make sure that only people at the appropriate level can modify the contents of the website that constituents are consuming, so some random hacker can't just go in there and change things up.
3. What is a role used for? to specify the capabilities/access level users of that role are granted.
4. Why is role based access control more scalable than discretionary or mandatory access control?

## Vocabulary Terms

1. Authorization: sending credentials to be checked to see whether the user is authorized to proceed. 
2. Role Based Access Control: assigning each user a generic role that specifies what that group of users is allowed to do (e.g. CRUD operations)
3. Capabilities: the types of operations that an acl controls. for example, read could be a capability. delete is another... .etc.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
  - how to implement event listeners in javascript on the server side in node.js
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  - how event listeners are used in the industry, because it seems like it would be hard to keep track of what event triggers which functions if more than one function responds to an event. 
3. What are you most excited about trying to implement or see how it works?
  - stacks and queues being used! 

## Preparation Materials

* [Event Driven Programming](https://www.digitalocean.com/community/tutorials/nodejs-event-driven-programming)
  * logical pattern to confine our programming to avoid complexities and collisions.
  * Example: web browsers. every time the user does something.
  * An Event Handler is a callback function that will be called when an event is triggered.
  * A Main Loop listens for event triggers and calls the associated event handler for that event.
  * EventEmitter native Node.js module for event driven programming. Others: EventEmitter2 and EventEmmitter3 that claim to be faster.
  * Usage:
    ```javascript
    const EventEmitter = require('events').EventEmitter;
    const chatRoomEvents = new EventEmitter;

    function userJoined(username){
        // Assuming we already have a function to alert all users.
        alertAllUsers('User ' + username + ' has joined the chat.');
        chatRoomEvents.on('message', displayMessage);
    }

    // Run the userJoined function when a 'userJoined' event is triggered.
    chatRoomEvents.on('userJoined', userJoined);

    function login(username){
        chatRoomEvents.emit('userJoined', username);
    }
    
    function displayMessage(message){
        document.write(message);
    }    

    chatRoomEvents.removeListener('message', displayMessage); //to remove the displayMessage function from the message event’s list of handlers:
    ```
  * By registering event listeners we can actually reverse the flow of communication between our objects. Rather than on object needing to reach inside another object to trigger a function, our objects can just emit events and whichever objects are listening to those event will process it in the way they have been told to.
    * Example:
    ```javascript
    class Food {
        constructor(name) {
            this.name = name;
        }

        becomeEaten() {
            return 'I have been eaten.';
        }
    }

    var bacon = new Food('bacon');

    class gator {
        eat() {
            bacon.becomeEaten();
        }
    }
    ```
    can turn into:
    ```javascript
    const EventEmitter = require('events').EventEmitter;
    const myGatorEvents = new EventEmitter;

    class Food {
        constructor(name) {
            this.name = name;
            // Become eaten when gator emits 'gatorEat'
            myGatorEvents.on('gatorEat', this.becomeEaten);
        }

        becomeEaten(){
            return 'I have been eaten.';
        }
    }

    var bacon = new Food('bacon');

    const gator = {
        eat() {
            myGatorEvents.emit('gatorEat');
        }
    }
    ```
* [Node docs: events](https://nodejs.org/api/events.html)
  * The EventEmitter calls all listeners synchronously in the order in which they were registered. This ensures the proper sequencing of events and helps avoid race conditions and logic errors. When appropriate, listener functions can switch to an asynchronous mode of operation using the setImmediate() or process.nextTick() methods:
    ```javascript
    const myEmitter = new MyEmitter();
    myEmitter.on('event', (a, b) => {
        setImmediate(() => {
        console.log('this happens asynchronously');
        });
    });
    myEmitter.emit('event', 'a', 'b');
    ```
  * Using the eventEmitter.once() method, it is possible to register a listener that is called at most once for a particular event. Once the event is emitted, the listener is unregistered and then called.
  * As a best practice, listeners should always be added for the 'error' events.
    ```javascript
    const myEmitter = new MyEmitter();
    myEmitter.on('error', (err) => {
        console.error('whoops! there was an error');
    });
    myEmitter.emit('error', new Error('whoops!'));
    // Prints: whoops! there was an error
    ```