# Using redux for centralized state storage 

Creating the store.
* First create store with `createStore(reducers, initialState, enhancers)` from `redux` library.
* Reducers can be combined with combineReducers({value: reducer}).
* Enhancers as of middleWares are applied to all dispatch methods and should be first `applyMiddleware`'ed and then `compose`'ed.

Using reducers to store and manipulate state.
* Reducers are functions that recieve current state and action and returns new state.
* State is a current state of the store and action is the object that has type and payload fields.
* Type field has the type of action and the payload has the payload for the action.

```javascript
export const fooReducer = (state, action) => {

}

```

#react #redux #state
