# react-interview-questions



# Redux

- Single data flow problem: data exchange between different "Component" is very difficult
- To solve this problem: "Component" only need to send "Action" to subscribe the notification from "Store" 
                        to access data anywhere



## Three major Components
- Store: Data store in "Store" can make sure projects easier to be maintained and design

- Action: Describe "Action type" and "Payload"

```javascript
{
  type: INCREMENT,  
  payload: {
    num: 1000
  }  
}
```

- Reducer: Manage and communicate with "Store"

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
We may use "combineReuducers" beacuse there many reducers
They have to be combined as a one reducer to interact with "Store"

```javascript
const calculatorApp = combineReducers({
    counter
});
```


・Hook

・HOC

・control vs uncontrol state

・render props

# What's the difference between Functional Components and Class Components
If you only need to write a simple function without accessing any "state", it is the time to use Functional Components

- Functional Components: Props transfers into function can be directly render, without processing "state" or doing any "event handlers"


- Class Components: Normal "React Components" life cycle



