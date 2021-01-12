# Read 26: Component Based UI

## Review, Research, and Discussion

1. Name 5 Javascript UI Frameworks (other than React): Angular, jquery, bootstrap, Vue
2. What’s the difference between a framework and a library? A framework is a group of libraries we use to create our program within its structure, A library is a piece of code that we use as a tool to accomplish something.

## Vocabulary Terms

Rendering: create a visual representation [src](https://www.quora.com/What-does-rendering-mean-in-computer-science-and-why-is-this-word-used-to-describe-what-it-means)
Templates: a blueprint or formula - that serves as a starting point for a new item/document. [src](https://www.google.com/search?sxsrf=ALeKk00EEg2IwaXMAeQMaNCSv0yZBByasQ%3A1610419764666&ei=NA79X_yLKKnP0PEPoraxoAg&q=define+template+computer+science&oq=define+template+computer+science&gs_lcp=CgZwc3ktYWIQAzoECAAQRzoECAAQDToGCAAQBxAeOgYIABANEB46CggAEAgQDRAKEB5QhxJYth5g4B9oAHADeACAAWiIAbcFkgEDOC4xmAEAoAEBqgEHZ3dzLXdpesgBCMABAQ&sclient=psy-ab&ved=0ahUKEwj89YuQsZXuAhWpJzQIHSJbDIQQ4dUDCA0&uact=5)
State

## Preview

* Which 3 things had you heard about previously and now have better clarity on?
  1. React
* Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
  1. More about SCSS
* What are you most excited about trying to implement or see how it works?
  1. Getting React working with a backend

## Preparation Materials

* [react hello world](https://facebook.github.io/react/docs/hello-world.html)
Smallest react example looks like this:

``` JSX
ReactDOM.render(
  <h1>Hello, world!</h1>,
  document.getElementById('root')
);
```

* [introducing JSX](https://facebook.github.io/react/docs/introducing-jsx.html)
  * Tag syntax that looks something like this:

    ``` JSX
    const element = <h1>Hello, world!</h1>;
    ```

  * instead of separating technologies by putting markup and logic in separate files, we can separate concerns with loosely coupled components that contain both. 
  * JSX is an expression too (regular JS function) after compilation.
  * Prevents injection attacks so it's safe to embed user input

* [rendering elements](https://facebook.github.io/react/docs/rendering-elements.html)
  * the smallest building block of a React app
  * to render something in an html div somewhere, you pass both the react element and the root DOM, like this:

  ```JSX
    const element = <h1>Hello, world</h1>;
    ReactDOM.render(element, document.getElementById('root'));
  ```

  * React elements are immutable and can't be changed, so the only way to update an item is to re-render it completely.
  * React only updates what's necessary - compares previous with new desired DOM state and updates only what's changed

## Bookmark

* [sass cheatsheet](https://devhints.io/sass)
* [react cheatsheet](https://devhints.io/react)
* [another react cheatsheet](https://reactcheatsheet.com/)
