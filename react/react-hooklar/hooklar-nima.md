# Hooklar nima ?

Hooklar Reactning 16.8 versiyasida qo'shildi.

Hooklar funksiya komponentlariga state va boshqa React xususiyatlariga murojaat qilish imkonini beradi. Shu sababli, class komponentlari endi kerak emas.

{% hint style="warning" %}
Hooklar odatda class komponentlarining o'rnini bosa olsada, React-dan classlarni olib tashlash to'g'risida rejalar yo'q.
{% endhint %}

### Hook nima ?

Hooklar state va lifecycle metodlari kabi React xususiyatlaga "hook"ni kiritsh imkonini beradi.

Mana hookga misol. Agar tushunmagan bo'lsangiz tashvishlanmang. Keyingi bo'limda bunga batafsilroq to'xtalamiz.

```jsx
import React, { useState } from "react";
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
      <button
        type="button"
        onClick={() => setColor("red")}
      >Red</button>
      <button
        type="button"
        onClick={() => setColor("pink")}
      >Pink</button>
      <button
        type="button"
        onClick={() => setColor("green")}
      >Green</button>
    </>
  );
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<FavoriteColor />);
```

{% embed url="https://www.w3schools.com/react/showreact.asp?filename=demo2_react_hooks" %}

`hook`larni React-dan `import` qilib olishingiz kerak.

Bu yerda ilovadagi holatni kuzatish uchun `useState` hookidan foydalanamiz.

State odatda kuzatilishi kerak bo'lgan ilova ma'lumotlariga yoki xususiyatlarini anglatadi.

### Hook qoidalari

Hooklarda 3 ta qoida mavjud:

* Hooklar faqat React funksiyasining komponentlari ichida chaqirilishi mumkin.
* Hooklar faqat komponentning eng tepasida chaqirilishi mumkin.
* Hooklar shartga asoslangan bo'lishi mumkin emas

{% hint style="warning" %}
**Eslatma:** Reactning class komponentlarida hooklar ishlamaydi.
{% endhint %}

### Maxsus hooklar

Agar bir nechta komponentlarda qayta ishlatilishi kerak bo'lgan statistik logika bo'lsa, o'zingizning shaxsiy hooklaringizni yaratishingiz mumkin.

Bu haqida <mark style="color:green;">Custom hooklar</mark> bo'limida batafsilroq to'xtalamiz.
