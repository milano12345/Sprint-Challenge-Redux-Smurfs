1.  Name 3 JavaScript Array/Object Methods that do not produce side-effects? Which method do we use to create a new object while extending the properties of another object?

@ForEach, Map, Concat

1.  Describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

@Reducers specify how the application's state changes in response to actions sent to the store. 
The reducer is a pure function that takes the previous state and an action, and returns the next state.
Given the same arguments, it should calculate the next state and return it. No surprises. No side effects. No API calls. No mutations. Just a calculation.

Actions are payloads of information that send data from your application to your store. 
They are the only source of information for the store. You send them to the store using store.dispatch().

A store holds the whole state tree of your application. The only way to change the state inside it is to dispatch an action on it.
A store is not a class. It's just an object with a few methods on it. To create it, pass your root reducing function to createStore.



1.  What is the difference between Application state and Component state? When would be a good time to use one over the other?

Redux uses what they call "stores" to hold application state. That means any component, anywhere in the app can access it (kind of like a database) so long as they hook into it.
Component state however, lives within that specific component. As such, it can only be updated within that component and passed down to its children via props.


1.  What is middleware?

@Middleware is software that lies between an operating system and the applications running on it.  It’s sometimes called plumbing, as it connects two applications together so data and databases can be easily passed between the “pipe.” Using middleware allows users to perform such requests as submitting forms on a web browser, or allowing the web server to return dynamic web pages based on a user’s profile.

1.  Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?

@Redux Thunk middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. The inner function receives the store methods dispatch and getState as parameters.

1.  Which `react-redux` method links up our `components` with our `redux store`?

Provider is a React component given to us by the “react-redux” library. It serves just one purpose : to “provide” the store to its child components. Now that we have “provided” the redux store to our application, we can now connect our components to it using { connect }.

