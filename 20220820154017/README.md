# Redux memoization with `createSelector`

Memoization is a form of caching. It involves tracking inputs to a function, and storing the inputs and the results for later reference. If a function is called with the same inputs as before, the function can skip doing the actual work, and return the same result it generated the last time it received those input values.

`createSelector` can accept multiple input selectors, which can be provided as separate arguments or as an array. The results from all the input selectors are provided as separate arguments to the output selector:

```javascript
const selectA = (state) => state.a;
const selectB = (state) => state.b;
const selectC = (state) => state.c;

const selectABC = createSelector([selectA, selectB, selectC], (a, b, c) => {
  // do something with a, b, and c, and return a result
  return a + b + c;
});

// Call the selector function and get a result
const abc = selectABC(state);

// could also be written as separate arguments, and works exactly the same
const selectABC2 = createSelector(selectA, selectB, selectC, (a, b, c) => {
  // do something with a, b, and c, and return a result
  return a + b + c;
});
```

#redux #memoization #rtk