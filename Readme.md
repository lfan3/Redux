# deep learning about Redux

## basic:
Action:  
```
const addTodoAction = {
  type: 'todos/todoAdded',
  payload: 'Buy milk'
}
```
Action pattern: event action(show notif), command action(get_books), comcument action(get megadata)  

Action Creators
```
const addTodo = text => {
  return {
    type: 'todos/todoAdded',
    payload: text
  }
}

const increment = () => {
  return {
    type: 'counter/increment'
  }
}
```
Reducer  
```
const initialState = { value: 0 }

function counterReducer(state = initialState, action) {
  if (action.type === 'counter/increment') {
    return {
      ...state,
      value: state.value + 1
    }
  }
  return state
}
```

Store:   
dispatch(Action) or dispatch(ActionCreator())
```
store.dispatch({ type: 'counter/increment' })
store.dispatch(increment())
store.getState()
```

