# Vue Fallthrough attributlar

{% hint style="success" %}
Komponentni rekvizit sifatida e'lon qilinmagan atributlar bilan chaqirish mumkin va ular shunchaki komponentdagi ildiz elementiga **tushadi .**

**Favqulodda atributlar** yordamida siz komponent yaratilgan ota-onadan yaxshiroq ko'rinishga ega bo'lasiz va bu bizning kodimizni soddalashtiradi, chunki atributni rekvizit sifatida e'lon qilishimiz shart emas.

O'tish uchun ishlatiladigan tipik atributlar `class`, `style`va `v-on`.
{% endhint %}

### Fallthrough atributlari

Masalan, uslubni komponent ichida yashirgandan ko'ra, komponent uslubini ota-onadan boshqarish yaxshi bo'lishi mumkin.

Keling, Vue-da yangi misol, asosiy vazifalar ro'yxatini yaratamiz va uslub atributi qilinadigan ishlarni ifodalovchi komponentlarga qanday tushishini ko'rib chiqamiz.

Shunday qilib, bizda `App.vue`qilinadigan ishlar ro'yxati va yangi narsalarni qo'shish uchun `<input>`element va a bo'lishi kerak. `<button>`Har bir ro'yxat elementi `<todo-item />`komponent hisoblanadi.

{% code title="App.vue:" %}
```html
<template>
  <h3>Todo List</h3>  
  <ul>
    <todo-item
      v-for="x in items"
      :key="x"
      :item-name="x"
    />
  </ul>
  <input v-model="newItem">
  <button @click="addItem">Add</button>
</template>

<script>
  export default {
    data() {
      return {
        newItem: '',
        items: ['Buy apples','Make pizza','Mow the lawn']
      };
    },
    methods: {
      addItem() {
        this.items.push(this.newItem),
        this.newItem = '';
      }
    }
  }
</script>
```
{% endcode %}

Va `TodoItem.vue`shunchaki rekvizit sifatida nima qilish kerakligi tavsifini oladi:

{% code title="TodoItem.vue:" %}
```html
<template>
  <li>{{ itemName }}</li>
</template>

<script>
  export default {
    props: ['itemName']
  }
</script>
```
{% endcode %}

Ilovamizni to'g'ri yaratish uchun bizga to'g'ri sozlash ham kerak `main.js`:

{% code title="main.js:" %}
```js
import { createApp } from 'vue'
  
import App from './App.vue'
import TodoItem from './components/TodoItem.vue'

const app = createApp(App)
app.component('todo-item', TodoItem)
app.mount('#app')
 
 
```
{% endcode %}

Ushbu bo'limning mohiyatini ko'rish uchun xususiyatlar bizning komponentimiz ichidagi ildiz elementiga tushishi mumkin `<template>`, biz ro'yxat elementlariga quyidagi uslublarni berishimiz mumkin `App.vue`:

`<li>`Biz komponent ichidagi elementlarga uslubni beramiz , dan `App.vue`:

<pre class="language-html"><code class="lang-html">&#x3C;template>
  &#x3C;h3>Todo List&#x3C;/h3>
  &#x3C;ul>
    &#x3C;todo-item
      v-for="x in items"
      :key="x"
      :item-name="x"
<strong>      style="background-color: lightgreen;"
</strong>    />
  &#x3C;/ul>
  &#x3C;input v-model="newItem">
  &#x3C;button @click="addItem">Add&#x3C;/button>
&#x3C;/template>
 
</code></pre>

**Uslub atributi haqiqatdan ham buzilganligini tasdiqlash uchun**`<li>` brauzerda vazifalar ro‘yxatidagi elementni o‘ng tugmasini bosib , “Tekshirish” ni tanlab, uslub atributi hozir elementda ekanligini ko‘rishimiz mumkin `<li>`:

![](https://www.w3schools.com/vue/img\_li-fallthru.png)

### "Sinf" va "uslub" atributlarini birlashtirish

Agar "sinf" yoki "uslub" atributlari allaqachon o'rnatilgan bo'lsa va "sinf" yoki "uslub" atributlari ham asosiy atributlardan kelib chiqsa, atributlar birlashtiriladi.

`<li>`Ota-onadan mavjud uslubga qo'shimcha ravishda, biz komponent ichidagi elementlarga chekka qo'shamiz `TodoItem.vue`:

<pre class="language-html"><code class="lang-html">&#x3C;template>
<strong>  &#x3C;li style="margin: 5px 0;">{{ itemName }}&#x3C;/li>
</strong>&#x3C;/template>

&#x3C;script>
  export default {
    props: ['itemName']
  }
&#x3C;/script>
 
</code></pre>

Agar biz brauzerda elementni o'ng tugmasini bossak, `<li>`atributlar birlashtirilganligini ko'rishimiz mumkin. Marja to'g'ridan-to'g'ri komponent ichidagi elementga o'rnatiladi `<li>`va ota-onadan tushadigan fon rangi bilan birlashtiriladi:

![](https://www.w3schools.com/vue/img\_li-fallthru-merge.png)

***

### $attrs

Agar komponentning ildiz darajasida bir nechta element mavjud bo'lsa, atributlar qaysi elementga to'g'ri kelishi aniq bo'lmaydi.

Qaysi ildiz elementi asosiy atributlarni olishini aniqlash uchun biz elementni o'rnatilgan `$attrs`ob'ekt bilan belgilashimiz mumkin, masalan:

<pre class="language-html" data-title="TodoItem.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;div class="pinkBall">&#x3C;/div>
<strong>  &#x3C;li v-bind="$attrs">{{ itemName }}&#x3C;/li>
</strong>  &#x3C;div class="pinkBall">&#x3C;/div>
&#x3C;/template>
</code></pre>
