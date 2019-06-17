# Reducer
- Reducers specify `how the application's state changes in response to actions sent to the store. `
- Remember that actions `only describe what happened`, but `don't describe how the application's state changes`.
# Designing the State Shape
- try to keep the data separate from the UI state.
- Think of the app's state `as a database`
# Handling Actions 
- we've decided what our state object looks like
- `The reducer is a pure function that takes the previous state and an action, and returns the next state`
- `(previousState, action) => newState`
## Why call it reducer? Because it's the type a function you would pass to array.reduce
### Things you should `never` do inside a reducer:
- Mutate its argument
- Perform side effects like API calls and routing transitions
- Call non-pure functions, e.g. `Date.now()` or `Math.random()`.
- **Given the same arguments, it should calculate the next state and return it. No surprises. No side effects. No API calls. No mutations. Just a calculation.**
### Should use combineReducer
