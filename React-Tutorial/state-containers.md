State Containers
================

A state container (store) is a tool to help you manage the model in the model view intent architecture. The state container:

* holds the model object
* controls changes to the model object
* notifies the view when the model changes

A state container can be implemented with three methods:

* `getState()` returns the current model object
* `dispatch(action)` sends an action (intent) to the store to update the model
* `subscribe(callback)` register a callback to be called when the model changes

Reducer
------

A state container may also have a function called a __reducer__. 

> The reducer processes actions (intents) against the current state, to produce a new state. 

Review the [state container example](https://codepen.io/liammclennan/pen/XPMGJB?editors=0010). 

Redux
-----

Redux is a popular open source state container. It's API is the same as described above (`getState(), dispatch(action), subscribe(callback)`). 

Read the [Redux motivation](https://redux.js.org/introduction/motivation).
Read the [3 principles](https://redux.js.org/introduction/threeprinciples). 

Review the [stopwatch converted to Redux](https://codepen.io/liammclennan/pen/NLpJpv?editors=0010). 

React-redux
-------

Set of helpers for connecting a Redux state container into a React application. 

Read [Usage with React](https://redux.js.org/basics/usagewithreact). 

React-redux allows us to create __connected components__, which are components that have access to the state store to receive data and to publish actions. The function that allows us to *connect* a component is called `connect`. 

```javascript
const ConnectedComponent = connect(mapStateToProps, mapDispatchToProps)(MyComponent);
```

### mapStateToProps

`mapStateToProps` is a function. Its argument is the entire Redux state object. Its result is a props object, to be merged into the components props. This function is where we extract the data that the component needs from the Redux state. 

```javascript
function mapStateToProps(state) {
    return {
        name: state.person.name
    }
}
```

### mapDispatchToProps

`mapDispatchToProps` is also a function. Its argument is the Redux dispatch function.  

```javascript
function mapDispatchToProps(dispatch) {
    return {
        onAppointmentAdded: function () {
            dispatch({
                type: ÁPPOINTMENT_ADDED, appointment
            });
        }
    }
}
```

### Provider

Connected components will only work if they are lower in the react component tree than a `<Provider/>` component. The provider is configured with a redux store and makes that store available to connected components that it contains.  

```html
<Provider store={store}>
    <MyConnectedComponent />
</Provider>
```

Review the [React-Redux stopwatch example](https://codepen.io/liammclennan/pen/xaqeWg?editors=0010).

### Exercise

Return to your solution to the [Official Tutorial](https://reactjs.org/tutorial/tutorial.html). Update it to use Redux and react-redux. Your completed solution should not use any local component state. 























































[Solution](https://codepen.io/liammclennan/pen/eLVrPE)
