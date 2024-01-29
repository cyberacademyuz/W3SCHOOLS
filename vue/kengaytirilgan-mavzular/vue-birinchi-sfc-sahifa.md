# Vue Birinchi SFC sahifa

{% hint style="success" %}
Bizning birinchi SFC veb-sahifamizni noldan yaratish uchun biz:

1. Yangi toza Vue loyihasini yarating
2. Kodni "App.vue" fayliga yozing
3. Veb-sahifani ishlab chiqish jarayonida avtomatik ravishda qanday yangilanishini ko'ring
4. Ishlab chiqarish uchun sahifa yarating
{% endhint %}

### Toza loyiha yarating

Endi biz Vue-da o'zimizning oddiy veb-sahifamizni yaratish uchun oldingi sahifada yaratgan namunaviy loyihadagi barcha tarkibni olib tashlaymiz.

Kod yozishni boshlashdan oldin , va teglar ichidagi barcha tarkibni olib tashlang `<template>`va `<script>`" `<style>`o'rnatish" yoki "ko'lamli" kabi atributlarni olib tashlang.

"App.vue" faylingiz endi shunday ko'rinishi kerak:

{% code title="App.vue:" %}
```html
<script></script>

<template></template>

<style></style>
```
{% endcode %}

Shuningdek, "src" jildidagi "aktivlar" va "komponentlar" papkalarini olib tashlang.

"main.js" fayli ichidagi aktivlar import qilinadigan qatorni olib tashlang, shunda "main.js" quyidagicha ko'rinadi:

{% code title="main.js:" %}
```jsx
import { createApp } from 'vue'
import App from './App.vue'

createApp(App).mount('#app')
```
{% endcode %}

Endi bizda ishlash uchun bo'sh loyiha bor.

### "App.vue" da kod yozing

Endi bizda toza loyiha bor, teg ichiga sarlavha qo'shing `<template>`, masalan:

```jsx
<template>
  <h1>Hello World!</h1>
</template>

<script></script>
<style></style>
```

"App.vue" faylini saqlang, terminaldagi localhost havolasiga rioya qilib brauzeringizga o'ting. Natijani ko'ryapsizmi? Brauzer endi VS kodidagi o'zgarishlarni har safar saqlaganingizda brauzerni qo'lda yangilamasdan avtomatik ravishda yangilanishi kerak.

Keling, biroz kattaroq Vue misolini ko'rib chiqaylik:

{% code title="App.vue:" %}
```html
<template>
  <h1>{{ message }}</h1>
</template>

<script>
export default {
  data() {
    return {
      message: 'This is some text'
    };
  }
};
</script>

<style></style>
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Yuqoridagi misolda "main.js" ga ma'lumotlarni "index.html" ichidagi tegga o'rnatilishi uchun `export default`ushlash imkonini beradi .`import App from './App.vue'<div id="app">`
{% endhint %}
