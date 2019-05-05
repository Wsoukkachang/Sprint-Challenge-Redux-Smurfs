1.  Name 3 JavaScript Array/Object Methods that do not produce side-effects? Which method do we use to create a new object while extending the properties of another object? 

.map, .filter, and .concat

1.  Describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?

Reducers are functions that take in some state, and a description of what changes took place and return a copy of our state.

Actions in Redux are packets of information that contain an action type and some data that we want associated with that action type. Actions are “dispatched” to our reducer.

The store contains our state for our application. Everything that changes within our application will be represented by a single JavaScript Object known as the store. 

The store known as a 'single source of truth' in a redux application because we never mutate the original object. We simply clone the state object, modify the clone, or replace the original state with the new copy.

1.  What is the difference between Application state and Component state? When would be a good time to use one over the other?

Application state is good for large scale applications or scaling up, where as Component state work better on smaller ones.

Also Component state is stored locally within a component and is not accessible from other components unless it’s explicitly passed as props to it’s sub components. When the number of components increases, the passing of props starts becoming cumbersome.

Where as Application state is a centralized global store which is accessible to any component that subscribes to the store.

1.  What is middleware?

Middleware will intercept every action before it flows through to the Reducers. It lets us do things with the data that we are passing through our action creators to the reducers.

Middleware can stop actions,forward an action untouched, dispatch a different action, dispatch multiple actions.

1.  Describe `redux-thunk`, what does it allow us to do? How does it change our `action-creators`?

Redux Thunk is a middleware created by Dan Abramov, that provides the ability to handle asynchronous operations or API calls inside our Action Creators.

1.  Which `react-redux` method links up our `components` with our `redux store`?

Connect