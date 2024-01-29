# ES6 Modullar

### Modullar

JavaScript modullari kodingizni alohida fayllarga ajratish imkonini beradi.

Bu kodlaringiz toʻplamini saqlashni osonlashtiradi.

ES modullari `import` va `export` steymentlariga tayanadi.

### Eksport

Istalgan fayldan funksiya yoki oʻzgaruvchini eksport qilishingiz mumkin.

Keling, `person.js` nomli fayl yaratamiz va uni eksport qilmoqchi bo'lgan kodlarimiz bilan to'ldiramiz.

Eksportning ikki turi mavjud: **Nomiga ega** va **Standart**.

### Nomlangan eksport

O'z nomiga ega eksportlarni ikki yo'l bilan yaratishingiz mumkin. Alohida bir qatorda yoki pastki qatorda barchasini bittada eksport qilish.

In-line sifatida eksport qilishga misol:

{% code title="person.js" %}
```jsx
export const name = "Jesse"
export const age = 40
```
{% endcode %}

pastki qismda barchasini bittada eksport qilishga misol:

{% code title="person.js" %}
```jsx
const name = "Jesse"
const age = 40

export { name, age }
```
{% endcode %}

### Standart eksportlar

Keling, `message.js` nomli boshqa fayl yaratamiz va standart eksportni ko'rsatib berish uchun undan foydalanamiz.

Faylingizda faqat bitta standart eksportga ega boʻlishingiz mumkin.

{% code title="message.js" %}
```jsx
const message = () => {
  const name = "Jesse";
  const age = 40;
  return name + ' is ' + age + 'years old.';
};

export default message;
```
{% endcode %}

### Import

Modullarni faylga nomga ega eksport yoki standart eksport ekanligiga qarab ikki hil usulda import qilishingiz mumkin.

Nomga ega eksportlar jingalak qavslar yordamida tuziladi. Standart eksportlar esa bunday tuzilmaydi.

{% code title="person.js faylidan o'z nomsiga eksportlarni import qiling:" %}
```jsx
import { name, age } from "./person.js";
```
{% endcode %}

{% code title="message.js faylidan standart eksportni import qiling:" %}
```jsx
import message from "./message.js";
```
{% endcode %}
