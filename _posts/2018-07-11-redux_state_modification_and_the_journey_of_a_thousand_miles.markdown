---
layout: post
title:      "Redux State Modification and the Journey of a Thousand Miles"
date:       2018-07-11 16:41:15 +0000
permalink:  redux_state_modification_and_the_journey_of_a_thousand_miles
---


Redux is a pattern for persisting data in a Javascript object with scope to a store of data, which acts as the 'single source of truth' for an entire application. An improvement on the most common state persistence tool for modern JS before its creation, redux is a portmanteau of 'Flux' and 'reducer', the technologies/concepts that it combines.

This has been one of the more confusing concepts to wrap my brain around, despite seemingly endless resources online, from the coauthor himself and people who have taken the time to really work down and build on certain concepts. The source code is very comprehensible, and yet to understand and implement, there is still a feeling of magic that seems to even out-surprise Rails magic.

Simply enough, Redux creates a single Javascript object that is protected within its own scope, which can't be updated except for by sending actions through a reducer with a payload that updates the object. That's it. There's no real magic, if you watch Dan Abramov's videos in [his course](https://egghead.io/courses/getting-started-with-redux), there's very little to it, it's a concept that extrapolates an idea of how to maintain state within the scope of components. 

Redux is not specifically for use with React, but in order to use it with React, there are some helpful extra node modules, including 'redux' and 'react-redux', which add functionality to create a 'store', the base of the state and the separated 'action' interactivity with the store.

## Built-In Modules/HOCs/Objects

### 'react-redux'

#### Provider

     This is a module that connects Redux to the 'store', the store is the single source of global truth for the application, this object tree that carries all state for the application.
		 
#### connect

     An HOC (Higher Order Component) that connects the exported component to the store, by way of the Provider wrapping the App component. Connect takes in two arguments, the first can specify which state objects should be brought into the current component's props, and the other are the potential dispatch-able action creators. They take as a second series of arguments the actual component itself, so that the export is still available to parent components.

### 'redux'

#### mapStateToProps

     This function takes in state as an argument and then returns which state objects should be drawn from the redux-state and brought into local state. The name is not required to be this, but it is a common/best practice.
		 
#### mapDispatchToProps

     This function takes in 'dispatch' as an argument and brings in exported dispatch action-creators from the reducers, so that they can have a direct connection with events that come from the component. Like mapStateToProps, the name is irrelevant, but it must take in dispatch as an argument.
		 
#### combineReducers

     As reducers are the way that we are able to dispatch action creators in Redux, separating functions by their category is a best practice. For user changes, there should be a users reducer, for other state changes of a similar category, there should be another reducer that works specifically with its like parts -- for this purpose, there is a combineReducers function that takes in all of the available reducers and effectively combines them into a 'root reducer' for accessibility throughout the state, but a separation for the intents and purposes of the developer.

#### applyMiddleware (for 'thunkMiddleware')

     applyMiddleware allows for the use of middleware, which often will take in 'thunk' or 'thunkMiddleware' as an argument. This is the recommended way of extending functionality in redux. It allows you to 'wrap the dispatch method for fun and profit', according to the documentation. It really just allows you to use asynchronous actions and callbacks with your dispatch actions. By using 'thunk', you can attach more than one dispatch to an event and have the functionality be based largely on successful API returns and not time... without which, we've been designing an isolate and fumbly brick.
		 

There is much to learn with Redux, there is a moment when it clicks, and there will always be the difficult applications that make your brain hurt, but understanding the pattern and the way that it works is helpful in creating apps that remove as much local state as possible and allow you to have a much less fumbly and inconsistent application.

