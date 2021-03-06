# react-interview-questions



# Redux

- Single data flow problem
    - data exchange between different "Component" is very difficult
- To solve this problem
    - "Component" only need to send "Action" to subscribe the notification from "Store" 
                        to access data anywhere


## Three major Components
- Store
    - Data store in "Store" can make sure projects easier to be maintained and design

- Action 
    - Describe "Action type" and "Payload"

```javascript
{
  type: INCREMENT,  
  payload: {
    num: 1000
  }  
}
```

- Reducer
    - Manage and communicate with "Store"

```javascript
const counter = (state = 0, action) => {
  switch (action.type) {
    case 'INCREMENT':
      return state + action.num;    
    default:
      return state;
  }
}
```


- Why use combineReducers?
    - We may use "combineReuducers" beacuse there many reducers
    - They have to be combined as a one reducer to interact with "Store"

```javascript
const calculatorApp = combineReducers({
    counter
});
```

- Redux.sega


## Hooks
- Why using Hooks?
  - Without any function can be resued on component, withouy using hooks, we try to use "HOC" or "Render Props" to solve reuse problems
  - Add many unrelated functions into life cycles, such as adding "call API" or "Business Logic functinos" into "ComponentDidmount"
- useState
- useEffect
- useMemo
    
## HOC

## control vs uncontrol state

## render props

# What's the difference between Functional Components and Class Components
If you only need to write a simple function without accessing any "state", it is the time to use Functional Components

- Function Component (just like a javascript function) : Stateless
  - Props transfers into function can be directly render
  - without processing "state" or doing any "event handlers"
  - it accepts a "props" objects and returns a "React element"

```javascript
function HelloVava(props) {
  return <h1>Hello, {props.name} </h1>;
}
```

- Class Component: Stateful
  - Manipulate normal "React Components" life cycle
  - Can manipulat "state" 
  
```javascript
class HelloVava extends React.Components {
  render() {
    return <h1> Hello, {this.props.name} </h1>
  }
}
```

# Provider

# await

# axios
 - XMLHttpRequests
 - node.js send http request
 - automatically transfer JSON data
 
# redux-thunk vs redux-saga

 - redux-thunk : hard to test ....
 - Basic Thunk 
```javascript
const increaseAsync = () => dispatch => {
    setTimeout(() => {
        dispatch(increment());
    }, 1000)
} 
```
 - Advanced Thunk 
 ```javascript
 const fetchBalence = () => fetch('https://www.xxxxxxx.api')
 const transferMoney = () => dispatch => (
    fetchBalance().then(() => 
        Promise.all([
            dispatch(checkA(true)),
            dispatch(checkB(true))
        ])
    ).then(() =>
        dispatch(notifyA())
    ).then(() =>
        dispatch(moveSomthing())
    )
 )  
 ```
 - redux-saga: easily to test, easily to read and write, can be written as scripts
 
 
# Virtual DOM vs Real DOM ？

# Performance Tools **** Cool

