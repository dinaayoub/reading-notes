# Readings: Express

## Preparation Materials
* [An introduction to NodeJS and Express](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)
  * Node is an open source runtime environment that allows running JavaScript code on the server side outside of a browser. It has a few advantages:
    * Great performance.
    * Less context switching between languages for front end and back end development.
    * benefits from improvements made to javascript which is a newer language.
    * has npm which provides us access to hundreds of thousands libraries/packages.
    * Portable, works on so many different platforms.
  * Express is the most popular node web framework and library that many other web frameworks rely on. It is unopinionated which means it doesn't have an opinion on how best to handle anyu particular task, so it's more flexible with fewer restrictions on how to use components together. It allows us to:
    * handle web requests with different paths and different verbs.
    * set common web app settings such as port, file locations of templates.
    * add middleware to run within the request handling pipeline.

* [What is NPM?](https://docs.npmjs.com/about-npm)
  * NPM is a software registry where open source developers can share and borrow packages. It consists of the website, the CLI and the registry. We mostly use the CLI to install packages, but we could also use the website to create our own organization so we can create packages and share them with the world.

* [What is Test Driven Development (TDD)?](https://www.agilealliance.org/glossary/tdd/#q=~(infinite~false~filters~(postType~(~'page~'post~'aa_book~'aa_event_session~'aa_experience_report~'aa_glossary~'aa_research_paper~'aa_video)~tags~(~'tdd))~searchTerm~'~sort~false~sortDirection~'asc~page~1))
  * The basic idea is that you write the test before you write the code
  * signs of  use:
    * code coverage. Less than 80% shows poor use.
    * version control. Should show that every time product code is checked in, test code must also be checked in for it.
  * Beginners can write the test code before the product code and get it working sufficiently for the test to pass.
  * Intermediate TDD can:
    * creates a test that fails when a bug is found so that when bug is fixed that test would succeed
    * come up with several unit tests to be written for a feature
    * can name tactics to guide writing tests (like best practices almost for that type of test)
    * can factor out reusable elements from existing unit tests so they can be reused in other places.
  * Advanced TDD:
    * create a roadmap of planned tests for a bunch of larger features
    * able to test drive a variety of design paradigms (object oriented, functional, event-driven) ----> I don't understand this one.
    * able to test drive a variety of technical domains: computation, user interfaces, persistent data access ---> not sure I get this one either.

* [CI/CD](https://www.youtube.com/watch?v=xSv_m3KhUO8&ab_channel=GitHubTraining%26Guides)
* CI is a strategy to ensure everyone's changes integrate, catch bugs, and reduce merge conflicts. Goes with automated testing, so every time code is added, the tests will automatically run.A CI server can make sure changes work and communicate those changes to webhooks and APIs.
* Continuous Delivery vs Continuous deployment
  * Delivery: develop code that you could release at any time. Coupled with CI, lets you develop code in more manageable increments.
  * Deployment: extension of CD. allows you to deploy newly developed features into production immediately with confidence (they've all run through CI)
* Webhooks: when the ci server finishes building and running the tests, it can notify people, shows up in github with status, and you can configure it to also automaticaly deploy to get Continuous Deployment.

## Bookmark
[nodeJS docs](https://nodejs.org/en/docs/)
[npm docs](https://docs.npmjs.com/)
[express docs](https://expressjs.com/en/4x/api.html)
[http status codes](https://www.restapitutorial.com/httpstatuscodes.html)
[supertest](https://github.com/visionmedia/supertest)

## Questions

1- What’s the difference between PUT and PATCH?
2- Provide links to 3 services or tools that allow you to “mock” an API for development like json-server
3- Compare and contrast Swagger and APIDoc.js
4- Which HTTP status codes should be sent with each type of (un)successful API call?
5- Compare and contrast SOAP and ReST

## Document the following Vocabulary Terms

* Web Server: a computer that listens for requests, processes them and sends responses, while storing files or databases [src](https://developer.mozilla.org/en-US/docs/Learn/Common_questions/What_is_a_web_server)
* Express: a node web framework and library used by many other node web frameworks [src](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs/Introduction)
* Routing: I think this is about writing routes in node js, which have a verb (such as get, post) and a location route such as /data.
* WRRC: Web request response cycle

## Preview

* Which 3 things had you heard about previously and now have better clarity on?
  1- What express is. I knew it was a library for node.js but i didn't know it is also a "node web framework"
  2- heard of test driven development before
  3- how to create your own npm package to share with the world
* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  1- how to write unit tests
  2- the answer to the questions i have about intermediate and advanced TDD skills
  3- The answers to the questions section about put and patch... etc as that wasn't in the readings. I will update my entry here with answers later.
* What are you most excited about trying to implement or see how it works?
  1- unit tests!
  2- using SOAP
