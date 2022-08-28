# Using redux toolkit to create reducers.

`createSlice` method creates slice with given `{ name, initialState, reducers }` it will automatically generate action creators for every reducer in this pattern `"${name}/${reducer}"` which is very helpfull.

`counterReducer.ts`
```typescript 
import { createSlice, PayloadAction } from "@redux/toolkit";

interface ICounterState {
  value: number
}

const initialState: ICounterState = {
  value: 0
}

export const counterSlice = createSlice({
  name: 'counter',
  initialState,
  // createSlice will infer state type from initialState
  reducers: {
    increment: state => {
      state.value += 1
    },
    decrement: state => {
      state.value -= 1
    },
    incrementByAmount: (state, action: PayloadAction<number>) => {
      state.value += action.payload
    }
  }
})

export const { increment, decrement, incrementByAmount } = counterSlice.actions
```

Also redux-toolkit uses library called Immer, it allows to write "mutating" reducer as shown in previous code block.

They're not actially mutating state, rather Immer tracks all the changes you've tried to make, and then uses that list of changes to return a safely immutably updated value.

#redux #reduxtoolkit #ts