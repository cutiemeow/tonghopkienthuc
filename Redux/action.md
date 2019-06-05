# ACTION
- Actions are payloads of information that send data from your application to your store. They are the only source of information for the store. You send them to the store using `store.dispatch()`.
- Action:
  - are simple javascript object
  - must have a `type` property that indicates the type of action being performed
  - type should be defined as string constants `const ACTION_CLICK="CLICK"`
  - should create a separate module and import when we need 
  
    `import { ADD_TODO, REMOVE_TODO } from '../actionTypes'`
    
  - 
