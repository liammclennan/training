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