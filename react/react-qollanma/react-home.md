# React HOME

{% hint style="success" %}
React - bu UI tuzish uchun JavaScript kutubxona hisoblanadi.

React bir sahifali saytlar tuzish uchun ishlatiladi.

React bizga qayta foydalanish mumkin bo'lgan UI komponentlar yaratishga imkon beradi.
{% endhint %}

### Misollar orqali o'rganish

Bizning "Reactni ko'rsat" vositamiz React kodlaringizning natijasini ko'rsatishni osonlashtiradi. U kodni ham, natijani ham ko'rsatadi.

```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';

function Hello(props) {
  return <h1>Hello World!</h1>;
}

const container = document.getElementById("root");
const root = ReactDOM.createRoot(container);
root.render(<Hello />);
```

### React viktorina

Viktorinada React bo'yicha ko'nikmalaringizni sinab ko'ring.

![](<../../.gitbook/assets/image (393).png>)

### React App yaratish

React-ni o'rganish va sinab ko'rish uchun kompyuteringizga React Environment-ni o'rnatishingiz kerak.

Ushbu qo'llanmada `create-react-app`dan foydalaniladi.

`create-react-app` vositasi React ilovalarini yaratishning rasmiy qoʻllab-quvvatlanadigan usuli hisoblanadi.

`create-react-app` dan foydalanish uchun Node.js talab qilinadi.

Ilovangizni yaratmoqchi bo'lgan papkangizda terminalni oching.

`my-react-app` nomli react ilovangizni yaratish uchun ushbu buyruqni bajaring:

```powershell
npx create-react-app my-react-app
```

`create-react-app` react ilovasini ishga tushirish uchun kerak bo'ladigan barcha narsani o'rnatadi.

{% hint style="warning" %}
**Eslatma:** Agar avvalroq `create-react-app`ni global miqyosda oʻrnatgan boʻlsangiz, `npx` har doim `create-react-app`ning eng soʻnggi versiyasidan foydalanishini taʼminlash uchun uni oʻchirib tashlashingiz tavsiya qilinadi. O'chirish uchun quyidagi buyruqni bajaring: `npm uninstall -g create-react-app`
{% endhint %}

### React ilovasini ishga tushiring

`my-react-app` papkasiga o'tish uchun ushbu buyruqni bajaring:

```bash
cd my-react-app
```

`my-react-app` react ilovasini ishga tushirish uchun ushbu buyruqni bajaring:

```bash
npm start
```

Yangi yaratilgan React ilovangiz yangi brauzer oynasida ochiladi! Agar ochilmasa, brauzeringizni oching va qidiruv qismiga `localhost:3000` ni kiriting.

Natija:\


<figure><img src="https://www.w3schools.com/react/screenshot_myfirstreact.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
`create-react-app` haqida [<mark style="color:green;">Reactni boshlash</mark>](react-boshlash.md) bo'limida ko'proq narsa bilib olasiz.
{% endhint %}

### Bilishingiz kerak bo'lgan texnologiyalar

ReactJS bilan ishlashni boshlashdan avval quyidagilar bo'yicha ba'zi ko'nikmalarga ega bo'lishingiz kerak:

* HTML
* CSS
* JavaScript

Shuningdek, ECMAScript 6 (ES6) da kiritilgan yangi JavaScript funksiyalari bilan ham biroz ko'nikmaga ega bo‘lishingiz kerak, ular haqida <mark style="color:green;">React ES6</mark> bo'limida bilib olasiz.
