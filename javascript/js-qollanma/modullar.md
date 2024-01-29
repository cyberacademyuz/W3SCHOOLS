# Modullar

### Modullar

Javascript modullari kodingizni turli fayllarga ajratish imkonini beradi.

Bu kodlaringiz toʻplamini saqlashni osonlashtiradi.

Modullar import steytmenti yordamida tashqi fayllardan import qilib olinadi.

Modullarni `<script>` tegida `type="module"` orqali ham import qilish mumkin.

```
<script type="module">
import message from "./message.js";
</script>
```

### Eksport

Funksiyalar yoki o'zgaruvchilardan tashkil topgan modullar har qanday tashqi faylda saqlanishi mumkin.

Eksportning ikki turi mavjud: nomga ega eksport va standart eksport.

### Nomlangan eksport

Keling, `person.js` nomli fayl yaratamiz va uni eksport qilmoqchi bo'lgan kodlarimiz bilan to'ldiramiz.

Oʻz nomiga ega eksportlarni ikki yo'l bilan yaratishingiz mumkin. Alohida bir qatorda yoki barchasini birdaniga pastki qatorda.

{% code title="In-line sifatida: person.js" %}
```
export const name = "Jesse";
export const age = 40;
```
{% endcode %}

{% code title="Hammasi bir vaqtning o'zida pastki qismida: person.js" %}
```
const name = "Jesse";
const age = 40;

export {name, age};
```
{% endcode %}

### Standart eksportlar

Keling, `message.js` nomli boshqa bir fayl yaratamiz va undan standart eksportni koʻrsatish uchun foydalanaylik.

Faylingizda faqat bitta standart eksportga ega boʻlishingiz mumkin.

{% code title="message.js" %}
```
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

{% code title="Nomga ega eksportlardan import qilish:" %}
```
// person.js faylidan nomli eksportlarni import qiling:
import { name, age } from "./person.js";
```
{% endcode %}

{% code title="Standart eksportlardan import qilish" %}
```
// message.js faylidan standart eksportni import qiling:
import message from "./message.js";
```
{% endcode %}

{% hint style="warning" %}
### Eslatma

Modullar faqat HTTP(S) protokoli bilan ishlaydi.

file:// protokoli orqali ochilgan veb-sahifa import/eksportdan foydalana olmaydi.
{% endhint %}
