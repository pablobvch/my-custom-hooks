# Custom Hooks Documentation

This repository contains custom hooks for React applications. These hooks are designed to simplify common tasks in React development.

## Hooks

### 1. `useCounter`

The `useCounter` hook provides a simple way to manage a counter state.

#### Usage

```
import { useCounter } from "./useCounter";

const CounterComponent = () => {
  const { counter, increment, decrement, reset } = useCounter(10);

  return (
    <div>
      {" "}
      <p>Counter: {counter}</p> <button onClick={increment}>Increment</button>{" "}
      <button onClick={decrement}>Decrement</button>{" "}
      <button onClick={reset}>Reset</button>{" "}
    </div>
  );
};
```

### 2. `useFetch`

The `useFetch` hook is used to fetch data from a given URL. It manages the loading and error states.

#### Usage

```
import { useFetch } from "./useFetch";

const FetchComponent = () => {
  const { data, isLoading, hasError } = useFetch(
    "https://api.example.com/data"
  );

  if (isLoading) return <p>Loading...</p>;
  if (hasError) return <p>Error loading data.</p>;

  return <div> {/* Render your data here */} </div>;
};
```


### 3. `useForm`

The `useForm` hook simplifies form state management. It handles input changes and form resetting.

#### Usage

```
import { useForm } from "./useForm";

const FormComponent = () => {
  const { formState, onInputChange, onResetForm } = useForm({
    name: "",
    email: "",
  });

  return (
    <form>
      {" "}
      <input name="name" value={formState.name} onChange={onInputChange} />{" "}
      <input name="email" value={formState.email} onChange={onInputChange} />{" "}
      <button type="button" onClick={onResetForm}>
        Reset
      </button>{" "}
    </form>
  );
};
```

### 4. `useTodo`

The `useTodo` hook manages a list of todos. It includes actions to add, remove, and toggle todos.

#### Usage

```
import { useTodo } from "./useTodo";

const TodoComponent = () => {
  const {
    todos,
    handleNewTodo,
    handleDeleteTodo,
    handleToggleTodo,
    pendingTodosCount,
    todosCount,
  } = useTodo();

  // Render your todos and controls here
};
```


## License

This project is open-source software licensed under the [MIT License](LICENSE).
