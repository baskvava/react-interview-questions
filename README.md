# react-interview-questions



・Redux
Single data flow problem: data exchange between different "Component" is very difficult

To solve this problem: "Component" only need to send "Action" to subscribe the notification from "Store" 
                        to access data anywhere


Store: Data store in "Store" can make sure projects easier to be maintained and design

Action: Describe "Action type" and "Payload"

e.g
{
  type: INCREMENT,  
  payload: {
    num: 1000
  }  
}

Reducer: Manage and communicate with "Store"

const counter = (state = 0, action) => {
  switch (action.type) {
    case 'INCREMENT':
      return state + action.num;    
    default:
      return state;
  }
}

We may use "combineReuducers" beacuse there many reducers
They have to be combined as a one reducer to interact with "Store"

const calculatorApp = combineReducers({
    counter
});



・Hook

・HOC

・control vs uncontrol state

・render props

・functional components vs class component
