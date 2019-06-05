# ACTION

- Actions are payloads of information that send data from your application to your store. They are the only source of information for the store. You send them to the store using `store.dispatch()`.
- Action:
  - are simple javascript object
  - must have a `type` property that indicates the type of action being performed
  - type should be defined as string constants `const ACTION_CLICK="CLICK"`
  - should create a separate module and import when we need 
  
    `import { ADD_TODO, REMOVE_TODO } from '../actionTypes'`
    
  # Action Creator
  - Action creators are exactly that—functions that create actions
  - In Redux, action creators simply return an action: 
  
        function addTodo(text) {
         return {
            type: ADD_TODO,
            text
         }
        }

## Action.js
    /*
    * action types
    */

    export const ADD_TODO = 'ADD_TODO'
    export const TOGGLE_TODO = 'TOGGLE_TODO'
    export const SET_VISIBILITY_FILTER = 'SET_VISIBILITY_FILTER'

    /*
    * other constants
    */

    export const VisibilityFilters = {
      SHOW_ALL: 'SHOW_ALL',
      SHOW_COMPLETED: 'SHOW_COMPLETED',
      SHOW_ACTIVE: 'SHOW_ACTIVE'
    }

    /*
    * action creators
    */

    export function addTodo(text) {
     return { type: ADD_TODO, text }
    }

    export function toggleTodo(index) {
     return { type: TOGGLE_TODO, index }
    }

    export function setVisibilityFilter(filter) {
     return { type: SET_VISIBILITY_FILTER, filter }
    }
