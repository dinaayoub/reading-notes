# Read 34: \<Login /> and \<Auth />

## Review, Research, and Discussion

1. Why is the Context API useful? It acts like a global object, passing data to components without doing it explicitly in each child. So in our metaphor 
2. Can a component outside of a provider get its context? Only if that component is a child of the context provider.
3. What are some common use cases for using the Context API? to keep app-wide state that can be accessed from all children, or to avoid having to use props to cascade state down to all the children of the app.
4. Describe “Context Hell” having mutable global variables can cause conflict between components written by different developers that are relying on the context while some other developer is changing it. [src](https://codethrasher.com/post/2019-08-02-the-path-to-hell/)

## Vocabulary Terms

* global state - the global variables for the entire app
* global context - the context throguh which we can access the global context
* provider - how the context is made available to the component's children
* consumer - the child that is getting data from the provider's context

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
context - i only knew it in an android environment, and thought this would be similar, which it is in some ways, but also not in other ways. So it was good to get clarity on that.
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
I'm looking forward to learning redux
3. What are you most excited about trying to implement or see how it works?
the context functions for today's lab. It would be nice to have the list of to do items globally without having to pass it here and there through props!

## Preparation Materials

* [what is role based access control?](https://digitalguardian.com/blog/what-role-based-access-control-rbac-examples-benefits-and-more)
* [react-cookies component](https://www.npmjs.com/package/react-cookies)
* [react-cookie library](https://www.npmjs.com/package/react-cookie)