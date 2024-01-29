# React CSS Style

CSS orqali Reactga still berishning ko'plab usullari mavjud, bu qo'llanmada uchta asosiy still berish usullari batafsil ko'rib chiqiladi:

* Inline stillar
* CSS Stylesheet
* CSS modullari

### Inline still

Style atributiga ega elementga still berish uchun, beriladigan qiymat JavaScript obyekti boʻlishi kerak:

{% code title="Still kodlari berilgan obyektni kiritish:" %}
```jsx
const Header = () => {
  return (
    <>
      <h1 style={{color: "red"}}>Hello Style!</h1>
      <p>Add a little style!</p>
    </>
  );
}
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** JSX da JavaScript steytmentlari jingalak qavslar ichida yoziladi va JavaScript obyektlari ham jingalak qavslardan foydalanganligi sababli, yuqoridagi misoldagi still ikkita jingalak qavslar `{{}}` ichida yozilgan.
{% endhint %}

#### camelCaseli xususiyat nomlari

Inline CSS JavaScript obyekti sifatida yozilganligi uchun, `background-color` kabi chiziq bilan ajratilgan xususiyatlar camel case sintaksida yozilishi kerak:

{% code title="background-color o'rniga backgroundColor dan foydalaning:" %}
```jsx
const Header = () => {
  return (
    <>
      <h1 style={{backgroundColor: "lightblue"}}>Hello Style!</h1>
      <p>Add a little style!</p>
    </>
  );
}
```
{% endcode %}

#### JavaScript obyekti

Bundan tashqari, still kodlarini o'z ichiga olgan obyekt yaratishingiz va style atributiga murojaat qilishingiz mumkin:

{% code title=" myStyle nomidagi still obyektini yaratish:" %}
```jsx
const Header = () => {
  const myStyle = {
    color: "white",
    backgroundColor: "DodgerBlue",
    padding: "10px",
    fontFamily: "Sans-Serif"
  };
  return (
    <>
      <h1 style={myStyle}>Hello Style!</h1>
      <p>Add a little style!</p>
    </>
  );
}
```
{% endcode %}

### CSS Stylesheet

CSS stillaringizni alohida faylda ham yozishingiz mumkin, shunchaki faylni `.css`  kengaytmasi bilan saqlang va uni ilovangizga import qiling.

{% code title="App.css: "App.css" nomli yangi fayl yarating va unga bir nechta CSS kodlarini kiriting:" %}
```css
body {
  background-color: #282c34;
  color: white;
  padding: 40px;
  font-family: Sans-Serif;
  text-align: center;
}
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Siz xohlagan faylni chaqirishingiz mumkin, faqat fayl kengaytmasini eslab qoling.
{% endhint %}

{% code title=" index.js:  Ilovangizga css faylini import qiling:" %}
```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';
import './App.css';

const Header = () => {
  return (
    <>
      <h1>Hello Style!</h1>
      <p>Add a little style!.</p>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Header />);
```
{% endcode %}

### CSS modullari

Ilovangizga stillar qo'shishning yana bir usuli - bu CSS modullaridan foydalanish.

CSS modullari alohida fayllarga joylashtirilgan komponentlar uchun qulay hisoblanadi.

{% hint style="warning" %}
Modul ichidagi CSS faqat uni import qilgan komponent uchun mavjud bo'ladi va berilgan nomlar bilan kelishmovchiliklar paydo bo'lishidan xavotirlanmasangiz ham bo'ladi.
{% endhint %}

`.module.css` kengaytmasi yordamida CSS modulini yarating, misol: `my-style.module.css`.

{% code title="my-style.module.css: "my-style.module.css" nomli yangi fayl yarating va unga bir nechta CSS kodlarini kiriting:" %}
```css
.bigblue {
  color: DodgerBlue;
  padding: 40px;
  font-family: Sans-Serif;
  text-align: center;
}
```
{% endcode %}

{% code title="Car.js: Stillaringizni komponentingizga import qiling:" %}
```jsx
import styles from './my-style.module.css'; 

const Car = () => {
  return <h1 className={styles.bigblue}>Hello Car!</h1>;
}

export default Car;
```
{% endcode %}

{% code title="index.js: Ilovangizga komponentni import qiling:" %}
```jsx
import ReactDOM from 'react-dom/client';
import Car from './Car.js';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_css_modules" %}
