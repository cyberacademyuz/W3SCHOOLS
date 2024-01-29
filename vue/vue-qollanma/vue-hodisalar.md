# Vue Hodisalar

{% hint style="success" %}
Vue-da hodisalarni boshqarish direktiva bilan amalga oshiriladi `v-on`, shuning uchun biz, masalan, tugma bosilganda nimadir sodir bo'lishimiz mumkin.

Hodisalarni qayta ishlash - HTML elementlari ma'lum bir hodisa sodir bo'lganda ma'lum bir kodni ishga tushirish uchun o'rnatiladi.

Vue-dagi voqealardan foydalanish oson va bizning sahifamizni chinakam sezgir qiladi.

Vue **usullari** - bu voqea sodir bo'lganda ishga tushirish uchun sozlanishi mumkin bo'lgan kod.

`v-on` **Modifikatorlar** yordamida siz voqeaga qanday munosabatda bo'lishni batafsilroq tasvirlashingiz mumkin.
{% endhint %}

### Voqealar bilan boshlang

Keling, o'rmondagi g'unajinlarni hisoblash uchun tugmani qanday bosishimiz mumkinligini ko'rsatish uchun misol bilan boshlaylik.

Bizga kerak:

1. Bir tugma
2. `v-on`"Click" hodisasini tinglash uchun \<button> tegida
3. Mos sonini ko'paytirish uchun kod
4. Moose sonini ushlab turish uchun Vue misolidagi xususiyat (o'zgaruvchi).
5. Qo'shaloq jingalak qavslar `{{}}`sonining ko'payishini ko'rsatish uchun

O'rmonda yana bitta muskulni sanash uchun tugmani bosing. Tugma har bosilganda count xususiyati ortadi.

```
<div id="app">
  <img src="img_moose.jpg">
  <p>{{ "Moose count: " + count }}</p>
  <button v-on:click="count++">Count moose</button>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        count: 0
      }
    }
  })
 app.mount('#app')
</script>
```

{% hint style="warning" %}
**Eslatma:** Vue bilan birga keladigan afzallik shundaki, \<p> yorlig'idagi mooselar soni avtomatik ravishda yangilanadi. Oddiy JavaScript bilan biz foydalanuvchi ko'rgan raqamni qo'shimcha kod qatori bilan yangilashimiz kerak.
{% endhint %}

### Voqealar

Kodni ishga tushirish uchun trigger sifatida foydalanishimiz mumkin bo'lgan ko'plab hodisalar mavjud, ulardan eng keng tarqalganlari: "klik", "sichqonchani bosish", "sichqonchani bosish", "tugmachani pastga tushirish" va "kirish".

Foydalanish uchun tadbirlarning toʻliq roʻyxatini koʻrish uchun [HTML DOM Voqealar sahifamizga](https://www-w3schools-com.translate.goog/jsref/dom\_obj\_event.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) tashrif buyurishingiz mumkin .

### 'dan'

Direktiv `v-on`bizga foydalanuvchi nima qilayotganiga javob beradigan sahifalarni yaratishga imkon beradi.

Vue `v-on`brauzerga qaysi voqeani tinglash kerakligini va bu voqea sodir bo'lganda nima qilish kerakligini aytib ishlaydi.

### usullari

Agar voqea sodir bo'lganda murakkabroq kodni ishga tushirishni istasak, kodni Vue usuliga qo'yishimiz va HTML atributidan ushbu usulga murojaat qilishimiz mumkin, masalan:

```
<p v-on:click="changeColor">Click me</p>
```

### Voqeani o'zgartiruvchilar

Va Vue usullariga qo'shimcha ravishda biz voqeani o'zgartirish uchun **hodisa modifikatorlari**`v-on` deb ataladigan narsadan foydalanishimiz mumkin , shunda u, masalan, sahifa yuklangandan keyin faqat bir marta sodir bo'ladi yoki ariza yuborilishining oldini olish uchun "yuborish" kabi hodisani o'zgartiring.

### Batafsil ma'lumot

Ko'rib turganimizdek, Vue-da voqealardan foydalanishni o'rganishimiz kerak bo'lgan uchta texnika mavjud:

1. Vue `v-on`direktivasi
2. Vue usullari
3. Vue `v-on`modifikatorlari

Ushbu oʻquv qoʻllanmasini davom ettirish va hodisalarni boshqarish boʻyicha ushbu usullar haqida koʻproq maʼlumot olish uchun “Keyingi” tugmasini bosing.
