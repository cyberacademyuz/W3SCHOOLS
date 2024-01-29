# Vue Propslar

{% hint style="success" %}
**Props** - bu Vue-dagi konfiguratsiya opsiyasi.

Rekvizitlar yordamida biz komponent yorlig'iga maxsus atributlar orqali ma'lumotlarni komponentlarga o'tkazishimiz mumkin.
{% endhint %}

### Komponentga ma'lumotlarni uzatish

Oldingi sahifadagi barcha uchta komponentda "Olma" deb yozilgan misolni eslaysizmi? Endi rekvizitlar yordamida biz ma'lumotlarni komponentlarimizga turli xil tarkib berish va ularni boshqacha ko'rinishga keltirishimiz mumkin.

Keling, "Olma", "Pitsa" va "Guruch" ni ko'rsatish uchun oddiy sahifa yarataylik.

Asosiy dastur faylida komponent teglari `App.vue`bilan rekvizitni uzatish uchun o'zimizning "food-name" atributini yaratamiz `<food-item/>:`

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <food-item food-name="Apples"/>
  <food-item food-name="Pizza"/>
  <food-item food-name="Rice"/>
</template>

<script></script>

<style>
  #app > div {
    border: dashed black 1px;
    display: inline-block;
    width: 120px;
    margin: 10px;
    padding: 10px;
    background-color: lightgreen;
  }
</style>
```
{% endcode %}

### Komponent ichidagi ma'lumotlarni qabul qilish

"Oziq-ovqat mahsuloti" atributi orqali yuborilgan ma'lumotlarni olish uchun `App.vue`biz ushbu yangi "rekvizit" konfiguratsiya opsiyasidan foydalanamiz. Biz olingan atributlarni sanab o'tamiz, shunda komponentimiz \*.vue faylimiz ular haqida biladi va endi biz ma'lumotlar xususiyatidan foydalanganimiz kabi rekvizitlarni xohlagan joyda ishlatishimiz mumkin.

{% code title="FoodItem.vue:" %}
```html
<script>
  export default {
    props: [
      'foodName'
    ]
  }
</script> 
```
{% endcode %}

{% hint style="success" %}
Props atributlari tegda so'zlarni ajratish uchun chiziqcha bilan yoziladi `-`(kabob-xo'jayin) `<template>`, lekin JavaScript-da kabob-rejissor qonuniy emas. Buning o'rniga biz atribut nomlarini JavaScript-da camelCase sifatida yozishimiz kerak va Vue buni avtomatik ravishda tushunadi!
{% endhint %}

Nihoyat, "Olma", "Pitsa" va "Guruch" elementlari bilan bizning misolimiz `<div>`quyidagicha ko'rinadi:

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <food-item food-name="Apples"/>
  <food-item food-name="Pizza"/>
  <food-item food-name="Rice"/>
</template>
```
{% endcode %}

<pre class="language-html" data-title="FoodItem.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;div>
<strong>    &#x3C;h2>{{ foodName }}&#x3C;/h2>
</strong>  &#x3C;/div>
&#x3C;/template>

&#x3C;script>
  export default {
    props: [
<strong>      'foodName'
</strong>    ]
  }
&#x3C;/script>

&#x3C;style>&#x3C;/style>
</code></pre>

Tez orada biz turli xil ma'lumotlar turlarini komponentlarga rekvizit atributlari sifatida qanday o'tkazishni ko'rib chiqamiz, lekin buni qilishdan oldin, keling, har bir oziq-ovqat turining tavsifi bilan kodimizni kengaytiramiz va oziq-ovqat elementlarini Flexbox o'ramiga joylashtiramiz `<div>`.

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <div id="wrapper">
    <food-item
      food-name="Apples"
      food-desc="Apples are a type of fruit that grow on trees."/>
    <food-item
      food-name="Pizza"
      food-desc="Pizza has a bread base with tomato sauce, cheese, and toppings on top."/>
    <food-item
      food-name="Rice"
      food-desc="Rice is a type of grain that people like to eat."/>
  </div>
