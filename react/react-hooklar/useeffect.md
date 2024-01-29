# useEffect

`useEffect` hooki komponentlaringizda tashqi ta'sirlarni amalga oshirishga imkon beradi.

Tashqi ta'sirlarga ba'zi misollar: ma'lumotlarni olish, DOMni to'g'ridan-to'g'ri yangilash va taymerlar.

`useEffect` ikkita argument qabul qiladi, lekin ikkinchi argumentni berish ixtiyoriy.

`useEffect(<function>, <dependency>)`

Misol sifatida taymerdan foydalanamiz.

{% code title="Dastlabki renderdan keyin 1 soniya kutish uchun setTimeout() dan foydalanish:" %}
```jsx
import { useState, useEffect } from "react";
import ReactDOM from "react-dom/client";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    setTimeout(() => {
      setCount((count) => count + 1);
    }, 1000);
  });

  return <h1>I've rendered {count} times!</h1>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Timer />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_useeffect_settimeout" %}

Lekin qarab turing! U faqat bir marta hisoblashi kerak bo'lsada, hisoblashda davom etadi!

`useEffect` har bir renderda ishlaydi. Bu count o'zgarganda, har safar qayta render bo'lishini va bu boshqa effektni ishga tushirishini bildiradi.

Biz buni hohlamaymiz. Tashqi ta'sirlar paydo bo'lganda nazorat qilishning bir qancha usullari bor.

Har doim array qabul qiladigan ikkinchi parametrni kiritishimiz kerak. Biz ixtiyoriy hisoblangan bog'liqliklarni ushbu arraydagi `useEffect`-ga o'tkazishimiz mumkin.

{% code title="1. Hech qanday bo'g'liklik o'tkazilmagan:" %}
```jsx
useEffect(() => {
  //Har bir renderda ishga tushadi
});
```
{% endcode %}

{% code title="2. Bo‘sh Array:" %}
```jsx
useEffect(() => {
  //Faqatgina birinchi renderda ishga tushadi
}, []);
```
{% endcode %}

{% code title="3. Props yoki steyt qiymatlari:" %}
```jsx
useEffect(() => {
  //Birinchi renderda ishga tushadi
  //Va istalgan vaqtda har qanday bog'liqlik qiymati o'zgaradi
}, [prop, state]);
```
{% endcode %}

Shunday qilib, bu muammoni hal qilish uchun keling, ushbu ta'sir (effekt)ni faqat dastlabki renderda ishga tushiraylik.

{% code title="Effektni faqat dastlabki renderda ishga tushirish:" %}
```jsx
import { useState, useEffect } from "react";
import ReactDOM from "react-dom/client";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    setTimeout(() => {
      setCount((count) => count + 1);
    }, 1000);
  }, []); // <- bu yerga bo'sh to'rtburchakli qavslarni qo'shing

  return <h1>I've rendered {count} times!</h1>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Timer />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_useeffect_settimeout2" %}

Bu yerda o'zgaruvchiga bog'liq bo'lgan `useEffect` hook misoli keltirilgan. Agar `count` o'zgaruvchisi yangilansa, effekt yana ishga tushadi:

```jsx
import { useState, useEffect } from "react";
import ReactDOM from "react-dom/client";

function Counter() {
  const [count, setCount] = useState(0);
  const [calculation, setCalculation] = useState(0);

  useEffect(() => {
    setCalculation(() => count * 2);
  }, [count]); // <- bu yerga count o'zgaruvchisini qo'shing

  return (
    <>
      <p>Count: {count}</p>
      <button onClick={() => setCount((c) => c + 1)}>+</button>
      <p>Calculation: {calculation}</p>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Counter />);
```

Agar bir nechta bog'liqliklar mavjud bo'lsa, ular `useEffect` bog'liqliklar qatoriga kiritilishi kerak.

### Cleanup effekti

Ba'zi effektlar xotira to'lib qolishini kamaytirish uchun tozalashni talab qiladi.

Taymoutlar, obunalar, hodisa tinglovchilari va ortiq kerak bo'lmaydigan boshqa effektlar yo'q qilinishi kerak.

Biz buni `useEffect` hookining oxiriga return funksiyasini kiritish orqali amalga oshiramiz.

{% code title="useEffect hookning oxiridagi taymerni tozalash:" %}
```jsx
import { useState, useEffect } from "react";
import ReactDOM from "react-dom/client";

function Timer() {
  const [count, setCount] = useState(0);

  useEffect(() => {
    let timer = setTimeout(() => {
    setCount((count) => count + 1);
  }, 1000);

  return () => clearTimeout(timer)
  }, []);

  return <h1>I've rendered {count} times!</h1>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Timer />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_useeffect_settimeout_cleanup" %}

{% hint style="warning" %}
**Eslatma:** Taymerni tozalash uchun uni nomlashimiz kerak.
{% endhint %}
