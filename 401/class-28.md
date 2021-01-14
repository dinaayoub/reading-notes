# Read 28: Component Composition

## Review, Research, and Discussion

1. Can a parent component access the state of a child component? Yes, but i'm not sure how apart from the child component sending it back using a function.
2. What can be passed along in a prop variable? variables (of any data type, including array and objects), and also functions
3. How can a child component “know” the state of another component? only through the state passed to it in props from its parent. So if it has a sibling the parent must be the hub of communication from one child to the other.

## Vocabulary Terms

* component props: properties sent by the parent component to the child component
* component state: this.state of the component which can hold state across requests
* application state: this.state of the application? not sure.

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?

2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
this cors error that i keep getting that is stopping my put and post from working despite much research online and using a "proxy":
Access to fetch at 'https://cors-anywhere.herokuapp.com/https://dina-basic-api-server.herokuapp.com/artists' from origin 'http://localhost:3000' has been blocked by CORS policy: No 'Access-Control-Allow-Origin' header is present on the requested resource. If an opaque response serves your needs, set the request's mode to 'no-cors' to fetch the resource with CORS disabled.
3. What are you most excited about trying to implement or see how it works?
loading spinny and testing APIs

## Preparation Materials

* [react basics recap](https://medium.freecodecamp.org/these-are-the-concepts-you-should-know-in-react-js-after-you-learn-the-basics-ee1d2f4b8030)
* [props.children](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891)
* [composition vs inheritance](https://reactjs.org/docs/composition-vs-inheritance.html)
* [react testing library api example](https://testing-library.com/docs/react-testing-library/example-intro)

## Bookmark

* [react-if component](https://www.npmjs.com/package/react-if)
* [react-testing-library-async](https://testing-library.com/docs/dom-testing-library/api-async)
