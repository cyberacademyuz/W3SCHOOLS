# React Sass Styling

### Sass nima ?

Sass CSS ning pre-protsessori hisoblanadi

Sass fayllari serverda bajariladi va CSS kodini brauzerga yuboradi.

Sass haqida ko'proq ma'lumot olish uchun <mark style="color:green;">Sass qo'llanma</mark>mizga o'ting.

### Sassdan foydalanishim mumkinmi ?

Agar loyihangizda `create-react-app` dan foydalansangiz, Sass-ni React loyihalaringizda osongina o'rnatishingiz va ishlatishingiz mumkin.

Terminalingizda ushbu buyruqni bajarish orqali Sass-ni o'rnating:

```bash
npm i sass
```

Endi Sass fayllarini loyihangizga qo'shishga tayyorsiz!

### Sass faylini yarating

Sass faylini xuddi CSS fayllarini yaratganingizdek yarating, lekin Sass fayllari `.scss` kengaytmasiga ega.

Sass fayllarida o'zgaruvchilar va boshqa Sass funksiyalaridan foydalanishingiz mumkin:



{% code title="my-sass.scss: Matn rangini berish uchun o'zgaruvchi yaratish:" %}
```sass
$myColor: red;

h1 {
  color: $myColor;
}
```
{% endcode %}

{% code title="index.js: Sass faylini CSS faylini import qilganingiz kabi import qiling:" %}
```jsx
import React from 'react';
import ReactDOM from 'react-dom/client';
import './my-sass.scss';

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
