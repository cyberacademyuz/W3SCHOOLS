# Vue Scoped styling

{% hint style="success" %}
`<style>`Komponentdagi teg ichida yoki ichida belgilangan uslublar `App.vue`aslida barcha komponentlarda global miqyosda mavjud.

Stylingni mahalliy ravishda faqat komponent bilan cheklash uchun biz `scope`ushbu komponentdagi atributdan foydalanishimiz mumkin:**`<style scoped>`**
{% endhint %}

### Global uslub

`<style>`Har qanday fayldagi teg ichida yozilgan CSS `*.vue`global miqyosda ishlaydi.

Bu shuni anglatadiki, agar biz, masalan, bitta fayldagi teg `<p>`ichida pushti fon rangi bo'lgan teglarni o'rnatsak, bu loyihadagi barcha fayllardagi teglarga ta'sir qiladi .`<style>*.vue<p>*.vue`

Ushbu ilovada bizda uchta `*.vue`fayl mavjud: `App.vue`, va ikkita komponent `CompOne.vue`va `CompTwo.vue`.

Ichki CSS uslubi barcha uchta fayldagi teglarga `CompOne.vue`ta'sir qiladi :`<p>*.vue`

```html
<template>
  <p>This p-tag belongs to 'CompOne.vue'</p>
</template>

<script></script>

<style>
  p {
    background-color: pink;
    width: 150px;
  }
</style>
```

### Keng qamrovli uslublar

Bitta komponentdagi uslublar boshqa komponentlardagi elementlarning uslubiga ta'sir qilmasligi uchun tegda "ko'lamli" atributidan foydalanamiz `<style>:`

`<style>`In tegiga atribut `CompOne.vue`beriladi `scoped`:

<pre class="language-html"><code class="lang-html">&#x3C;template>
  &#x3C;p>This p-tag belongs to 'CompOne.vue'&#x3C;/p>
&#x3C;/template>

&#x3C;script>&#x3C;/script>

<strong>&#x3C;style scoped>
</strong>  p {
    background-color: pink;
    width: 150px;
  }
&#x3C;/style>
</code></pre>
