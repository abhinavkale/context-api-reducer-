# Context-API + Reducer = **Redux**

## Created basic **Todo-App** with context-api, reducer and actions

Reducer is used in very big scale applications, Formally, reducer is the authState object is the state that you want to be passed down to your components and actions object contains all the actions that you would typically use with Redux.

The `useReducer` hook returns a dispatch function just like Redux.
```javaScript
  import { useReducer } from "react";
```

Need to create `action.types.js` file like what actions you what to perform in this application. I used `ADD_TODO` and `REMOVE_TODO` (**Actins should be in Uppercase**)
For eg.  
```javaScript
  export const ADD_TODO = "ADD_TODO";
```

Reducer takes advantage of action.types file and provide method to particular action
For eg.
```javaScript
import { ADD_TODO } from "./action.types";

export default (state, action) => {
  switch (action.type) {
    case ADD_TODO:
      break;
    default:
  }
};
```

Here we normally use `switch` case to handle if there are multiple actions 

action contains **action.type** type of action and **action.payload** like what information you need to carry

## useReducer
```javaScript
  const [state, dispatch] = useReducer(reducer, initialArg, init);
```

`dispatch` method receives an object that represents the action we desire to be done.
```javaScript
  dispatch({
        type: ADD_TODO,
        payload: todo,
  });
```

## Outputs
![Screenshot from 2021-05-13 22-47](https://user-images.githubusercontent.com/56266493/118169998-3a604f00-b447-11eb-9393-7594ff3723f8.png)


![Screenshot from 2021-05-13 22-47](https://user-images.githubusercontent.com/56266493/118170071-5237d300-b447-11eb-9216-6484572120fa.png)


![Screenshot from 2021-05-13 22-48](https://user-images.githubusercontent.com/56266493/118170130-5f54c200-b447-11eb-89f7-5af30c7f5c27.png)






