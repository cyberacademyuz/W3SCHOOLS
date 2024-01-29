# Vue Lokal komponentlar

{% hint style="success" %}
Biz hozirgacha komponentlarni kiritganimiz ularni `*.vue`loyihadagi barcha fayllardan foydalanish imkonini beradi.

**Komponentlar mahalliy bo'lishi mumkin** , ya'ni ularga faqat ma'lum bir `*.vue`fayl ichida kirish mumkin.
{% endhint %}

### Global komponentlar

Komponentlarni shu paytgacha ichiga kiritganimiz ushbu loyihadagi barcha boshqa fayllar `main.js`ichida komponentlarga kirish imkonini beradi .`<template>*.vue`

Biz `CompOne.vue`komponentni ikkalasining ichida ishlatamiz `CompTwo.vue`va `App.vue`mavjud sozlamalarimiz bilan komponentlar bir-biriga kirish mumkinligini ko'rsatish uchun foydalanamiz `main.js`.

{% code title="main.js:" %}
```js
import { createApp } from 'vue'
 
import App from './App.vue'
import CompOne from './components/CompOne.vue'
import CompTwo from './components/CompTwo.vue'

const app = createApp(App)
app.component('comp-one', CompOne)
app.component('comp-two', CompTwo)
app.mount('#app')
```
{% endcode %}

### Mahalliy komponentlar

Biz komponentni faylga kiritish o'rniga to'g'ridan-to'g'ri tegga `<script>`kiritishimiz `*.vue`mumkin `main.js`.

Agar komponentni to'g'ridan-to'g'ri faylga qo'shsak `*.vue`, komponent faqat shu faylda mahalliy sifatida foydalanish mumkin bo'ladi.

`CompOne.vue`ga mahalliy `App.vue`va faqat u yerda kirish mumkin qilish uchun biz uni dan olib tashlaymiz `main.js.`

{% code title="main.js:" %}
```js
import { createApp } from 'vue'

import App from './App.vue'
import CompOne from './components/CompOne.vue' 
import CompTwo from './components/CompTwo.vue'
 
const app = createApp(App)
app.component('comp-one', CompOne) 
app.component('comp-two', CompTwo)
app.mount('#app')
```
{% endcode %}

Va uning o'rniga `CompOne.vue`to'g'ridan-to'g'ri tegga qo'shing .`<script>App.vue`

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h3>Local Component&#x3C;/h3>
  &#x3C;p>The CompOne.vue component is a local component and can only be used inside App.vue.&#x3C;/p>
  &#x3C;comp-one />
  &#x3C;comp-two />
&#x3C;/template>

&#x3C;script> 
<strong>  import CompOne from './components/CompOne.vue';
</strong>
<strong>  export default {
</strong><strong>    components: {
</strong><strong>      'comp-one': CompOne
</strong><strong>    }
</strong><strong>  }
</strong>&#x3C;/script> 
</code></pre>

Komponent `CompOne.vue`endi faqat ichida mavjud `App.vue`.

Agar siz dasturni ishlab chiqish rejimida ishga tushirsangiz va `CompOne.vue`ichkaridan foydalanishga harakat qilsangiz `CompTwo.vue`, siz ogohlantirish olasiz:

<figure><img src="https://www.w3schools.com/vue/img_localComp_warn2.png" alt=""><figcaption></figcaption></figure>
