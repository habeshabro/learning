```jsx
const store = Redux.createStore(
  (state = {login: false}) => state
);
const loginAction = () => {
  return {
    type: 'LOGIN'
  }
};
const ret = store.getState();
store.dispatch(loginAction())
```

actions are dispatched, reducers handle it. They take state and action as arguments.

```jsx
const authReducer = (state = defaultState, action) => {
	  switch(action.type){
    case 'LOGIN':
      return {authenticated: true};
    case 'LOGOUT':
      return {authenticated: false};  
    default:
      return state
  }
};
```
you can also subscribe and "listen" to the store to execute actions when an action is dispatched

```jsx
store.subscribe(() => count++)
```

combining reducers

```js
const rootReducer = Redux.combineReducers({
  auth: authenticationReducer,
  notes: notesReducer
});
```

for async functions

```js
const requestingData = () => { return {type: REQUESTING_DATA} }
const receivedData = (data) => { return {type: RECEIVED_DATA, users: data.users} }
const handleAsync = () => {
  return function(dispatch) {
    // Dispatch request action here
    dispatch(requestingData())
    setTimeout(function() {
      let data = {
        users: ['Jeff', 'William', 'Alice']
      }
      // Dispatch received data action here
      dispatch(receivedData(data))
    }, 2500);
  }
};

const store = Redux.createStore(
  asyncDataReducer,
  Redux.applyMiddleware(ReduxThunk.default)
);
```