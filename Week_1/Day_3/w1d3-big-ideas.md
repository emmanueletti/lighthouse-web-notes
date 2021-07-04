### Big Ideas from W1D2 - Objects

- all of JS is designed around objects
- almost everything in JS is derived from key:value data strucures (objects)
- object keys are always strings
- 3 ways to access object properties
  - bracket notation
    - more flexible
    - allows for computed quering of objects
    - allows for referencing object keys that use non-standard naming
  - dot notation (shorthand)
    - simpler to write but very inflexible
    - can only be used to reference the exact name of already existing keys

* whenever you call a function and pass an arguement into it, the function creates a copy of that arguement's value and creates a variable to assign it to according to its definition

```javascript
const myFunction = (data) => {
  return data.length;
};

myFunction('hello');
```

- what happens here is that when myFunction is called and run's it will take the value passed in as an argument and within its scope/frame in the call stack/heap it will create a variable called "data" and assign it to the value "hello"
- once myFunction returns it then gets pushed off the call stack and then its local variables get deleted automatically from heap memory (garbage collected)
- this is why parent scopes can't access variables/data in child scopes but child scopes can access and remember parent scope variables
- BUT when functions or objects are passed as an arguement to a function, a pointer reference is what is copied into the functions local variable - NOT a copy of the obj/function

```javascript
const myFunction = (obj) => {
  return obj.key;
};

const myObj = { a: 1, b: 2 };

myFunction(myObj);
```

- when functions get passed no primitives (objects, arrays) a direct copy is NOT created and passed to the local functions variable (pass by value) BUT instead a reference to the objct is passed to the local functions variable (pass by reference)

- use python tutor's javascript visualizer to help see how JS evaluates scripts (use with HTTPS everywhere turned off)
