# useState

Reactning `useState` hooki bizga funksiya komponentidagi holatni kuzatish imkonini beradi.

State odatda ilovada kuzatilishi kerak bo'lgan ma'lumotlar yoki xususiyatlarni anglatadi.

### Import `useState`

`useState` hookidan foydalanish uchun avvalo uni komponentimizga `import` qilishimiz kerak.

Komponentingizning yuqori qismiga, `useState` hookini `import` qiling.

```jsx
import { useState } from "react";
```

E'tibor bering, biz useState ni reactdan destructuring qilyapmiz, chunki bu o'z nomiga ega eksport.

{% hint style="warning" %}
Destructuring haqida ko'proq ma'lumot olish uchun <mark style="color:green;">ES6 bo'limiga</mark> o'ting.
{% endhint %}

### `useState`ni ishga tushirish

Funksiya komponentimizda `useState` ni chaqirish orqali steytimizni ishga tushiramiz.

`useState` dastlabki holatni qabul qiladi va ikkita qiymat qaytaradi:

* Hozirgi holat.
* Holatni yangilaydigan funksiya.

{% code title="Funktsiya komponentining yuqori qismidagi steytni ishga tushiring." %}
```jsx
import { useState } from "react";

function FavoriteColor() {
  const [color, setColor] = useState("");
}
```
{% endcode %}

&#x20;`useState`-dan qaytariladigan qiymatlarni destructuring qilayotganimizga e'tibor bering.

Birinchi qiymat `color` bizning hozirgi steytimiz.

Ikkinchi qiymat, `setColor`, bizning steytimizni yangilash uchun ishlatiladigan funksiyadir.

{% hint style="warning" %}
Bu nomlar o'zgaruvchilar bo'lib, uni o'zingiz xohlagaandek nomlashingiz mumkin.
{% endhint %}

Boshlang'ich steytni bo'sh string qildik: `useState("")`

### Steytni o'qish

Endi steytimizni komponentimizning istalgan joyiga kiritishimiz mumkin.

{% code title="Render qilinadigan komponentda steyt o'zgaruvchisidan foydalanish:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";

function FavoriteColor() {
  const [color, setColor] = useState("red");

  return <h1>My favorite color is {color}!</h1>
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<FavoriteColor />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_usestate" %}

### Steytni yangilash

Steytimizni yangilash uchun steytni yangilovchi funksiyadan foydalanamiz.

{% hint style="warning" %}
Biz hech qachon steytni to'g'ridan-to'g'ri yangilamasligimiz kerak. Masalan: `color = "red" qilib bo'lmaydi.`
{% endhint %}

{% code title="Steytni yangilash uchun tugmadan foydalanish:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";

function FavoriteColor() {
  const [color, setColor] = useState("red");

  return (
    <>
      <h1>My favorite color is {color}!</h1>
      <button
        type="button"
        onClick={() => setColor("blue")}
      >Blue</button>
    </>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<FavoriteColor />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_usestate_update" %}

### Steyt nima qabul qila oladi

`useState` hookidan stringlar, raqamlar, boolean qiymatlar, arraylar, obyektlar va ularning har qanday kombinatsiyasini kuzatish uchun foydalanish mumkin!

Biz individual qiymatlarni kuzatish uchun bir nechta steyt hooklarini yaratishimiz mumkin.

{% code title="Bir nechta steyt hooklarini yaratish:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";

function Car() {
  const [brand, setBrand] = useState("Ford");
  const [model, setModel] = useState("Mustang");
  const [year, setYear] = useState("1964");
  const [color, setColor] = useState("red");

  return (
    <>
      <h1>My {brand}</h1>
      <p>
        It is a {color} {model} from {year}.
      </p>
    </>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_usestate2" %}

Yoki faqat bitta steytdan foydalanishimiz va uning o'rniga obyekt kiritishimiz mumkin!

{% code title="Obyektni kuzatadigan bitta hook yaratish:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";

function Car() {
  const [car, setCar] = useState({
    brand: "Ford",
    model: "Mustang",
    year: "1964",
    color: "red"
  });

  return (
    <>
      <h1>My {car.brand}</h1>
      <p>
        It is a {car.color} {car.model} from {car.year}.
      </p>
    </>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_usestate5" %}

{% hint style="warning" %}
Hozir bitta obyektni kuzatayotganimiz sababli, komponentni ko'rsatishda ushbu obyektga, keyin esa ushbu obyektning xususiyatiga murojaat qilishimiz kerak. (Masalan: `car.brand`)
{% endhint %}

### Steytdagi obyektlar va arraylarni yangilash

State yangilanganda, butun state qaytadan yoziladi.

Agar faqatgina Carning color-ini yangilamoqchi bo'lsak nima bo'ladi ?

Agar faqatgina `setCar({color: "blue"})`ga murojaat qilsak, bu steytimizdan `brand`, `model` va `year`ni olib tashlaydi.

Bizga yordam berish uchun JavaScriptning Spread operatoridan foydalanishimiz mumkin.

{% code title="Faqat Carning colorini yangilash uchun JavaScriptning spread operatoridan foydalanish:" %}
```jsx
import { useState } from "react";
import ReactDOM from "react-dom/client";

function Car() {
  const [car, setCar] = useState({
    brand: "Ford",
    model: "Mustang",
    year: "1964",
    color: "red"
  });

  const updateColor = () => {
    setCar(previousState => {
      return { ...previousState, color: "blue" }
    });
  }

  return (
    <>
      <h1>My {car.brand}</h1>
      <p>
        It is a {car.color} {car.model} from {car.year}.
      </p>
      <button
        type="button"
        onClick={updateColor}
      >Blue</button>
    </>
  )
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_usestate4" %}

Bizga steytning joriy qiymati kerakligi sababli, funktsiyani o'zimizning `setCar` funksiyamizga o'tkazamiz. Bu funksiya oldingi qiymatni oladi.

Keyin obyektni qaytaramiz, `previousState` ni spread qilamiz va faqat rangni qayta yozamiz.
