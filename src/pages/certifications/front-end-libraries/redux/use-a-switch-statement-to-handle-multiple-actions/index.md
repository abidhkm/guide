---
title: Use a Switch Statement to Handle Multiple Actions
---
## Use a Switch Statement to Handle Multiple Actions

Tip: Make sure you don't use "break" commands after return statements within the switch cases.

### Solution

````javascript
const defaultState = {
  authenticated: false
};

const authReducer = (state = defaultState, action) => {
  // change code below this line
  switch(action.type) {
    case 'LOGIN': return {authenticated:true}
    case 'LOGOUT':return {authenticated:false}
    default: return state
  }
  // change code above this line
};

const store = Redux.createStore(authReducer);

const loginUser = () => {
  return {
    type: 'LOGIN'
  }
};

const logoutUser = () => {
  return {
    type: 'LOGOUT'
  }
};
````
