# Readings: Data Modeling

## Questions

1. Name 3 advantages to Test Driven Development
    1. fewer bugs in the later stages of development so it saves you time
    2. easier maintenance of the code
    3. allows you to deploy more regularly confidently if you've got good coverage.
2. In what case would you need to use beforeEach() or afterEach() in a test suite?
when using console spy to do a mock implementation
3. What is one downside of Test Driven Development
larger up front development cost as it takes more time to do it this way initially
4. What’s the primary difference between ES6 Classes and Constructor/Prototype Classes?
ES6 classes allow inheritance using "extends"? not sure.
5. Why REST?
good question. based on class today it's not very clear yet, but seems to be because it allows us to use very standard CRUD verbs.

## Vocabulary

* functional programming - programming that goes somewhat linearly by applying functions.
* object-oriented programming (OOP) - programming that utilizes classes, inheritance, methods... etc to model the world after "objects" that have verbs for us to use.
* class - something we create an object of - a model.
* super - the class that this one extends. we use it to call the class this one is based on's constructor, for example.
* this - the current object in which this operation is happening
* Test Driven Development (TDD) - again? development that starts with writing the test before writing the code, write enough code to make the test pass, then continue on.
* Jest - a module that allows us to run tests to do CI
* Continuous Integration (CI) - a strategy that allows us to run tests every time there's a code check in, it enables continuous deployment as well.
* REST - representational state transfer - allows us a set of verbs to perform CRUD operations over http.
* Data Model - the base properties and methods for an object we will want to use. in a way sort of the template of an object.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
    1. what nosql means.
    2. how to use mongodb.
    3. what mongoose is and how it helps us.
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
    1. more examples of mongodb usefulness
3. What are you most excited about trying to implement or see how it works?
    1. excited to get my first mongodb up and running in the cloud, and not just locally!

## Preparation Materials

* [sql vs nosql (Video)](https://www.youtube.com/watch?v=ZS_kXvOeQ5Y)
* [nosql vs sql](https://www.thegeekstuff.com/2014/01/sql-vs-nosql-db/?utm_source=tuicool)
* [nosql modeling techniques](https://highlyscalable.wordpress.com/2012/03/01/nosql-data-modeling-techniques/)

## Bookmark

* [mongoose api](https://mongoosejs.com/docs/api.html#Model)