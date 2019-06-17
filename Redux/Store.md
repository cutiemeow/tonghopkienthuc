# Store
- Store is the object that bring (action, reducer) together. The store has the following responsibilities:
 1. Hold the app state
 2. Allow access  to state via `getState()`
 3. Allows state to be updated via `dispatch(action)`
 4. Register listener via `subscribe(listener)`
 5. Handles unregistering of listeners via the function returned by `subscribe(listener)`.
