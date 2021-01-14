# Read 29:  Routing

## Review, Research, and Discussion

1. Do child components have direct access to props/state from the parent? No. for props passed in to the child: yes for read access, no for write access which they would have to do through a passed in function that executes in the parent. But they don't have access to their parent's state directly.
2. When a component “wraps” another component, how does the child component’s output get rendered? using the child component's render() function which will get rendered inside the parent component's render() function.

```JSX
<Main>
  <Content />
</Main>
```

3. Can a component, such as <Content />, which is a child also be used as a standalone component elsewhere in the application? Yes, i guess, but it would have to not depend on the props sent to it from its parent.
4. What trick can a parent use to share all props with it’s children? send them in as a prop too? so for example, <Child parentProps = this.props (or this.state/>

## Vocabulary Terms

* props.children: you can use props.children on components that represent ‘generic boxes’ and that ‘don’t know their children ahead of time’. Anything inside the parent tag gets passed as props.children so you can render whatever you want inside the parent container. This is because React encourages using "composition" (children) instead of inheritance [src1](https://codeburst.io/a-quick-intro-to-reacts-props-children-cb3d2fce4891) [src2](https://reactjs.org/docs/composition-vs-inheritance.html)
* composition: a natural pattern of the component model, so we can build components from other components of varying complexity that are reusable in the code. It can reduce component nesting. [src](https://dev.to/bouhm/thinking-in-react-component-composition-fp5#:~:text=In%20React%2C%20composition%20is%20a,in%20building%20many%20other%20components.)

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
props, components (and how they are a way to use composition instead of inheritance)
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
react routers
3. What are you most excited about trying to implement or see how it works?
i'm excited to build an app that really reuses components in multiple places (apart from header and footer) so I can see how this would worl in a real-life situation.

## Preparation Materials

* [browser router tutorial](https://blog.pshrmn.com/entry/simple-react-router-v4-tutorial/)
* [browser router api docs](https://reacttraining.com/react-router/web/api)

## Bookmark

* [react-if component](https://www.npmjs.com/package/react-if)
* [react testing library queries](https://testing-library.com/docs/dom-testing-library/api-queries)
* [aria roles](https://www.w3.org/TR/html-aria/)
