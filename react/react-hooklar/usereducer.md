# useReducer

`useReducer` hooki `useState` hookga o'xshaydi.

Bu maxsus steyt logikasiga imkon beradi.

Agar murakkab logikaga tayanadigan bir nechta steyt qismlarini kuzatib borsangiz, `useReducer` foydali bo'lishi mumkin.

### Sintaksis

`useReducer` hook ikkita argument qabul qiladi.

{% hint style="warning" %}
useReducer(\<reducer>, \<initialState>)
{% endhint %}

`reducer` funksiyasi private steyt logikangizni o'z ichiga oladi va `initialState` oddiy qiymat bo'lishi mumkin, lekin odatda obyektni o'z ichiga oladi.

`useReducer` hook joriy `state` va `dispatch` metodini qaytaradi.

{% code title="Hisoblagich ilovasida useReducer ga misol:" %}
```jsx
import { useReducer } from "react";
import ReactDOM from "react-dom/client";

const initialTodos = [
  {
    id: 1,
    title: "Todo 1",
    complete: false,
  },
  {
    id: 2,
    title: "Todo 2",
    complete: false,
  },
];

const reducer = (state, action) => {
  switch (action.type) {
    case "COMPLETE":
      return state.map((todo) => {
        if (todo.id === action.id) {
          return { ...todo, complete: !todo.complete };
        } else {
          return todo;
        }
      });
    default:
      return state;
  }
};

function Todos() {
  const [todos, dispatch] = useReducer(reducer, initialTodos);

  const handleComplete = (todo) => {
    dispatch({ type: "COMPLETE", id: todo.id });
  };

  return (
    <>
      {todos.map((todo) => (
        <div key={todo.id}>
          <label>
            <input
              type="checkbox"
              checked={todo.complete}
              onChange={() => handleComplete(todo)}
            />
            {todo.title}
          </label>
        </div>
      ))}
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Todos />);
```
{% endcode %}

Bu todoning to'liq holatini kuzatib borish mantig'idir.

Todo qo'shish, o'chirish va bajarish uchun barcha logikalar qo'shimcha harakatlar qo'shish orqali bitta useReducer Hook-da bo'lishi mumkin.