</template>

<script></script>

<style>
  #wrapper {
    display: flex;
    flex-wrap: wrap;
  }
  #wrapper > div {
    border: dashed black 1px;
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
    <h2>{{ foodName }}</h2>
    <p>{{ foodDesc }}</p>
  </div>
</template>

<script>
  export default {
    props: [
      'foodName',
      'foodDesc'
    ]
  }
</script>

<style></style>
```
{% endcode %}

### Mantiqiy rekvizitlar

Biz turli xil ma'lumotlar turlarining rekvizitlarini uzatish orqali turli funktsiyalarga erishishimiz mumkin va komponentlar dan yaratilganda atributlar qanday berilishi qoidalarini belgilashimiz mumkin `App.vue`.

Keling, yangi "isFavorite" rekvizitini qo'shamiz. Bu qiymatga ega mantiqiy rekvizit bo'lishi kerak `true`yoki oziq-ovqat sevimli deb hisoblansa, uni to'g'ridan-to'g'ri sevimli shtamp yorlig'ini ko'rsatish uchun `false`ishlatishimiz mumkin .`v-show<img>`

`v-bind:`Stringdan farqli maʼlumotlar turiga ega rekvizitlarni oʻtkazish uchun biz uzatmoqchi boʻlgan atributning oldiga yozishimiz kerak .

`App.vue`Biz mantiqiy "isFavorite" rekvizitini "is-favorite" atributi sifatida shunday o'tkazamiz:

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <p>My favorite food has a diploma image attached to it.</p>
  <div id="wrapper">
    <food-item
      food-name="Apples"
      food-desc="Apples are a type of fruit that grow on trees."
      v-bind:is-favorite="true"/>
    <food-item
      food-name="Pizza"
      food-desc="Pizza has a bread base with tomato sauce, cheese, and toppings on top."
      v-bind:is-favorite="false"/>
    <food-item
      food-name="Rice"
      food-desc="Rice is a type of grain that people like to eat."
      v-bind:is-favorite="false"/>
  </div>
</template>
```
{% endcode %}

Biz mantiqiy "isFavorite" rekvizitini olamiz `FoodItem.vue`va agar taom sevimli deb hisoblansa, sevimli shtampni ko'rsatamiz:

{% code title="FoodItem.vue:" %}
```html
<template>
  <div>
    <h2>
      {{ foodName }}
      <img src="/img_quality.svg" v-show="isFavorite">
    </h2>
    <p>{{ foodDesc }}</p>
  </div>
</template>

<script>
  export default {
      props: ['foodName','foodDesc','isFavorite']
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

{% hint style="warning" %}
**Tasvirlar:** Yuqoridagi misoldagi rasmni kompyuteringizdagi loyihada mahalliy sifatida ishlashi uchun yuqoridagi misolni oching, rasmni o'ng tugmasini bosing, "Rasmni boshqa saqlash..." ni tanlang va uni loyihangizdagi "ommaviy" papkaga saqlang. .

![](https://www.w3schools.com/vue/img\_save\_img\_as.png) ![](https://www.w3schools.com/vue/img\_image\_path.png)
{% endhint %}

### Prop interfeysi

Yuqoridagi misolda, ichidagi kodga asoslanib `FoodItem.vue`, biz "isFavorite" rekvizitini qabul qilishimizni aniq bila olmaymiz va bu mantiqiy qiymat yoki yo'qligini aniq bila olmaymiz. Bunda bizga yordam berish uchun biz oladigan rekvizitlarning ma'lumotlar turini aniqlashimiz mumkin, biz talab qilinadigan rekvizitlarni o'rnatishimiz mumkin va hatto biz olgan rekvizitlarni tasdiqlash uchun tekshirish funktsiyalarini ham qila olamiz.

Biz oladigan rekvizitlarni aniqlash, agar siz jamoada ishlasangiz, boshqa odamlar uchun hujjat bo'lib xizmat qiladi va agar biz belgilagan qoidalar buzilgan bo'lsa, konsolda ogohlantirishlar beradiy

### Ob'ekt sifatida rekvizitlar

, Biz `FoodItem.vue`massivdagi rekvizitlarni mos yozuvlar sifatida qanday belgilaganimizni izohlaymiz va buning o'rniga ob'ektdagi rekvizitlarni aniqlaymiz. Shuningdek, biz rekvizit nomidan tashqari har bir rekvizitning ma'lumotlar turini aniqlashimiz mumkin, masalan:

{% code title="FoodItem.vue:" %}
```html
<script>
  export default {
    // props: ['foodName','foodDesc','isFavorite']
    props: {
      foodName: String,
      foodDesc: String,
      isFavorite: Boolean
    }
  }
