# React Componentlar

Komponentlar HTML elementlarini qaytaruvchi funksiyalarga o'xshaydi.

### React komponentlari

Komponentlar mustaqil va qayta ishlatiladigan kod qismlari hisoblanadi. Ular JavaScript funksiyalari bilan bir xil maqsadda ishlaydi, lekin izolyatsiyada ishlaydi va HTML elementlarini qaytaradi.

Komponentlar ikki xil bo'ladi: Class komponentlar va Funksiya komponentlar, bu qo'llanmada biz Funksiya komponentlariga e'tibor qaratamiz.

{% hint style="warning" %}
Eski react kodlarida asosan Class komponentlaridan foydalanilganligiga duch kelishingiz mumkin. Endi React 16.8 da qo'shilgan Hooks bilan birga funksiya komponentlaridan foydalanish tavsiya etiladi. Malumot uchun aytib o'tish lozimki, Class komponentlari bo'yicha o'rganish ixtiyoriy hisoblangan bo'lim mavjud.
{% endhint %}

### Birinchi komponentingizni yaratish

React komponentini yaratishda komponent nomi _katta_ katta harf bilan boshlanishi kerak.

#### Class komponenti

Class komponenti `extends React.Component` steytmentini o'z ichiga olishi kerak. Ushbu steytment **React.Component** uchun meros yaratadi va sizning komponentingizga **React.Component**ning funksiyalariga murojaat qilish huquqini beradi.

Komponent ham `render()` metodini talab qiladi, bu metod HTML elementini qaytaradi.

{% code title="Car deb nomlangan Class komponentini yaratish:" %}
```jsx
class Car extends React.Component {
  render() {
    return <h2>Hi, I am a Car!</h2>;
  };
};
```
{% endcode %}

### Funksiya komponenti

Bu yerda ham yuqoridagi kabi misol ko'rsatilgan, ammo unda class komponenti o'rniga funksiya komponentidan foydalanilagan.

Funksiya komponenti HTMLni ham qaytaradi va xuddi Class komponenti kabi ishlaydi, lekin funksiya komponentlari kamroq kod yordamida yoziladi va tushunishga osonroq bo'ladi. Biz bu qo'llanmada funksiya komponentidan foydalanishni afzal deb bilamiz.

{% code title="Car nomli funktsiya komponentini yaratish:" %}
```jsx
function Car() {
  return <h2>Hi, I am a Car!</h2>;
}
```
{% endcode %}

### Komponentni ko'rsatish

Endi sizning React ilovangizda `<h2>` elementini qaytaradigan Car nomli komponent mavjud.

Ushbu komponentni ilovangizda ishlatish uchun oddiy HTML kabi sintaksisdan foydalaning: `<Car />`

`Car` komponentini "root" elementida ko'rsating:

```jsx
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```

### Props

Komponentlar properties-ni ifodalovchi `props` sifatida uzatilishi mumkin.

Propslar funksiyaning argumentlariga o'xshaydi va ularni komponentga atribut sifatida yuborasiz.

Keyingi bo'limda `props` haqida ko'proq bilib olasiz .

{% code title="Colorni Car komponentiga o'tkazish uchun atributdan foydalanish va uni render() funksiyasida ishlatish:" %}
```jsx
function Car(props) {
  return <h2>I am a {props.color} Car!</h2>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car color="red"/>);
```
{% endcode %}

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_component_props" %}

### Komponentlar ichidagi komponentlar

Komponentlar ichidagi boshqa bir komponentlarga murojaat qilishimiz ham mumkin:

{% code title="Garage komponenti ichida Car komponentidan foydalanish:" %}
```jsx
function Car() {
  return <h2>I am a Car!</h2>;
}

function Garage() {
  return (
    <>
      <h1>Who lives in my Garage?</h1>
      <Car />
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Garage />);
```
{% endcode %}

### Fayllardagi komponentlar

React kodni qayta ishlatishga mo'ljallangan va komponentlaringizni alohida fayllarga ajratishni tavsiya qiladi.

Buning uchun .js kengaytmali yangi fayl yarating va uning ichiga kodni qo'ying:

{% hint style="warning" %}
E'tibor bering, fayl nomi bosh harf bilan boshlanishi kerak.
{% endhint %}

Bu yangi fayl, biz uni “Car.js” deb nomladik:

```jsx
function Car() {
  return <h2>Hi, I am a Car!</h2>;
}

export default Car;
```

Car komponentidan foydalanish uchun faylni ilovangizga import qilishingiz kerak.

Endi ilovaga "Car.js" faylini import qilamiz va `Car` komponentini xuddi shu faylda yaratilgandek ishlatishimiz mumkin.

```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';
import Car from './Car.js';

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Car />);
```

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_comp_in_files" %}
