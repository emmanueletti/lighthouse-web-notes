### Big Ideas from W1D4 - Callbacks

- in JS everything is either a primitive or an object
  - Primitives
    - boolean
    - string
    - null
    - undefined
    - bigint
  - Objects
    - objects
    - arrays (fancy objects)
- special to JS: functions (behavior) are treated as values and can thus be
  - passed around to variables
  - passed into other functions are arguements
  - returned from other functions
  - stored in arrays and objects
- functions are ["first class citizens / entities"](https://en.wikipedia.org/wiki/First-class_citizen)
- callback functions are functions that passed to other functions and then called by those functions (Higher order functions)
- Higher order functions are functions that call other functions (callbacks)
- Single Responsilbity can be achieved by creating higher order functions
- or by creating smaller functions use the return value of another small function as its inputs
- all array and object names need to be pluralized!!
- use const for everything until you have to use let b/c varaible is to be reassigned
- examples of really useful JS HOF's
  - map => when you need to transform every element in an array - does not change the original array
  - filter => when you need to filter out certain elements based on passing certain requirements - does not change the original array
  - reduce => can do anytthing! super powerful!

#### Functional Programming

- important part of functional programming is breakdong down functionality into small packages actions that are single tasked
- each action is then peiced together like lego blocks to "compose" the results we want
- each function "block" is made as general and reuseable as possible
- BUT only to the point that readability isn't reduced
- readability comes first before optimization!
- it can be okay not to have the more optimzed single responsible code, code written will never be perfect, readiblity ALWAYS comes first
- always ask if in 6 months time, will I or another developer be able to understand what I have written
- code that can't be read can't be maintained, added on

#### Solving problems strategy

1. breakdown the problem
   - inputs?
   - outputs?
   - contraints?
   - edge case?
   - solve the first iterations by hand
2. solve problem ITERATIVELY with FOCAL fundamentals
3. refactor
   - can loops be replaced with JS higher order functions? (map, filter, reduce, etc)
   - any pre-built JS methods?
   - DRY?
   - single responsiblity?
   - modules and import what is needed?
   - can results be composed?

- to see if function can be simplified, walk through what the function does and see all the times you have to say "and then it does..."
  - BUT within reason
