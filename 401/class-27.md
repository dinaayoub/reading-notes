# Read 27: Props and State

## Review, Research, and Discussion

1. Does a deployed React application require a server? No, it can be a fully client side application like we did today in lab.
2. Why do we prefer to test a React application at the behavior rather than the unit level? because children don't have access to the parents, and it's easier to pass information to the child 'unit' through the parent.
3. What does npm run build do? it compiles the application so you can then deploy it
4. Describe the actual composition / architecture of a React application: the index file places the the root

## Vocabulary Terms

- BDD: behavior-driven development which combines test driven development with the business side to create a common understanding between devs, PMs, and other disciplines [src](https://en.wikipedia.org/wiki/Behavior-driven_development)
- Acceptance Tests: tests that make sure the requirements of a spec document are met [src](https://en.wikipedia.org/wiki/Acceptance_testing)
- mounting: an OS makes files available to users via the computer's file system? seems like you may mean something else here though. [src](<https://en.wikipedia.org/wiki/Mount_(computing)#:~:text=Mounting%20is%20a%20process%20by,via%20the%20computer's%20file%20system.>)
- build: compiles the code

## Preview

1. Which 3 things had you heard about previously and now have better clarity on?
   deploying to github pages
2. Which 3 things are you hoping to learn more about in the upcoming lecture/demo?
   testing api calls, like we do with supertest, but in react.
3. What are you most excited about trying to implement or see how it works?
   connecting a react front end with a backend server.

## Preparation Materials

- [setState explained](https://css-tricks.com/understanding-react-setstate/)

  - only legitimate way to update state after initial setup
  - you can send a function to setState like this:

    ```JSX
    handleIncrement = () => {
    this.setState((prevState) => ({ count: prevState.count + 1 }))
    this.setState((prevState) => ({ count: prevState.count + 1 }))
    this.setState((prevState) => ({ count: prevState.count + 1 }))
    }
    ```

  - Pass a function when you want to update state multiple times
  - Do not depend on this.state immediately after calling setState() and make use of the updater function instead, like this:

    ```JSX
      changeCount = () => {
      this.setState((prevState) => {
        return { count: prevState.count - 1}
      })
    }
    ```

- [handling events](https://facebook.github.io/react/docs/handling-events.html)

  - React event handlers look a little different than regular html ones:

    ```JSX
      <button onclick="activateLasers()">
      //becomes
      <button onClick={activateLasers}>
    ```

  - You can pass in extra parameters like this (either one works):

    ```JSX
    <button onClick={(e) => this.deleteRow(id, e)}>Delete Row</button>
    <button onClick={this.deleteRow.bind(this, id)}>Delete Row</button>
    ```

- [forms](https://facebook.github.io/react/docs/forms.html)

  - forms in react are slightly different - you put the onsubmit on the form then you have access to all the components of the form.

    ```JSX
     <form onSubmit={this.handleSubmit}>
        <label>
          Name:
          <input type="text" value={this.state.value} onChange={this.handleChange} />
        </label>
         <input type="submit" value="Submit" />
      </form>
    ```

- [state and lifecycle](https://facebook.github.io/react/docs/state-and-lifecycle.html)
- [components and props](https://reactjs.org/docs/components-and-props.html)
- [React Testing Library](https://testing-library.com/docs/react-testing-library)
  this seems to be a broken link. Maybe you meant this link? https://github.com/testing-library/jest-dom
- [RTL Testing Example](https://thomlom.dev/beginner-guide-testing-react-apps/)

## Bookmark

- [Roles Reference](https://developer.mozilla.org/en-US/docs/Web/Accessibility/ARIA/ARIA_Techniques#Roles)