</script>
```
{% endcode %}

Shu tarzda belgilangan rekvizitlar bilan boshqa odamlar ichkariga qarashlari `FoodItem.vue`va komponent nima kutayotganini osongina ko'rishlari mumkin.

Agar komponent asosiy elementdan yaratilgan bo'lsa (bizning holimizda `App.vue`) va noto'g'ri ma'lumotlar turiga ega bo'lgan rekvizit berilsa, konsolda siz quyidagi kabi ogohlantirish olasiz:

![Noto'g'ri ma'lumotlar turidagi prop ogohlantirishining skrinshoti](https://www.w3schools.com/vue/img\_propType.png)

Bunday ogohlantirishlar o'zimizga va boshqalarga komponent qanday foydalanilmasligini bilish va xatoni tuzatishimiz uchun nima noto'g'ri ekanligini aytib berish uchun foydalidir.

### Kerakli rekvizitlar

Vue-ga tayanch zarurligini aytish uchun biz tayanchni ob'ekt sifatida aniqlashimiz kerak. Keling, "foodName" rekvizitini quyidagi tarzda talab qilaylik:

{% code title="FoodItem.vue:" %}
```html
<script>
  export default {
    // props: ['foodName','foodDesc','isFavorite']
    props: {
      foodName: {
        type: String,
        required: true
      },
      foodDesc: String,
      isFavorite: Boolean
    }
  }
</script> 
```
{% endcode %}

Agar komponent asosiy elementdan yaratilgan bo'lsa (bizning holimizda `App.vue`) va kerakli rekvizit aniqlanmagan bo'lsa, siz konsolda quyidagi kabi ogohlantirish olasiz:

![Kerakli tayanch ogohlantirishining skrinshoti](https://www.w3schools.com/vue/img\_propRequired.png)

Bunday ogohlantirishlar o'zimizga va boshqalarga komponent qanday foydalanilmasligini bilish va xatoni tuzatishimiz uchun nima noto'g'ri ekanligini aytib berish uchun foydalidir.

### Standart qiymat

Biz rekvizit uchun standart qiymatni o'rnatishimiz mumkin.

Keling, 'FoodItem' komponentida 'foodDesc' prop uchun standart qiymat yarataylik va keyin 'foodDesc' rekvizitini aniqlamasdan guruch uchun shunday element yarataylik:

{% code title="App.vue:" %}
```html
<template>
  <h1>Food</h1>
  <p>My favorite food has a diploma image attached to it.</p>
  <div id="wrapper">
    <food-item
      food-name="Apples"
      food-desc="Apples are a type of fruit that grow on trees."
      v-bind:is-favorite="true"/>
    <food-item
      food-name="Pizza"
      food-desc="Pizza has a bread base with tomato sauce, cheese, and toppings on top."
      v-bind:is-favorite="false"/>
    <food-item
      food-name="Rice"
      food-desc="Rice is a type of grain that people like to eat." 
      v-bind:is-favorite="false"/>
  </div>
</template> 
```
{% endcode %}

{% code title="FoodItem.vue:" %}
```html
<script>
  export default {
    props: {
      foodName: {
        type: String,
        required: true
      },
      foodDesc: {
        type: String,
        required: false,
        default: 'This is the default description.'
      }
      isFavorite: {
        type: Boolean,
        required: false,
        default: false
      }
    }
  }
