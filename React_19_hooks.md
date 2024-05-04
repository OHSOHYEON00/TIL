React 19 Beta Updated

# Actions

Background

- It is very common to need to change state values in react after data mutation. This is often caused by forms, and we want to be able to automatically handle pending states, errors, form resets, etc.

Actions

- All functions that use async transitions (useTransition hook) are called Actions.


## useTransition

```
export function useTransition(): [boolean, TransitionStartFunction];
```
boolean: pending state (value provided by React to prevent the user from controlling UI pending state changes for async calls separately)

TransitionStartFunction: call async call inside, error handling


## useActionState

- Renamed from the existing `useFormState` hook. `useFormState` is deprecated.

```
export function useActionState<State>(
    action: (state: Awaited<State>) => State | Promise<State>,
    initialState: Awaited<State>,
    permalink?: string,
): [state: Awaited<State>, dispatch: () => void, isPending: boolean];
```

- state: async call state
- dispatch: You can attach the dispatch: function to start action and its value directly to elements like form, button, input, etc. as an event handler for submitting the form.
  - Example: <form onSubmit={dispatch}>
	- If the form action succeeds, React will automatically initialize the form. If the developer needs to reset the form arbitrarily, they can use the React Dom API called `requestFormReset`.
- isPending: pending state of the Action

The data is the result of the action function passed as props.


## useFormStatus

Purpose

- To let elements in a form know when they need to know the state of the form without drilling into props.

Condition

- the component must be rendered inside the form
	Why: Because the form acts like a Context Provider, you don't need to supply the value of the form separately

How to use it

- Call the useFormStatus hook from within the component that needs to know the state value of the form to use the value.


## useOptimistic

Purpose

- lets you know a different state while an async action is in progress.

```
    export function useOptimistic<State>(
        passthrough: State,
    ): [State, (action: State | ((pendingState: State) => State)) => void];
```

## use

- new API from React

Purpose

- lets you read the value of a resource (Promise, Context) regardless of the component's layer.

Features

- `use` can be used within loops, and conditional statements.
- Of course, `use` API must be called in function (functional component or hook)
- the result of `use` is the value for the Promise or Context

### Questions

Q1. I see that `useTransition` is also used to call async, and `useActionState` is also used to call async, but I don't know why they need both?

Q2. How can I use `useOptimistic` hook useful?

Q3. Vague understanding of `use` 
```
When called with a Promise, the use API integrates with Suspense and error boundaries. The component calling use suspends while the Promise passed to use is pending. If the component that calls use is wrapped in a Suspense boundary, the fallback will be displayed.  Once the Promise is resolved, the Suspense fallback is replaced by the rendered components using the data returned by the use API. If the Promise passed to use is rejected, the fallback of the nearest Error Boundary will be displayed.
```


### References
https://react.dev/blog/2024/04/25/react-19#whats-new-in-react-19

