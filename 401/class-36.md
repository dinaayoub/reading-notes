# Read 36 - Application State with Redux

## Review, Research, and Discussion

1. What are the advantages of storing tokens in “Cookies” vs “Local Storage”? Cookies can be read by the server while local storage can only be read by the client. you can only store 4KB of data in a cookie which is efficient and small whereas local storage can be up to 5MB. [src](https://medium.com/datadriveninvestor/cookies-vs-local-storage-2f3732c7d977)
2. Explain 3rd party cookies: cookies created by a website other than the one the user is visiting. Usually are used for advertising purposes or to provide services that rely on a 3rd party, such as live chat. [src](https://clearcode.cc/blog/difference-between-first-party-third-party-cookies/#:~:text=Third%2Dparty%20cookies%20are%20those,services%2C%20such%20as%20live%20chats.)
3. How do pixel tags work? They're a small 1x1 pixel graphic that loads the tracking pixel from a server (which runs some code) when the user opens a page, added by the website owner. It is used to track things such as OS, type of website or email, type of client used, client's screen resolution, time visited... etc. Most common use is for advertising and retargetting purposes. [src](https://en.ryte.com/wiki/Tracking_Pixel)

## Vocabulary Terms

* cookies - files that store temporary data in a web browser
* authorization - usually a code of some kind to verify whether a user has permissions to acess something
* access control - a way of assigning roles to users so that different types of users can access different parts of the program through authentication & authorization
* conditional rendering - showing certain parts of your program only to authorized users

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
The difference between cookies and local storage
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
Pixel tags sound really interesting. I'd love to learn more about them.
3. What are you most excited about trying to implement or see how it works?
Redux. Hoping it makes more sense to me than most of React has so far, though I doubt it given how complex Lena describes it as :). 

## Preparation Materials

* [Dan Abramov Redux Tutorials](https://egghead.io/courses/getting-started-with-redux)

## Bookmark

* [worlds easiest guide to redux](https://medium.freecodecamp.org/understanding-redux-the-worlds-easiest-guide-to-beginning-redux-c695f45546f6)
* [testing reducers](https://medium.com/@netxm/testing-redux-reducers-with-jest-6653abbfe3e1)
* [Redux Docs](https://redux.js.org/)