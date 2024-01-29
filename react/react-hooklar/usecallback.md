# useCallback

Reactning `useCallback` hooki xotirada saqlangan callback funksiyani qaytaradi.

{% hint style="warning" %}
Memoizatsiyani qiymatni keshlash deb hisoblang, shunda uni qayta hisoblash kerak emas.
{% endhint %}

Bu bizga resurs talab qiladigan funksiyalarni har bir renderda avtomatik tarzda ishlamasligi uchun izolyatsiyalash (ajratish) imkonini beradi.

`useCallback` hook faqat bog'liqliklaridan biri yangilanganda ishlaydi.

Bu ish faoliyatini yaxshilashi mumkin.

{% hint style="warning" %}
`useCallback`va `useMemo` hooklar bir biriga o'xshash. Ularning asosiy farqi shundaki, `useMemo` xotirada saqlangan _qiymatni_ qaytaradi, `useCallback` esa xotirada saqlangan _funksiyani_ qaytaradi. useMemo haqida ko'proq ma'lumotni <mark style="color:green;">useMemo bo'limida</mark> olishingiz mumkin.
{% endhint %}

#### Muammo

`useCallback` dan foydalanishning sabablaridan biri, agar uning porpsi o'zgarmagan bo'lsa, komponentni qayta renderlashni oldini olishdir.

Ushbu misolda, agar `todos` o'zgarmasa, `Todos` komponenti qayta renderlanmaydi deb o'ylashingiz mumkin:

{% hint style="warning" %}
Bu React.memo bo'limidagi misolga o'xshash.
{% endhint %}

{% code title="index.js" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = () => {
    setTodos((t) => [...t, "New Todo"]);
  };

  return (
    <>
      <Todos todos={todos} addTodo={addTodo} />
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

{% code title="Todos.js" %}
```jsx
import { memo } from "react";

const Todos = ({ todos, addTodo }) => {
  console.log("child render");
  return (
    <>
      <h2>My Todos</h2>
      {todos.map((todo, index) => {
        return <p key={index}>{todo}</p>;
      })}
      <button onClick={addTodo}>Add Todo</button>
    </>
  );
};

export default memo(Todos);
```
{% endcode %}

Buni ishga tushirib ko'ring va qiymatni oshirish tugmasini bosing.

`todos` o'zgarmagan taqdirda ham `Todos` komponenti qayta renderlanishini sezasiz.

Bu nega ishlamayapti ? Biz `memo`dan foydalanyapmiz, shuning uchun `Todos` komponenti qayta renderlamasligi kerak, chunki count ko'paytirilganda `todos` steyti ham `addTodo` funksiyasi ham o'zgarmaydi.

Buning sababi "referential equality" deb ataladigan narsada.

Har safar komponent qayta renderlanganda, uning funktsiyalari qayta yaratiladi. Shu sababli, `addTodo` funktsiyasi aslida o'zgardi.

### Yechim

Buni to'g'irlash uchun, agar kerak bo'lmasa, funksiyaning qayta yaratilishiga yo'l qo'ymaslik uchun `useCallback` hookidan foydalanishimiz mumkin.

`Todos` komponentining ortiqcha qayta renderlanishini oldini olish uchun `useCallback` hookidan  foydalaning:

{% code title="index.js" %}
```jsx
import { useState, useCallback } from "react";
import ReactDOM from "react-dom/client";
import Todos from "./Todos";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = useCallback(() => {
    setTodos((t) => [...t, "New Todo"]);
  }, [todos]);

  return (
    <>
      <Todos todos={todos} addTodo={addTodo} />
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

{% code title="Todos.js" %}
```jsx
import { memo } from "react";

const Todos = ({ todos, addTodo }) => {
  console.log("child render");
  return (
    <>
      <h2>My Todos</h2>
      {todos.map((todo, index) => {
        return <p key={index}>{todo}</p>;
      })}
      <button onClick={addTodo}>Add Todo</button>
    </>
  );
};

export default memo(Todos);
```
{% endcode %}

Endi `Todos` komponenti faqat `todos` propi o'zgarganda qayta renderlanadi.
