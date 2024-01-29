# React Yangilash

## React 18 ga yangilash

Mavjud React loyihangizni 18 versiyaga yangilash uchun 2 ta qadam talab qilinadi.

{% hint style="warning" %}
Agar allaqachon React 18 versiyasidan foydalanadigan `create-react-app` ning so‘nggi versiyasidan foydalanayotgan bo‘lsangiz, ushbu bo‘limni o‘tkazib yuborishingiz mumkin.
{% endhint %}

## 1-Qadam: React 18 ni o'rnatish

Eng so'nggi versiyani o'rnatish uchun loyiha papkasida terminal orqali quyidagil buyruqlarni ishga tushiring:

```bash
npm i react@latest react-dom@latest
```

## 2-Qadam: Yangi root API-dan foydalanish

React 18 ning konkurent funksiyalaridan foydalanish uchun client render bo'lishi uchun yangi root API dan foydalanishingiz kerak bo‘ladi.

```jsx
// Oldin
import ReactDOM from 'react-dom';
ReactDOM.render(<App />, document.getElementById('root'));

// Keyin
import ReactDOM from 'react-dom/client';
const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<App />);
```

{% hint style="warning" %}
Ilovangizda yangi root API-dan foydalanmasangiz ham ishlaydi. Agar `ReactDOM.render` dan foydalanishda davom etsangiz, ilovangiz React 17 da ishlaydi.
{% endhint %}