</script>
```
{% endcode %}

### Props Validator funktsiyasi

Shuningdek, biz prop qiymatining haqiqiy yoki yo'qligini hal qiladigan validator funktsiyasini aniqlashimiz mumkin.

Bunday validator funktsiyalari rost yoki yolg'onni qaytarishi kerak. Tasdiqlovchi noto'g'ri qaytarsa, bu prop qiymati yaroqsiz degan ma'noni anglatadi. Sahifamizni ishlab chiquvchi rejimida ishga tushirganimizda noto‘g‘ri tayanch qiymati brauzer konsolida ogohlantirish hosil qiladi va ogohlantirish komponentlardan maqsadli foydalanilganligiga ishonch hosil qilish uchun foydali maslahatdir.

Aytaylik, biz oziq-ovqat tavsifi ma'lum uzunlikda, 20 dan 50 tagacha belgi bo'lishini xohlaymiz. Taqdim etilgan oziq-ovqat tavsifi yaroqli uzunlikka ega ekanligiga ishonch hosil qilish uchun biz validator funksiyasini qo‘shishimiz mumkin.

{% code title="FoodItem.vue:" %}
```html
<script>
  export default {
    props: {
      foodName: {
        type: String,
        required: true
      },
      foodDesc: {
        type: String,
        required: false,
        default: 'This is the default description.',
        validator: function(value) {
          if( 20<value.length && value.length<50 ) {
            return true;
          }
          else {
            return false;
          }
        }
      }
      isFavorite: {
        type: Boolean,
        required: false,
        default: false
      }
    }
  }
</script>
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Agar siz mahalliy loyihangizga yuqoridagi validator kodini qo'shsangiz, ishlab chiqish rejimida ogohlantirish olasiz, chunki pizza uchun taom tavsifi 65 belgidan iborat bo'lib, validator funksiyasi ruxsat berganidan 15 belgi uzunroqdir.

![](https://www.w3schools.com/vue/img\_validator\_warning.png)
{% endhint %}

### Proplarni o'zgartirish

Asosiy elementda komponent yaratilganda, biz bola elementda olingan rekvizit qiymatini o'zgartirishga ruxsat berilmaydi. Shunday qilib, `FoodItem.vue`biz dan olingan "isFavorite" prop qiymatini o'zgartira olmaymiz `App.vue`. Tayanch faqat ota-onadan o'qiladi, bu `App.vue`bizning holatlarimizda.

Aytaylik, foydalanuvchi tugmani bosish orqali qaysi taomni sevimli deb hisoblashini o'zgartirish imkoniyatiga ega bo'lishini xohlaymiz. Endi "isFavorite" rekvizitini o'zgartirish kerak, lekin biz buni qila olmaymiz, chunki u faqat o'qiladi.

Bizga "isFavorite" ni o'zgartirishga ruxsat berilmagan. Bu xato hosil qiladi.

```js
methods: {
  toggleFavorite() { 
    this.isFavorite = !this.isFavorite;
  }
}
```

Buni hal qilish uchun biz "foodIsFavorite" ichidagi yangi ma'lumotlar qiymatini ishga tushirish uchun rekvizitdan foydalanishimiz mumkin `FoodItem.vue`, masalan:

```js
data() {
  return { 
    foodIsFavorite: this.isFavorite
  }
}
```

Va endi biz foydalanuvchi ushbu yangi ma'lumotlar qiymatini almashtirishi uchun usul qo'shishimiz mumkin:

```js
methods: {
  toggleFavorite() { 
    this.foodIsFavorite = !this.foodIsFavorite;
  }
}
```

Shuningdek, har bir oziq-ovqat mahsulotiga almashtirish tugmachasini qo'shishimiz va tegni yangi "foodIsFavorite" ma'lumotlar xususiyatiga qarab o'zgartirishimiz `v-show`kerak `<img>`. Va misolimizni soddalashtirish uchun biz rekvizitlar deklaratsiyasini shunchaki massivga qisqartiramiz.

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
