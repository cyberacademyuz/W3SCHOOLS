# Vue Scopped slotlar

{% hint style="success" %}
Scoped **uyasi** komponentdan mahalliy ma'lumotlarni taqdim etadi, shunda ota-ona uni qanday ko'rsatishni tanlashi mumkin.
{% endhint %}

### Ma'lumotlarni ota-onaga yuborish

`v-bind`Mahalliy ma'lumotlarni ota-onaga yuborish uchun komponent uyasida foydalanamiz:

{% code title="SlotComp.vue:" %}
```html
<template>
  <slot v-bind:lclData="data"></slot>
</template>

<script>
  export default {
    data() {
      return {
        data: 'This is local data'
      }
    }
  }
</script>
 
```
{% endcode %}

Komponent ichidagi ma'lumotlarni "mahalliy" deb atash mumkin, chunki ular ota-onaga kirish imkoni yo'q, agar ular bu erda bo'lgani kabi ota-onaga yuborilmasa `v-bind`.

### Scoped Slotdan ma'lumotlarni qabul qilish

Komponentdagi mahalliy ma'lumotlar bilan yuboriladi `v-bind`va uni ota-ona bilan olish mumkin `v-slot`:

<pre class="language-html" data-title="App.vue:"><code class="lang-html"><strong>&#x3C;slot-comp v-slot:"dataFromSlot">
</strong>  &#x3C;h2>{{ dataFromSlot.lclData }}&#x3C;/h2>
&#x3C;/slot-comp>
 
</code></pre>

Yuqoridagi misolda, "dataFromSlot" bu shunchaki ism bo'lib, biz ko'lamli uyasidan olgan ma'lumotlar ob'ektini ko'rsatish uchun o'zimiz tanlashimiz mumkin. Biz "lclData" xususiyatidan foydalanib, matn qatorini slotdan olamiz va matnni tegda yakunlash uchun interpolatsiyadan foydalanamiz `<h2>`.

### Massivga ega bo'lgan Slot

Keng qamrovli slot yordamida massivdan ma'lumotlarni yuborishi mumkin `v-for`, lekin undagi kod `App.vue`asosan bir xil:

<pre class="language-html" data-title="SlotComp.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;slot
    v-for="x in foods"
    :key="x"
<strong>    :foodName="x"
</strong>  >&#x3C;/slot>
&#x3C;/template>

&#x3C;script>
  export default {
    data() {
      return {
        foods: ['Apple','Pizza','Rice','Fish','Cake']
      }
    }
  }
&#x3C;/script>
</code></pre>

<pre class="language-html" data-title="App.vue:"><code class="lang-html"><strong>&#x3C;slot-comp v-slot="food">
</strong>  &#x3C;h2>{{ food.foodName }}&#x3C;/h2>
&#x3C;/slot-comp>
</code></pre>

### Ob'ektlar massiviga ega bo'lgan Slot

Keng qamrovli slot quyidagi yordamida ob'ektlar massividan ma'lumotlarni yuborishi mumkin `v-for`:

<pre class="language-html" data-title="SlotComp.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;slot
    v-for="x in foods"
    :key="x.name"
<strong>    :foodName="x.name"
</strong><strong>    :foodDesc="x.desc"
</strong><strong>    :foodUrl="x.url"
</strong>  >&#x3C;/slot>
&#x3C;/template>

&#x3C;script>
  export default {
    data() {
      return {
        foods: [
          { name: 'Apple', desc: 'Apples are a type of fruit that grow on trees.', url: 'img_apple.svg' },
          { name: 'Pizza', desc: 'Pizza has a bread base with tomato sauce, cheese, and toppings on top.', url: 'img_pizza.svg' },
          { name: 'Rice', desc: 'Rice is a type of grain that people like to eat.', url: 'img_rice.svg' },
          { name: 'Fish', desc: 'Fish is an animal that lives in water.', url: 'img_fish.svg' },
          { name: 'Cake', desc: 'Cake is something sweet that tastes good but is not considered healthy.', url: 'img_cake.svg' }
       ]
      }
    }
  }
&#x3C;/script>
</code></pre>

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;slot-comp v-slot="food">
  &#x3C;hr>
<strong>  &#x3C;h2>{{ food.foodName }}&#x3C;img :src=food.foodUrl>&#x3C;/h2>
</strong><strong>  &#x3C;p>{{ food.foodDesc }}&#x3C;/p>
</strong>&#x3C;/slot-comp>
</code></pre>

### Skoplangan Slotdan statik ma'lumotlar

Ko'lamli slot statik ma'lumotlarni, ya'ni Vue misolining ma'lumotlar xususiyatiga tegishli bo'lmagan ma'lumotlarni ham yuborishi mumkin.

Statik ma'lumotlarni yuborishda biz foydalanmaymiz `v-bind`.

Quyidagi misolda biz farqni ko'rishimiz uchun bitta statik matnni va dinamik ravishda ma'lumotlar misoliga bog'langan bitta matnni yuboramiz.

{% code title="SlotComp.vue:" %}
```html
<template>
  <slot
    staticText="This text is static"
    :dynamicText="text"
  ></slot>
</template>

<script>
  export default {
    data() {
      return {
        text: 'This text is from the data property'
      }
    }
  }
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<slot-comp v-slot="texts">
  <h2>{{ texts.staticText }}</h2>
  <p>{{ texts.dynamicText }}</p>
</slot-comp>
```
{% endcode %}

### Nomlangan Scoped Slots

Qamrovli uyalar nomlanishi mumkin.

Nomlangan ko'lamli slotlardan foydalanish uchun komponent ichidagi slotlarni "name" atributi bilan nomlashimiz kerak.

Nomlangan slotdan ma'lumotlarni olish uchun biz komponentdan foydalanadigan ota-ona nomiga, direktiva `v-slot`yoki stenografiya bilan murojaat qilishimiz kerak `#`.

Ushbu misolda komponent bir marta "leftSlot" uyasiga, bir marta esa "rightSlot" uyasiga qarab yaratilgan.

{% code title="SlotComp.vue:" %}
```html
<template>
  <slot
    name="leftSlot"
    :text="leftText"
  ></slot>
  <slot
    name="rightSlot"
    :text="rightText"
  ></slot>
</template>

<script>
  export default {
    data() {
      return {
        leftText: 'This text belongs to the LEFT slot.',
        rightText: 'This text belongs to the RIGHT slot.'
      }
    }
  }
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<slot-comp #leftSlot="leftProps">
  <div>{{ leftProps.text }}</div>
</slot-comp>
<slot-comp #rightSlot="rightProps">
  <div>{{ rightProps.text }}</div>
</slot-comp>
```
{% endcode %}

Shu bilan bir qatorda, biz komponentni bir marta ikki xil `"template"`teg bilan yaratishimiz mumkin, har bir `"template"`teg boshqa uyaga ishora qiladi.

Ushbu misolda komponent faqat bir marta yaratilgan, lekin ikkita `"template"`teg bilan, har biri boshqa uyaga ishora qiladi.

`SlotComp.vue`oldingi misoldagi kabi bir xil.

{% code title="App.vue:" %}
```html
<slot-comp>

  <template #leftSlot="leftProps">
    <div>{{ leftProps.text }}</div>
  </template>

  <template #rightSlot="rightProps">
    <div>{{ rightProps.text }}</div>
  </template>

</slot-comp>
```
{% endcode %}
