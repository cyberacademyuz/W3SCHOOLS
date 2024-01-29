# Vue v-slot

{% hint style="success" %}
**Nomlangan uyalarga`v-slot`** murojaat qilish uchun bizga direktiv kerak .

**Nomlangan slotlar** kontentning bola komponenti shablonida qayerga joylashtirilishini ko'proq nazorat qilish imkonini beradi.

**Nomlangan uyalar** yanada moslashuvchan va qayta foydalanish mumkin bo'lgan komponentlarni yaratish uchun ishlatilishi mumkin.
{% endhint %}

Slotlarni ishlatishdan `v-slot`va nomlanishidan oldin, komponentda ikkita slotdan foydalansak nima bo'lishini ko'rib chiqamiz:

{% code title="App.vue:" %}
```html
<h1>App.vue</h1>
<p>The component has two div tags with one slot in each.</p>
<slot-comp>'Hello!'</slot-comp>
```
{% endcode %}

`SlotComp.vue`:

```html
<h3>Component</h3>
<div>
  <slot></slot>
</div>
<div>
  <slot></slot>
</div>
```

Komponentdagi ikkita uyasi bilan kontent oddiygina ikkala joyda ham paydo bo'lishini ko'rishimiz mumkin.

### v-uyasi va nomlangan uyalar

Agar bizda bir nechta komponent mavjud bo'lsa , lekin biz qaysi tarkibda ko'rinishini `<slot>`nazorat qilmoqchi bo'lsak , biz slotlarni nomlashimiz va tarkibni kerakli joyga yuborish uchun foydalanishimiz kerak.`<slot>v-slot`

Slotlarni farqlash uchun biz uyalarga turli nomlar beramiz.

<pre class="language-html" data-title="SlotComp.vue:"><code class="lang-html">&#x3C;h3>Component&#x3C;/h3>
&#x3C;div>
<strong>  &#x3C;slot name="topSlot">&#x3C;/slot>
</strong>&#x3C;/div>
&#x3C;div>
<strong>  &#x3C;slot name="bottomSlot">&#x3C;/slot>
</strong>&#x3C;/div>
 
 
</code></pre>

Va endi biz `v-slot`undan `App.vue`tarkibni to'g'ri uyaga yo'naltirish uchun foydalanishimiz mumkin.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;h1>App.vue&#x3C;/h1>
&#x3C;p>The component has two div tags with one slot in each.&#x3C;/p>
<strong>&#x3C;slot-comp v-slot:bottomSlot>'Hello!'&#x3C;/slot-comp>
</strong></code></pre>

### Standart uyasi

Agar sizda `<slot>`nomsiz bo'lsa, bu bilan belgilangan komponentlar yoki bilan belgilanmagan komponentlar `<slot>`uchun birlamchi bo'ladi .`v-slot:defaultv-slot`

Bu qanday ishlashini ko'rish uchun biz avvalgi misolimizda ikkita kichik o'zgartirish kiritishimiz kerak:

{% code title="SlotComp.vue:" %}
```html
<h3>Component</h3>
<div>
  <slot name="topSlot"></slot>
</div>
<div>
  <slot name="bottomSlot"></slot>
</div>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<h1>App.vue</h1>
<p>The component has two div tags with one slot in each.</p>
<slot-comp v-slot:bottomSlot>'Hello!'</slot-comp>
 
```
{% endcode %}

`v-slot:default`Yuqorida aytib o'tganimizdek, kontentning standart slotga tegishli ekanligini yanada aniqroq qilish uchun kontentni standart qiymat bilan belgilashimiz mumkin .

{% code title="SlotComp.vue:" %}
```html
<h3>Component</h3>
<div>
  <slot></slot>
</div>
<div>
  <slot name="bottomSlot"></slot>
</div>
```
{% endcode %}

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;h1>App.vue&#x3C;/h1>
&#x3C;p>The component has two div tags with one slot in each.&#x3C;/p>
<strong>&#x3C;slot-comp v-slot:default>'Default slot'&#x3C;/slot-comp>
</strong> 
</code></pre>

### v uyasi \<template>

Ko'rib turganingizdek, `v-slot`direktiv komponent tegida atribut sifatida ishlatilishi mumkin.

`v-slot<template>`kontentning katta qismlarini ma'lum bir joyga yo'naltirish uchun tegda ham foydalanish mumkin `<slot>`.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;h1>App.vue&#x3C;/h1>
&#x3C;p>The component has two div tags with one slot in each.&#x3C;/p>
&#x3C;slot-comp>
<strong>  &#x3C;template v-slot:bottomSlot>
</strong>    &#x3C;h4>To the bottom slot!&#x3C;/h4>
    &#x3C;p>This p tag and the h4 tag above are directed to the bottom slot with the v-slot directive used on the template tag.&#x3C;/p>
  &#x3C;/template>
  &#x3C;p>This goes into the default slot&#x3C;/p>
&#x3C;/slot-comp>
</code></pre>

{% code title="SlotComp.vue:" %}
```html
<h3>Component</h3>
<div>
  <slot></slot>
</div>
<div>
  <slot name="bottomSlot"></slot>
</div>
```
{% endcode %}

Biz `<template>`tegdan ba'zi tarkibni ma'lum biriga yo'naltirish uchun foydalanamiz `<slot>`, chunki `<template>`teg ko'rsatilmaydi, u faqat kontent uchun joy ushlagichdir. Buni qurilgan sahifani tekshirish orqali ko'rishingiz mumkin: u erda shablon tegini topa olmaysiz.

### v-slot stenografiya \#

`v-slot:`ning qisqartmasi `#`.

Bu shuni anglatadiki:

<pre class="language-html"><code class="lang-html"><strong>&#x3C;slot-comp v-slot:topSlot>'Hello!'&#x3C;/slot-comp>
</strong></code></pre>

Quyidagi kabi yozilishi mumkin:

<pre class="language-html"><code class="lang-html"><strong>&#x3C;slot-comp #topSlot>'Hello!'&#x3C;/slot-comp>
</strong></code></pre>

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;h1>App.vue&#x3C;/h1>
&#x3C;p>The component has two div tags with one slot in each.&#x3C;/p>
<strong>&#x3C;slot-comp #topSlot>'Hello!'&#x3C;/slot-comp>
</strong></code></pre>

{% code title="SlotComp.vue:" %}
```html
<h3>Component</h3>
<div>
  <slot name="topSlot"></slot>
</div>
<div>
  <slot name="bottomSlot"></slot>
</div>
```
{% endcode %}
