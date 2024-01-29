# React Boshlash

{% hint style="warning" %}
React-ni productionda ishlatish uchun npm-ni o'z ichiga olgan Node.js kerak.
{% endhint %}

React nima ekanligi haqida umumiy ma'lumot olish uchun React kodini HTML-da yozib ko'rishingiz mumkin.

Ammo productionda React-dan foydalanish uchun sizda **npm** va **Node.js** o'rnatilgan bo'lishi kerak.

### HTMLda to'g'ridan-to'g'ri Reactdan foydalanish&#x20;

Reactni o'rganishni boshlashning eng tezkor usuli bu React kodlarini to'g'ridan-to'g'ri HTML fayllarda yozishdir.

<figure><img src="../../.gitbook/assets/image (441).png" alt=""><figcaption></figcaption></figure>

Uchta skript qo'shishdan boshlang, birinchi ikkita skript JavaScript-larda React kodini yozishga imkon beradi, uchinchi script Babel scripti esa eski brauzerlarda JSX sintaksisidan va ES6 dan foydalanish imkonini beradi.

JSX haqida <mark style="color:green;">React JSX</mark> bo'limida batafsil bilib olasiz.

HTML faylingizga uchta CDN qo'shish:

```html
<!DOCTYPE html>
<html>
  <head>
    <script src="" crossorigin></script>
    <script src="" crossorigin></script>
    <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  </head>
  <body>

    <div id="mydiv"></div>

    <script type="text/babel">
      function Hello() {
        return <h1>Hello World!</h1>;
      }

      const container = document.getElementById('mydiv');
      const root = ReactDOM.createRoot(container);
      root.render(<Hello />)
    </script>

  </body>
</html>
```

React-dan bu usulda foydalanish test maqsadida yaxshi bo'lishi mumkin, ammo production uchun React muhitini o'rnatishingiz kerak bo'ladi.

### React muhitini o'rnatish

Agar sizda npx va Node.js oʻrnatilgan boʻlsa, `create-react-app` yordamida React ilovasini yaratishingiz mumkin.

{% hint style="warning" %}
**Eslatma:** Agar avvalroq `create-react-app`ni global miqyosda oʻrnatgan boʻlsangiz, npx har doim `create-react-app`ning eng soʻnggi versiyasidan foydalanishini taʼminlash uchun uni oʻchirib tashlashingiz tavsiya qilinadi.&#x20;

O'chirish uchun quyidagi buyruqni bajaring: `npm uninstall -g create-react-app`
{% endhint %}

`my-react-app` nomli react ilovangizni yaratish uchun ushbu buyruqni bajaring:

```powershell
npx create-react-app my-react-app
```

`create-react-app` react ilovasini ishga tushirish uchun kerak bo'ladigan barcha narsani o'rnatadi.

### React ilovasini ishga tushiring

_Endi birinchi haqiqiy_ React ilovangizni ishga tushirishga tayyorsiz!

`my-react-app` papkasiga o'tish uchun ushbu buyruqni bajaring:

```bash
cd my-react-app
```

`my-react-app` react ilovasini ishga tushirish uchun ushbu buyruqni bajaring:

```powershell
npm start
```

Yangi yaratilgan React ilovangiz yangi brauzer oynasida ochiladi! Agar ochilmas, brauzeringizni oching va qidiruv qismiga `localhost:3000` ni kiriting.

Natija:

<figure><img src="https://www.w3schools.com/react/screenshot_myfirstreact.png" alt=""><figcaption></figcaption></figure>

### React ilovasini o'zgartiring

Hozircha yaxshi, lekin kontentni qanday o'zgartirishim mumkin ?

`my-react-app` papkasiga qarasangiz `src`  nomli papkani topasiz. `src` papkasining ichida, `App.js` deb nomlangan fayl bor, uni ochib qarasangiz quyidagicha ko'rinishda bo'ladi:

{% code title="/myReactApp/src/App.js:" %}
```jsx
import logo from './logo.svg';
import './App.css';

function App() {
  return (
    <div className="App">
      <header className="App-header">
        <img src={logo} className="App-logo" alt="logo" />
        <p>
          Edit <code>src/App.js</code> and save to reload.
        </p>
        <a
          className="App-link"
          href=""
          target="_blank"
          rel="noopener noreferrer"
        >
          Learn React
        </a>
      </header>
    </div>
  );
}

export default App;
```
{% endcode %}

HTML kodlarini o'zgartirib ko'ring va faylni saqlang.

{% hint style="warning" %}
O'zgarishlar faylni saqlaganingizdan keyin darhol ko'rinishiga e'tibor bering, brauzerni qayta yuklashingiz shart emas!
{% endhint %}

`<div className="App">` ichidagi barcha narsani `<h1>` elementiga almashtiring.

Saqlash tugmasini bosganingizda brauzerdagi o'zgarishlarga qarang:

```jsx
function App() {
  return (
    <div className="App">
      <h1>Hello World!</h1>
    </div>
  );
}

export default App;
```

{% hint style="warning" %}
E'tibor bering, biz kerak bo'lmagan importlarni olib tashladik (logo.svg va App.css).
{% endhint %}

Natija:

<figure><img src="https://www.w3schools.com/react/screenshot_helloworld.png" alt=""><figcaption></figcaption></figure>

### Endi nima ?

Endi sizning kompyuteringizda React Environmenti mavjud va siz React haqida ko'proq ma'lumot olishga tayyorsiz.

Ushbu qo'llanmaning qolgan qismida Reactning turli jihatlarini va ular brauzerda qanday ko'rsatilishini tushuntirish uchun "Show React" vositamizdan foydalanamiz.

Agar xuddi shu ishlarni kompyuteringizda bajarmoqchi bo'lsangiz, `src` papkasi faqat bitta `index.js` faylini o'z ichiga olishi uchun qolgan fayllarni o'chirib tashlashdan boshlang. Shuningdek, `index.js`  ichidagi keraksiz kod qatorlarini quyidagi “Show React” vositasidagi misolga o‘xshatish uchun olib tashlashingiz kerak:

Natijani ko'rish uchun "Run Example" tugmasini bosing.

{% code title="index.js:" %}
```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';

const myFirstElement = <h1>Hello React!</h1>

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(myFirstElement);
```
{% endcode %}
