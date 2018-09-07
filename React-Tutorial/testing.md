Testing
=======

Being the part of the application concerned with display and human-computer interaction the user interface is also the least amenable to automated testing. To test a UI you need to try the UI. 

When testing we can *test the behaviour* of an application or *the implementation* of an application. It is easy to test the implementation of a React user interface, that is, test each piece individually and verify that it does what the programmer intended. Note that this doesn't tell us anything about the functionality of the application being correct. 

Read [the redux documentation on testing](https://redux.js.org/recipes/writingtests).

To test the behaviour of a React user interface, that is, to test that the application is functioning correctly, is usually not worthwhile. If you need to then look to full browser automation, but understand that the cost of creating and maintaining those tests is very high.

Testing Implementation of React Apps
----------------------------

### Testing React Components

React components are functions. To test them, you can call them and inspect the results. Recall our `HelloWorld` component:

```jsx
const HelloWorld = (props) =>
  <div>Hello {props.name}</div>;
```

a test could be:

```javascript
it('should render "Hello Fred"', ()=> {
    expect(HelloWorld({name: "Fred"}).props.children).toEqual(['Hello ', 'Fred']);
});
```

to do more advanced inspection use [Enzyme](http://airbnb.io/enzyme/).

Enzyme lets us pretend to render a React component into a browser DOM (using jsdom). Review the [full DOM rendering example](http://airbnb.io/enzyme/#full-dom-rendering). 

### Exercise

Return to your solution to the [Official Tutorial](https://reactjs.org/tutorial/tutorial.html). Add some tests using Enzyme.  