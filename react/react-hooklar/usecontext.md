# useContext

### React Context

React Context - steytni global miqyosda boshqarish usulidir.

U ichma ich joylashtirilgan komponentlar o'rtasidagi holatni `useState`ni yo'lg'iz o'zini ishlatganga qaraganda osonroq ulashish uchun `useState` bilan birga ishlatilishi mumkin

### Muammo

Steyt steytga murojaat qilishni talab qiladigan stek ichida ota komponent tomonidan o'rab olinishi kerak.

Tasavvur qiling, bizda ko'plab ichma ich joylashgan komponentlar mavjud. Stackning yuqori va pastki qismidagi komponent steytga murojaat qilishi kerak.

Buni context-siz amalga oshirish uchun har bir ichki komponent orqali steytni "props" sifatida o'tkazishimiz kerak bo'ladi. Bu "prop drilling" deb ataladi.

{% code title=""props"ni ichki komponentlar orqali o'tkazish:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";

function Component1() {
  const [user, setUser] = useState("Jesse Hall");

  return (
    <>
      <h1>{`Hello ${user}!`}</h1>
      <Component2 user={user} />
    </>
  );
}

function Component2({ user }) {
  return (
    <>
      <h1>Component 2</h1>
      <Component3 user={user} />
    </>
  );
}

function Component3({ user }) {
  return (
    <>
      <h1>Component 3</h1>
      <Component4 user={user} />
    </>
  );
}

function Component4({ user }) {
  return (
    <>
      <h1>Component 4</h1>
      <Component5 user={user} />
    </>
  );
}

function Component5({ user }) {
  return (
    <>
      <h1>Component 5</h1>
      <h2>{`Hello ${user} again!`}</h2>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Component1 />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_context1" %}

2-4-komponentlar steytga muhtoj bo'lmasa ham, ular 5-komponentga yetib borishi uchun steytni o'tkazishlari kerak.

### Yechim

Yechim context yaratishdir.

#### Context  yaratish

Kontekst yaratish uchun `createContext` ni import qilishimiiz va ishga tushirish kerak:

```jsx
import { useState, createContext } from "react";
import ReactDOM from "react-dom/client";

const UserContext = createContext()
```

Keyinchalik, Context steytiga muhtoj bo'lgan komponentlar shajarasini o'rash uchun Context Providerdan foydalanamiz.

### Context Provider

Context Provider bilan bola komponentlarini o'rab oling va steyt qiymatini bering.

```jsx
function Component1() {
  const [user, setUser] = useState("Jesse Hall");

  return (
    <UserContext.Provider value={user}>
      <h1>{`Hello ${user}!`}</h1>
      <Component2 user={user} />
    </UserContext.Provider>
  );
}
```

Endi ushbu shajaradagi barcha komponentlar user context-iga murojaat qilish huquqiga ega bo'ladi.

### `useContext` hookidan foydalanish

Kontekstni bola komponentida ishlatish uchun `useContext` hooki yordamida unga murojaat qilishimiz kerak.

Birinchi, import steytmentiga `useContext`ni kiriting:

```jsx
import { useState, createContext, useContext } from "react";
```

Keyin barcha komponentlarda user context-iga murojaat qilish mumkin:

```jsx
function Component5() {
  const user = useContext(UserContext);

  return (
    <>
      <h1>Component 5</h1>
      <h2>{`Hello ${user} again!`}</h2>
    </>
  );
}
```

### To'liq misol

React Context-dan foydalangan holda to'liq misol:

```jsx
import { useState, createContext, useContext } from "react";
import ReactDOM from "react-dom/client";

const UserContext = createContext();

function Component1() {
  const [user, setUser] = useState("Jesse Hall");

  return (
    <UserContext.Provider value={user}>
      <h1>{`Hello ${user}!`}</h1>
      <Component2 />
    </UserContext.Provider>
  );
}

function Component2() {
  return (
    <>
      <h1>Component 2</h1>
      <Component3 />
    </>
  );
}

function Component3() {
  return (
    <>
      <h1>Component 3</h1>
      <Component4 />
    </>
  );
}

function Component4() {
  return (
    <>
      <h1>Component 4</h1>
      <Component5 />
    </>
  );
}

function Component5() {
  const user = useContext(UserContext);

  return (
    <>
      <h1>Component 5</h1>
      <h2>{`Hello ${user} again!`}</h2>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Component1 />);
```
