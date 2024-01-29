# Vue v-on

{% hint style="success" %}
Oddiy JavaScript-da hodisalarni boshqarish kabi, `v-on`Vue-dagi direktiva brauzerga aytadi:

1. qaysi hodisani tinglash kerak ("klik", "tugmachani pastga tushirish", "sichqonchani bosish" va boshqalar)
2. bu voqea sodir bo'lganda nima qilish kerak
{% endhint %}

### Foydalanishga misollar`v-on`

Keling, turli hodisalar va bu hodisalar sodir bo'lganda ishga tushirish uchun turli kodlar bilan qanday foydalanish mumkinligini ko'rish uchun ba'zi misollarni ko'rib chiqaylik `v-on`.

{% hint style="warning" %}
**Eslatma:** Voqea sodir bo'lganda yanada rivojlangan kodni ishga tushirish uchun Vue usullarini joriy qilishimiz kerak. Ushbu qo'llanmaning keyingi sahifasida Vue usullari haqida bilib oling.
{% endhint %}

### onclick hodisasi

v-on direktivasi bizga ko'rsatilgan hodisalarga asoslangan harakatlarni bajarishga imkon beradi.

`v-on:click`Element bosilganda amalni bajarish uchun foydalaning.

Direktiv `v-on`\<button> tegida 'click' hodisasini tinglash uchun ishlatiladi. "Click" hodisasi sodir bo'lganda, "lightOn" ma'lumotlar xususiyati "to'g'ri" va "noto'g'ri" o'rtasida almashtiriladi va lampochka orqasidagi sariq \<div> ko'rinadigan/yashirin bo'ladi.

```
<div id="app">
  <div id="lightDiv">
    <div v-show="lightOn"></div>
    <img src="img_lightBulb.svg">
  </div>
  <button v-on:click="lightOn = !lightOn">Switch light</button>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        lightOn: false
      }
    }
  })
  app.mount('#app')
</script>
```

### oninput hodisasi

`v-on:input`Element matn maydoni ichidagi tugmani bosish kabi kiritishni olganida amalni bajarish uchun foydalaning .

{% code title="Matn kiritish maydoni uchun tugmalar sonini hisoblang:" %}
```
<div id="app">
  <input v-on:input="inpCount++">
  <p>{{ 'Input events occured: ' + inpCount }}</p>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        inpCount: 0
      }
    }
  })
  app.mount('#app')
</script>
```
{% endcode %}

### sichqonchani siljitish hodisasi

`v-on:mousemove`Sichqoncha ko‘rsatkichi element ustida harakat qilganda amalni bajarish uchun foydalaning .

{% code title="Sichqoncha ko'rsatkichi har safar harakatlansa, <div> elementining fon rangini o'zgartiring:" %}
```
<div id="app">
  <p>Move the mouse pointer over the box below</p>
  <div v-on:mousemove="colorVal=Math.floor(Math.random()*360)"
       v-bind:style="{backgroundColor:'hsl('+colorVal+',80%,80%)'}">
  </div>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        colorVal: 50
      }
    }
  })
  app.mount('#app')
</script>
```
{% endcode %}

### v-for tsiklida v-on-dan foydalaning

Siz `v-on`direktivani tsikl ichida ham ishlatishingiz mumkin `v-for`.

Massiv elementlari qiymat ichidagi har bir iteratsiya uchun mavjud `v-on`.

Oziq-ovqat massiviga asoslangan ro'yxatni ko'rsating va tasvir manbasini o'zgartirish uchun massiv elementidagi qiymatdan foydalanadigan har bir element uchun bosish hodisasini qo'shing.

```
<div id="app">
  <img v-bind:src="imgUrl">
  <ol>
    <li v-for="food in manyFoods" v-on:click="imgUrl=food.url">
      {{ food.name }}
    </li>
  </ol>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        imgUrl: 'img_salad.svg',
        manyFoods: [
          {name: 'Burrito', url: 'img_burrito.svg'},
          {name: 'Salad', url: 'img_salad.svg'},
          {name: 'Cake', url: 'img_cake.svg'},
          {name: 'Soup', url: 'img_soup.svg'}
        ]
      }
    }
  })
  app.mount('#app')
</script>
```

### uchun qisqa qo'l`v-on`

'' stenografiyasi `v-on`oddiygina ' `@`'.\\

`@`Bu erda biz ' ' o'rniga ' ' yozamiz `v-on`:

```
<button @:click="lightOn = !lightOn">Switch light</button>
```

`@`Ushbu qo'llanmada biz sintaksisdan biroz keyinroq foydalanishni boshlaymiz .
