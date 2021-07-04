### Big Ideas from W2D2 - Promises

- promises are a way to make async control flow more manageable
- using callback functions that get executed after an async function finishes can result in really messy and hard to reach callback hell
- promises allow for the use of .then and .catch chaining
- to use the nicer promise chaining, you have to wrap your vanilla async function in a function that returns a promise

#### function method of creating promise

```javascript
// before
// will need to nest a callback
setTimeout(() => {
  resolve();
}, 2000);

// after
// can use chaining
const promiseTest = () => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(`My new promise`);
    }, 2000);
  });
};

// function call that returns the new promose
promiseTest().then((data) => {
  console.log(data);
  // expected output: "My new promise"
});

console.log('Main thread hi');
```

#### creating the new promise right away

```javascript
const myPromise = new Promise((resolve, reject) => {
  setTimeout(() => {
    resolve('foo');
  }, 300);
});

promise1.then((value) => {
  console.log(value);
  // expected output: "foo"
});
```

- whatever is passed into the resolve will be accessible as an arguement for the next .then
- whatever is passed into the reject will be accessible by the .catch
