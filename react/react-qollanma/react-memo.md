# React Memo

`memo`dan foydalanishda, agar uning propslari o'zgarmagan bo'lsa, React komponentni render qilishni o'tkazib yuborishiga olib keladi.

Bu ish faoliyatini yaxshilashi mumkin.

{% hint style="warning" %}
Ushbu bo'limda React Hooks ishlatiladi. Hooks haqida qo'shimcha ma'lumot olish uchun <mark style="color:green;">React Hooks</mark> bo'limiga o'ting.
{% endhint %}

### Muammo

Ushbu misolda, todos o'zgarmagan bo'lsa ham, `Todos` komponenti qayta render qilinadi.

{% code title="index.js:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState(["todo 1", "todo 2"]);

  const increment = () => {
    setCount((c) => c + 1);
  };

  return (
    <>
      <Todos todos={todos} />
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
      </div>
    </>
  );
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
{% endcode %}

{% code title="Todos.js:" %}
```jsx
const Todos = ({ todos }) => {
  console.log("child render");
  return (
    <>
      <h2>My Todos</h2>
      {todos.map((todo, index) => {
        return <p key={index}>{todo}</p>;
      })}
    </>
  );
};

export default Todos;
```
{% endcode %}

Tugmani bosganingizda, `Todos` komponenti qayta render qilinadi.

Agar ushbu komponent murakkab bo'lsa, u ishlash bilan bog'liq muammolarga olib kelishi mumkin.

### Yechim

Buni tuzatish uchun `memo`dan foydalanishimiz mumkin.

`Todos` komponentini ortiqcha render qilmaslik uchun `memo` dan foydalaning.

`Todos` komponenti eksportini `memo` ga aylantiring:

{% code title="index.js:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState(["todo 1", "todo 2"]);

  const increment = () => {
    setCount((c) => c + 1);
  };

  return (
    <>
      <Todos todos={todos} />
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
      </div>
    </>
  );
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
{% endcode %}

{% code title="Todos.js:" %}
```jsx
import { memo } from "react";

const Todos = ({ todos }) => {
  console.log("child render");
  return (
    <>
      <h2>My Todos</h2>
      {todos.map((todo, index) => {
        return <p key={index}>{todo}</p>;
      })}
    </>
  );
};

export default memo(Todos);
```
{% endcode %}

Endi `Todos` komponenti faqat props orqali unga uzatiladigan `todos` orqali yangilanganda render bo'ladi.
