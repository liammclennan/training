Model View Intent Architecture
==============================

Model view intent is an architecture for building declarative user interfaces. 

The __Model__ is an object containing all the data required to describe the user interface. 

The __View__ is a function that converts the model into a user interface. 

__Intents__ are things the issue does that should result in a change to the model, which in tern results in a change to the user interface. 

Review the [static model view intent example](https://codepen.io/liammclennan/pen/JvEWQM?editors=0010).

Some rules:

1. The user interface must be generated entirely based upon the model. 
1. If the model changes, the user interface also changes. The model and user interface are guaranteed to be in sync. 
1. The only way the model changes is by processing intents. 

In React parlance, intents are called __actions__. 

Review [complete model view intent example](https://codepen.io/liammclennan/pen/bMgWVG?editors=0010).

