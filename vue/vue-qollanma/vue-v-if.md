# Vue v-if

{% hint style="success" %}
`v-if`Oddiy JavaScript-ga qaraganda, direktiva bilan Vue-dagi shartga qarab HTML elementini yaratish ancha oson .

Vue bilan siz shartli ravishda yaratmoqchi bo'lgan HTML elementiga to'g'ridan-to'g'ri if-iborasini yozasiz. Bu juda oddiy.
{% endhint %}

### Vue-da shartli renderlash

**Vue-da shartli renderlash**`v-if` , `v-else-if`va direktivalari yordamida amalga oshiriladi `v-else`.

Shartli ko‘rsatish HTML elementi faqat shart rost bo‘lsa yaratiladi, ya’ni agar o‘zgaruvchi “to‘g‘ri” bo‘lsa, “Stokda” matni yaratiladi, agar bu o‘zgaruvchi “noto‘g‘ri” bo‘lsa, “Stokda yo‘q” matni yaratiladi.

Stokda yozuv mashinkalari bor yoki yo'qligiga qarab turli xil xabarlarni yozing:

```
<p v-if="typewritersInStock">
  in stock
</p>

<p v-else>
  not in stock
</p>
```

### Vuedagi shartlar

`true`Shart yoki "agar-bayonot" bu yoki bo'lgan narsadir `false`.

Shart ko'pincha yuqoridagi misoldagi kabi ikkita qiymat o'rtasida bir qiymat boshqasidan kattaroq yoki yo'qligini tekshirish uchun **taqqoslashdir .**

* Bunday tekshirishlarni amalga oshirish uchun , yoki kabi **taqqoslash operatorlaridan** foydalanamiz .`<>=!==`
* Taqqoslash tekshiruvlari yoki kabi **mantiqiy operatorlar** bilan ham birlashtirilishi mumkin .`&&||`
* JavaScript taqqoslashlari haqida ko'proq ma'lumot olish uchun [JavaScript o'quv](https://www-w3schools-com.translate.goog/js/js\_comparisons.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) sahifamizga o'ting .

Saqlashda mavjud yoki yo'qligini aniqlash uchun biz saqlashdagi yozuv mashinkalari sonini taqqoslash tekshiruvi bilan ishlatishimiz mumkin:

Saqlashdagi yozuv mashinkalari soniga qarab “Stokda” yoki “Stokda yo‘q” deb yozishni tanlash uchun taqqoslash tekshiruvidan foydalaning.

```
<p v-if="typewriterCount > 0">
  in stock
</p>

<p v-else>
  not in stock
</p>
```

### Shartli ko'rsatish bo'yicha ko'rsatmalar

Ushbu umumiy ko'rinish shartli qayta ishlash uchun ishlatiladigan turli Vue direktivalari qanday birgalikda ishlatilishini tasvirlaydi.

| siyosat     | tafsilotlar                                                                                                                                                                      |
| ----------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `v-if`      | `v-else-if`Yakka holda yoki va/yoki bilan ishlatilishi mumkin `v-else`. Agar ichidagi shart `v-if`"to'g'ri" bo'lsa `v-else-if`yoki `v-else`hisobga olinmasa.                     |
| `v-else-if` | `v-if`Keyin yoki boshqasidan foydalanish kerak `v-else-if`. Agar ichidagi shart `v-else-if`"to'g'ri" bo'lsa `v-else-if`yoki `v-else`keyin kelgan shart hisobga olinmaydi.        |
| `v-else`    | Har doim to'g'ri, lekin agar if-iborasining birinchi qismi noto'g'ri bo'lsa, hisobga olinadi. if iborasining eng oxirida, `v-if`va dan keyin joylashtirilishi kerak `v-else-if`. |

Yuqorida ko'rsatilgan uchta ko'rsatmaga ega bo'lgan misolni ko'rish uchun biz avvalgi misolni kengaytiramiz, `v-else-if`shunda foydalanuvchi "Stokda", "Juda oz qoldi!" yoki "Stokda yo'q":

Taqqoslash tekshiruvidan foydalanib, "Stokda", "Juda oz qoldi!" yoki saqlashdagi yozuv mashinkalari soniga qarab "Stokda yo'q".

```
<p v-if="typewriterCount>3">
  In stock
</p>

<p v-else-if="typewriterCount>0">
  Very few left!
</p>

<p v-else>
  Not in stock
</p>
```

### Funktsiyadan qaytariladigan qiymatdan foydalaning

Direktiv bilan taqqoslash tekshiruvidan foydalanish o'rniga `v-if`biz funktsiyadan "haqiqiy" yoki "noto'g'ri" qaytish qiymatidan foydalanishimiz mumkin:

Agar ma'lum bir matnda "pitsa" so'zi bo'lsa, tegishli xabar bilan \<p> tegini yarating. 'Includes()' usuli matnda ma'lum so'zlarni o'z ichiga olganligini tekshiradigan mahalliy JavaScript usulidir.

```
<div id="app">
  <p v-if="text.includes('pizza')">The text includes the word 'pizza'</p>
  <p v-else>The word 'pizza' is not found in the text</p>
</div>data() {
  return {
    text: 'I like taco, pizza, Thai beef salad, pho soup and tagine.'
  }
}
```

Yuqoridagi misol, `v-if`\<div> va \<img> teglari kabi boshqa teglarni ham yaratishi mumkinligini ko'rsatish uchun kengaytirilishi mumkin:

Agar ma'lum bir matnda "pitsa" so'zi bo'lsa, pizza tasviri bilan \<div> tegini va xabarli \<p> ​​tegini yarating. "Includes()" usuli - bu matnda ma'lum so'zlarni o'z ichiga olganligini tekshiradigan mahalliy JavaScript usuli.

```
<div id="app">
  <div v-if="text.includes('pizza')">
    <p>The text includes the word 'pizza'</p>
    <img src="img_pizza.svg">
  </div>
  <p v-else>The word 'pizza' is not found in the text</p>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        text: 'I like taco, pizza, Thai beef salad, pho soup and tagine.'
      }
    }
  })
  app.mount('#app')
</script>
```

Quyida misol yanada kengaytirilgan.

Agar ma'lum bir matnda "pitsa" yoki "burrito" so'zlari bo'lsa yoki bu so'zlarning hech biri bo'lmasa, turli xil tasvirlar va matnlar yaratiladi.

```
<div id="app">
  <div v-if="text.includes('pizza')">
    <p>The text includes the word 'pizza'</p>
    <img src="img_pizza.svg">
  </div>
  <div v-else-if="text.includes('burrito')">
    <p>The text includes the word 'burrito', but not 'pizza'</p>
    <img src="img_burrito.svg">
  </div>
  <p v-else>The words 'pizza' or 'burrito' are not found in the text</p>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        text: 'I like taco, pizza, Thai beef salad, pho soup and tagine.'
      }
    }
  })
  app.mount('#app')
</script>
```

{% hint style="success" %}
Vue yordamida biz an'anaviy JavaScript-ga qaraganda ma'lum sharoitlarda elementlarni yaratadigan kodni yozishimiz mumkin.
{% endhint %}
