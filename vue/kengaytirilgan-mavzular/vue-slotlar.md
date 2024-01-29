# Vue Slotlar

{% hint style="success" %}
**Slotlar** Vue-da yanada moslashuvchan va qayta foydalanish mumkin bo'lgan qismlarga imkon beruvchi kuchli xususiyatdir.

Biz ota-onadan bola komponentiga kontent yuborish uchun Vue-dagi **slotlardan** foydalanamiz .`<template>`
{% endhint %}

### uyalar

`<template>`Hozirgacha biz tarkibiy qismlarni o'z-o'zidan yopiladigan teglar sifatida ishlatganmiz:

{% code title="App.vue:" %}
```html
<template>
  <slot-comp />
</template> 
```
{% endcode %}

Buning o'rniga biz ochish va yopish teglaridan foydalanishimiz va ichiga ba'zi tarkibni qo'yishimiz mumkin, masalan, matn:

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
<strong>  &#x3C;slot-comp>Hello World!&#x3C;/slot-comp>
</strong>&#x3C;/template>
 
</code></pre>

Lekin "Salom dunyo!" komponent ichida va uni bizning sahifamizda ko'rsatish uchun biz `<slot>`komponent ichidagi tegdan foydalanishimiz kerak. Teg `<slot>`kontent uchun to'ldiruvchi vazifasini bajaradi, shuning uchun dastur yaratilgandan so'ng, `<slot>`unga yuborilgan tarkib bilan almashtiriladi.

<pre class="language-html" data-title="SlotComp.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;div>  
    &#x3C;p>SlotComp.vue&#x3C;/p>
<strong>    &#x3C;slot>&#x3C;/slot>
</strong>  &#x3C;/div>
&#x3C;/template>
</code></pre>

### Kartalar kabi uyalar

Slotlar, shuningdek, kartaga o'xshash ko'rinishga ega bo'lish uchun dinamik HTML tarkibining katta qismlarini o'rash uchun ham ishlatilishi mumkin.

Ilgari biz ma'lumotlarni komponentlar ichida tarkib yaratish uchun rekvizit sifatida yuborgan edik, endi biz HTML tarkibini to'g'ridan-to'g'ri teg ichiga yuborishimiz mumkin `<slot>`.

{% code title="App.vue:" %}
```html
<template>
  <h3>Slots in Vue</h3>  
  <p>We create card-like div boxes from the foods array.</p>
  <div id="wrapper">
    <slot-comp v-for="x in foods">
      <img v-bind:src="x.url">
      <h4>{{x.name}}</h4>
      <p>{{x.desc}}</p>
    </slot-comp>
  </div>
</template>
```
{% endcode %}

Kontent bo'lgan komponentga kirganda , biz ilovamizdagi boshqa divlarga ta'sir qilmasdan, kontent atrofida kartaga o'xshash ko'rinish yaratish uchun `<slot>`uning atrofida div-dan foydalanamiz `<slot>`va uni mahalliy tarzda stillaymiz .`<div>`

{% code title="SlotComp.vue:" %}
```html
<template>
  <div> <!-- This div makes the card-like appearance -->
    <slot></slot>
  </div>
</template>

<script></script>

<style scoped>
  div {
    box-shadow: 0 4px 8px 0 rgba(0,0,0,0.2);
    border-radius: 10px;
    margin: 10px;
  }
</style>
```
{% endcode %}

Kontent atrofida kartaga o'xshash ramka hosil qiluvchi komponentlar turli elementlarni yaratish uchun qayta ishlatilishi mumkin, lekin atrofida bir xil kartaga o'xshash ramka bilan.

Ushbu misolda biz altbilgi yaratish uchun oziq-ovqat mahsulotlari bilan bir xil komponentdan foydalanamiz.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h3>Reusable Slot Cards&#x3C;/h3>
  &#x3C;p>We create card-like div boxes from the foods array.&#x3C;/p>
  &#x3C;p>We also create a card-like footer by reusing the same component.&#x3C;/p>
  &#x3C;div id="wrapper">
    &#x3C;slot-comp v-for="x in foods">
      &#x3C;img v-bind:src="x.url">
      &#x3C;h4>{{x.name}}&#x3C;/h4>
    &#x3C;/slot-comp>
  &#x3C;/div>
<strong>  &#x3C;footer>
</strong><strong>    &#x3C;slot-comp>
</strong><strong>      &#x3C;h4>Footer&#x3C;/h4>
</strong><strong>    &#x3C;/slot-comp>
</strong><strong>  &#x3C;/footer>
</strong>&#x3C;/template>
</code></pre>

### zaxira tarkib

Agar komponent tarkibsiz yaratilgan bo'lsa, bizda zaxira kontent bo'lishi mumkin `<slot>`.

Ushbu ilovaning birinchi komponentida hech qanday tarkib mavjud emas, shuning uchun zaxira kontent taqdim etiladi.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h3>Slots Fallback Content&#x3C;/h3>
  &#x3C;p>A component without content provided can have fallback content in the slot tag.&#x3C;/p>
  &#x3C;slot-comp>
<strong>    &#x3C;!-- Empty -->
</strong>  &#x3C;/slot-comp>
  &#x3C;slot-comp>
    &#x3C;h4>This content is provided from App.vue&#x3C;/h4>
  &#x3C;/slot-comp>
&#x3C;/template>
</code></pre>

{% code title="SlotComp.vue:" %}
```html
<template>
  <div>
    <slot>
      <h4>This is fallback content</h4>
    </slot>
  </div>
</template>
```
{% endcode %}
