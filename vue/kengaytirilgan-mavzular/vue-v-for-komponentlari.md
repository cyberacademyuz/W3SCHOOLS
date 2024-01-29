# Vue v-for komponentlari

{% hint style="success" %}
`v-for`Komponentlardan bir xil turdagi ko'plab elementlarni yaratish uchun qayta foydalanish mumkin .

Komponentdan elementlarni yaratishda `v-for`rekvizitlarni massivdagi qiymatlar asosida dinamik ravishda tayinlash ham juda foydali.
{% endhint %}

### v-for bilan komponent elementlarini yarating

`v-for`Endi biz oziq-ovqat mahsuloti nomlari bilan massiv asosida komponent elementlarini yaratamiz.

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <p>Components created with v-for based on an array.</p>
  <div id="wrapper">
    <food-item
      v-for="x in foods"
      v-bind:food-name="x"/>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        foods: ['Apples','Pizza','Rice','Fish','Cake']
      };
    }
  }
</script>
```
{% endcode %}

{% code title="FoodItem.vue:" %}
```html
<template>
  <div>
    <h2>{{ foodName }}</h2>
  </div>
</template>

<script>
  export default {
    props: ['foodName']
  }
</script>
```
{% endcode %}

### v-bog'lash stenografiyasi

Rekvizitlarni dinamik ravishda bog'lash uchun biz dan foydalanamiz va biz avvalgidan ko'ra ko'proq `v-bind`foydalanamiz, chunki biz ushbu qo'llanmaning qolgan qismida stenografiyadan foydalanamiz.`v-bindv-bind::`

### "Kalit" tayanchi

Elementlar bilan yaratilgandan keyin massivni o'zgartirsak `v-for`, Vue bilan yaratilgan bunday elementlarni yangilash usuli tufayli xatolar paydo bo'lishi mumkin `v-for`. Vue unumdorlikni optimallashtirish uchun elementlardan qayta foydalanadi, shuning uchun biror elementni olib tashlasak, barcha elementlarni qayta yaratish o‘rniga allaqachon mavjud elementlar qayta ishlatiladi va element xususiyatlari endi to‘g‘ri kelmasligi mumkin.

Elementlarning noto'g'ri qayta ishlatilishining sababi shundaki, elementlarning noyob identifikatori yo'qligi va biz kalit tayanchdan aynan shu maqsadda foydalanamiz: Vue-ga elementlarni bir-biridan ajratib turishiga imkon berish uchun.

`v-for`Biz kalit tayanchsiz noto'g'ri xatti-harakatlarni yaratamiz, lekin birinchi navbatda ko'rsatish uchun ishlatiladigan oziq-ovqatlar bilan veb-sahifa yarataylik : taom nomi, tavsifi, sevimli taom uchun rasm va sevimli holatni o'zgartirish tugmasi.

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <p>Food items are generated with v-for from the 'foods' array.</p>
  <div id="wrapper">
    <food-item
      v-for="x in foods"
      :food-name="x.name"
      :food-desc="x.desc"
      :is-favorite="x.favorite"/>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        foods: [
          { name: 'Apples',
            desc: 'Apples are a type of fruit that grow on trees.',
            favorite: true },
          { name: 'Pizza',
            desc: 'Pizza has a bread base with tomato sauce, cheese, and toppings on top.',
            favorite: false },
          { name: 'Rice',
            desc: 'Rice is a type of grain that people like to eat.',
            favorite: false }
          { name: 'Fish',
            desc: 'Fish is an animal that lives in water.',
            favorite: true }
          { name: 'Cake',
            desc: 'Cake is something sweet that tastes good.',
            favorite: false }
        ]
      };
    }
  }
</script>

<style>
  #wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #wrapper > div {
    border: dashed black 1px;
    flex-basis: 120px;
    margin: 10px;
    padding: 10px;
    background-color: lightgreen;
  }
</style>
```
{% endcode %}

{% code title="FoodItem.vue:" %}
```html
<template>
  <div>
    <h2>
      {{ foodName }}
      <img src="/img_quality.svg" v-show="foodIsFavorite">
    </h2>
    <p>{{ foodDesc }}</p>
    <button v-on:click="toggleFavorite">Favorite</button>
  </div>
</template>

<script>
  export default {
    props: ['foodName','foodDesc','isFavorite'],
    data() {
      return {
        foodIsFavorite: this.isFavorite
      }
    },
    methods: {
      toggleFavorite() {
        this.foodIsFavorite = !this.foodIsFavorite;
      }
    }
  }
</script>

<style>
  img {
    height: 1.5em;
    float: right;
  }
</style>
```
{% endcode %}

Bizga kalit tayanchi kerakligini ko'rish uchun massivdagi ikkinchi elementni olib tashlaydigan tugma yarataylik. Bu sodir bo'lganda, kalit tayanchsiz, sevimli tasvir "Baliq" elementidan "Cake" elementiga o'tkaziladi va bu to'g'ri EMAS:

Oldingi misoldan yagona farq shundaki, biz tugmachani qo'shamiz:

```html
<button @click="removeItem">Remove Item</button>
```

va usul:

```js
methods: {
  removeItem() {
    this.foods.splice(1,1);
  }
}
```

ichida `App.vue`.

Yuqorida aytib o'tilganidek: element olib tashlanganida sevimli tasvirning "baliq" dan "tort" ga o'zgarishi bu xato Vue elementlarni qayta ishlatish orqali sahifani optimallashtirish bilan bog'liq va shu bilan birga Vue elementlarni bir-biridan to'liq ajrata olmaydi. . Shuning uchun elementlarni yaratishda har bir elementni alohida belgilash uchun har doim kalit tayanchni kiritishimiz kerak `v-for`. Kalit tayanchdan foydalanganda, biz endi bu muammoga duch kelmaymiz.

Biz massiv elementi indeksini asosiy prop qiymati sifatida ishlatmaymiz, chunki massiv elementlari olib tashlanganida va qo'shilganda u o'zgaradi. Biz har bir element uchun ID raqami kabi noyob qiymatni saqlab qolish uchun yangi maʼlumotlar xususiyatini yaratishimiz mumkin, ammo oziq-ovqat mahsulotlari allaqachon noyob nomlarga ega boʻlgani uchun biz undan foydalanishimiz mumkin:

`App.vue`Yaratilgan har bir elementni alohida aniqlash `v-for`va muammoni hal qilish uchun biz faqat bitta qatorni qo'shishimiz kerak :

```html
<food-item
  v-for="x in foods"
  :key="x.name"
  :food-name="x.name"
  :food-desc="x.desc"
  :is-favorite="x.favorite"
/>
```
