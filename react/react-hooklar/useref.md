# useRef

`useRef` hooki renderlar orasidagi qiymatlarni saqlab qolish imkonini beradi.

U yangilanganda qaytadan render bo'lishga sabab bo'lmaydigan o'zgaruvchi qiymatini saqlash uchun ishlatilishi mumkin.

U DOM elementiga to'g'ridan-to'g'ri murojaat qilish uchun ishlatilishi mumkin.

### Qayta renderlashga olib kelmaydi

Agar ilovamiz `useState` hooki yordamida necha marta renderlanishini hisoblashga harakat qilsak, cheksiz tsiklga tushib qolamiz, chunki bu hookning o'zi qayta render bo'lishga sabab bo'ladi.

Bunga yo'l qo'ymaslik uchun `useRef` hookidan  foydalanishimiz mumkin.

{% code title="Ilova renderlarini kuzatish uchun useRef dan foydalaning." %}
```jsx
import { useState, useEffect, useRef } from "react";
import ReactDOM from "react-dom/client";

function App() {
  const [inputValue, setInputValue] = useState("");
  const count = useRef(0);

  useEffect(() => {
    count.current = count.current + 1;
  });

  return (
    <>
      <input
        type="text"
        value={inputValue}
        onChange={(e) => setInputValue(e.target.value)}
      />
      <h1>Render Count: {count.current}</h1>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_useref" %}

`useRef()` faqat bitta elementni ya'ni `current` deb nomlangan obyektni qaytaradi.

`useRef` ni ishga tushirganimizda boshlang'ich qiymatni beramiz: `useRef(0)`.

{% hint style="warning" %}
Bu mana bunday qilishga o'xshaydi: `const count = {current: 0]`.`count.current` dan foydalanib countga murojaat qilishimiz mumkin.
{% endhint %}

Buni kompyuteringizda ishga tushiring va dasturni renderlash soni ortib borayotganini ko'rish uchun inputga yozib ko'ring.

### DOM elementlariga murojaat qilish

Umuman olganda, React-ga barcha DOM manipulyatsiyasini boshqarishga ruxsat berishni xohlaymiz.

Ammo `useref`dan muammo tug'dirmasdan foydalanish mumkin bo'lgan ba'zi holatlar mavjud.

React-da DOM-ga to'g'ridan to'gri murojaat qilish uchun elementga `ref` atributini qo'shishimiz mumkin.

{% code title="Inputni fokus qilish uchun useRef dan foydalaning:" %}
```jsx
import { useRef } from "react";
import ReactDOM from "react-dom/client";

function App() {
  const inputElement = useRef();

  const focusInput = () => {
    inputElement.current.focus();
  };

  return (
    <>
      <input type="text" ref={inputElement} />
      <button onClick={focusInput}>Focus Input</button>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_useref2" %}

### Steyt o'zgarishlarini kuzatish

`useRef` hooki oldingi steyt qiymatlarini kuzatish uchun ham ishlatilishi mumkin.

Buning sababi, biz renderlar orasida `useRef` qiymatlarini saqlab qolishimiz mumkin.

{% code title="Avvalgi steyt qiymatlarini kuzatish uchun useRefdan foydalanish:" %}
```jsx
import { useState, useEffect, useRef } from "react";
import ReactDOM from "react-dom/client";

function App() {
  const [inputValue, setInputValue] = useState("");
  const previousInputValue = useRef("");

  useEffect(() => {
    previousInputValue.current = inputValue;
  }, [inputValue]);

  return (
    <>
      <input
        type="text"
        value={inputValue}
        onChange={(e) => setInputValue(e.target.value)}
      />
      <h2>Current Value: {inputValue}</h2>
      <h2>Previous Value: {previousInputValue.current}</h2>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_useref3" %}

Bu safar avvalgi steytni kuzatish uchun, `useState`, `useEffect` va `useRef` kombinatsiyasidan foydalandik.

`useEffect`da input maydoniga matn kiritish orqali `inputValue` ni har safar yangilanganda `useRef` ning joriy qiymatini yangilaymiz.
