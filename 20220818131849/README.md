# Setting up redux with typescript

`configureStore` API doesn't need any typings, but we will need to export `getState` as the root state and `dispatch` as the app dispatch so that they updated as the store updates.

`store.ts`
```typescript
import { configureStore } from "@redux/toolkit";

const store = configureStore({
	reducers: {
		posts: postsReducer,
		users: usersReducer
	};
});

export const RootState = ReturnType<typeof store.getState>;
export const AppDispatch = typeof store.dispatch;
```

Typing for react hooks. `useDispatch` will not know about thunks in redux store, so it needs to be typed. `useSelector` takes the store as the argument so we can pass here so we dont have to pass it every time.

`hooks.ts`
```typescript
import { TypedUseSelctorHook, useDuspatch, useSelector } from "react-redux";
import type { RootState , AppDispatch } from "./store.ts";

export const useAppDispatch: () => AppDispatch = useDispatch;
export const useAppSelector: TypedUseSelectorHook<RootState> = useSelector;
```

#redux #react-redux #configuration
