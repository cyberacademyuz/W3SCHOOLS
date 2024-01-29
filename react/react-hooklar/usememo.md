# useMemo

Reactning `useMemo` hooki xotirada saqlangan qiymatni qaytaradi.

{% hint style="warning" %}
Memoizatsiyani qiymatni keshlash deb hisoblang, shunda uni qayta hisoblash kerak emas.
{% endhint %}

`useMemo` hooki faqat bog'liqliklaridan biri yangilanganda ishlaydi.

Bu ish faoliyatini yaxshilashi mumkin.

{% hint style="warning" %}
`useMemo` va `useCallback` hooklar bir biriga o'xshash. Ularning asosiy farqi shundaki, `useMemo` xotirada saqlangan _qiymatni_ qaytaradi, `useCallback` esa xotirada saqlangan _funksiyani_ qaytaradi. useMemo haqida ko'proq ma'lumotni <mark style="color:green;">useMemo bo'limida</mark> olishingiz mumkin.
{% endhint %}

### Ishlash

`useMemo` hook qimmat va resurs talab qiladigan funksiyalarni ortiqcha ishga tushirishdan saqlash uchun ishlatilishi mumkin.

Ushbu misolda har bir renderda ishlaydigan qimmat funksiya mavjud.

Hisobni o'zgartirganda yoki topshiriq qo'shsangiz, bajarishda kechikish borligini sezasiz.

{% code title="Yomon ishlaydidan funktsiya. expensiveCalculation funktsiyasi har bir renderda ishlaydi:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);
  const calculation = expensiveCalculation(count);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = () => {
    setTodos((t) => [...t, "New Todo"]);
  };

  return (
    <div>
      <div>
        <h2>My Todos</h2>
        {todos.map((todo, index) => {
          return <p key={index}>{todo}</p>;
        })}
        <button onClick={addTodo}>Add Todo</button>
      </div>
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
        <h2>Expensive Calculation</h2>
        {calculation}
      </div>
    </div>
  );
};

const expensiveCalculation = (num) => {
  console.log("Calculating...");
  for (let i = 0; i < 1000000000; i++) {
    num += 1;
  }
  return num;
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
{% endcode %}

### `useMemo` foydalanish

Ushbu performance muammosini hal qilish uchun `expensiveCalculation` funksiyasini eslab qolish uchun `useMemo` hook-dan foydalanishimiz mumkin. Bu funksiya faqat kerak bo'lganda ishlaydi.

Qimmat funktsiya chaqiruvini `useMemo` bilan o'rashimiz mumkin.

`useMemo` hook bog'liqliklarni e'lon qilish uchun ikkinchi parametr qabul qiladi. Qimmat funktsiya faqat uning bog'liqliklari o'zgarganda ishlaydi.

Quyidagi misolda qimmat funksiya faqat `count` o'zgartirilganda ishlaydi, todolar qo'shilganda emas.

{% code title=" useMemo hook yordamida performancega misol:" %}
```jsx
import { useState, useMemo } from "react";
import ReactDOM from "react-dom/client";

const App = () => {
  const [count, setCount] = useState(0);
  const [todos, setTodos] = useState([]);
  const calculation = useMemo(() => expensiveCalculation(count), [count]);

  const increment = () => {
    setCount((c) => c + 1);
  };
  const addTodo = () => {
    setTodos((t) => [...t, "New Todo"]);
  };

  return (
    <div>
      <div>
        <h2>My Todos</h2>
        {todos.map((todo, index) => {
          return <p key={index}>{todo}</p>;
        })}
        <button onClick={addTodo}>Add Todo</button>
      </div>
      <hr />
      <div>
        Count: {count}
        <button onClick={increment}>+</button>
        <h2>Expensive Calculation</h2>
        {calculation}
      </div>
    </div>
  );
};

const expensiveCalculation = (num) => {
  console.log("Calculating...");
  for (let i = 0; i < 1000000000; i++) {
    num += 1;
  }
  return num;
};

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
{% endcode %}
