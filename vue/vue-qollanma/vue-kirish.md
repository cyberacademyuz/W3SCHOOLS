# Vue Kirish

{% hint style="success" %}
Vue - bu JavaScript **freymworki**. Uni HTML sahifasiga \<script> tegi orqali qo'shish mumkin.

Vue HTML atributlarini **direktivlar** bilan kengaytiradi va ma'lumotlarni HTMLga expressionlar bilan bog'laydi.
{% endhint %}

### Vue - bu JavaScript freymworki

Vue - bu JavaScript-da yozilgan front-end uchun JavaScript freymwork.

Vue-ga o'xshash freymworklar React va Angulardir, ammo Vue soddaroq va boshlash osonroq.

Vue JavaScript fayli sifatida taqdim qilinadi va veb-sahifaga \<script> elementi bilan qo'shiladi:

```javascript
<script>
  src="https://unpkg.com/vue@3/dist/vue.global.js">
</script>
```

### Nega Vue-ni o'rganish kerak ?

* U oddiy va ishlatish uchun qulay.
* U oddiy va murakkab loyihalarni bajara oladi.
* Uning tobora ommalashib borayapti va open source hamjamiyatini qo'llab quvvatlaydi.
* Oddiy JavaScript-da HTML va JavaScript **qanday** bog'langanishini yozishimiz kerak, lekin Vue-da shunchaki **IS** ulanish mavjudligiga ishonch hosil qilishimiz va qolganlari bilan Vue-ga g'amxo'rlik qilishimiz kerak. <mark style="color:green;">(Chala)</mark>
* U templatega asoslangan sintaksis hisoblanib, ma'lumotlarni ikki tomonlama bog'lash va markazlashtirilgan steyt boshqaruvi bilan yanada samarali ishlab chiqish jarayoniga imkon beradi.

Agar ushbu fikrlardan ba'zilarini tushunish qiyin bo'lsa, tashvishlanmang, o'quv qo'llanmaning oxirida tushunib olasiz.

### Mening birinchi sahifam

Endi asosiy 5 bosqich orqali birinchi Vue veb-sahifamizni qanday yaratishni o'rganamiz:

1. Oddiy HTML faylidan boshlang.
2. Vue ga ulanish uchun `id="app"` ga ega `<div>` elementini qo'shing.
3. Vue havolasi bilan `<scipt>` tegini qo‘shish orqali brauzerga Vue kodini qanday ishlatishni ayting.
4. IIchida Vue misoli mavjud \<script> tegini qo'shing
5. Vue misolini `<div id="app">` tegiga ulang.

Ushbu qadamlar quyida batafsil ko'rsatib berilgan, va oxirida barcha kodlar "Try yourself" misolida keltirilgan.

#### 1-qadam: HTML sahifasi

Oddiy HTML sahifasidan boshlang:

```
<!DOCTYPE html>
<html lang="en">
<head>
  <title>My first Vue page</title>
</head>
<body>

</body>
</html>
```

#### 2-qadam: \<div> qo'shing

Ulanish uchun Vue sahifangizga HTML elementi kerak

`<body>` tegi ichiga `<div>`tegini qo'ying va unga identifikator bering:

```
<body>
  <div id="app"></div>
</body>
```

#### 3-qadam: Vue-ga havola qo'shing

Brauzerimizga Vue kodi tushuntirib berish uchun ushbu `<script>`tegni qo'shing:

```
<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
```

#### 4-qadam: Vue misolini qo'shing

Endi Vue kodimizni qo'shishimiz kerak.

Bu Vue kodiga misol hisoblanadi va u ma'lumotlar, metodlar va boshqa narsalarni o'z ichiga olishi mumkin, ammo hozir u faqat xabarni o'z ichiga oladi.

Ushbu `<script>` tegining oxirgi qatorida bizning Vue misolimiz `<div id="app">` tegiga ulangan:

```
<div id="app"></div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<script>

  const app = Vue.createApp({
    data() {
      return {
        message: "Hello World!"
      }
    }
  })

 app.mount('#app')

</script>
```

#### 5-qadam: Matn interpolatsiyasi bilan "xabar" ni ko'rsatish

Va nihoyat, matn interpolyatsiyasidan, ikki jingalak qavsli \{{ \}} Vue sintaksisidan ma'lumotlar uchun placeholder sifatida foydalanishimiz mumkin.

```
<div id="app"> {{ message }} </div>
```

Brauzer `{{ message }}`Vue misolidagi "xabar" xususiyatida saqlangan matn bilan almashadi.

Mana bizning birinchi Vue sahifamiz:

#### Misol: Mening birinchi Vue sahifam!

Quyidagi “O‘zingiz sinab ko‘ring” tugmasi orqani ushbu kodni sinab ko‘ring.

{% code title="" %}
```
<!DOCTYPE html>
<html lang="en">
<head>
  <title>My first Vue page</title>
</head>
<body>

  <div id="app">
    {{ message }}
  </div>

  <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

  <script>
    const app = Vue.createApp({
      data() {
        return {
          message: "Hello World!"
        }
      }
    })

   app.mount('#app')

  </script>
</body>
</html>
```
{% endcode %}

### Matn interpolyatsiyasi

Matn interpolyatsiyasi - bu Vue koddan matn olinganda veb-sahifada ko'rsatish uchun kerak.

Brauzer sahinani quyidagi kod bilan qabul qiladi:

```
<div id="app"> {{ message }} </div>
```

Keyin brauzer Vue kodining  "message" xususiyati ichidagi matnni topadi va Vue kodini bunga tarjima qiladi:

```
<div id="app">Hello World!</div>
```

### Matn interpolyatsiyasida Javascript

Ikki jingalak qavs `{{ }}` ichida oddiy **JavaScript exprssionlari** ham yozilishi mumkin.

{% code title="<div> elementi ichidagi xabarga tasodifiy raqam qo'shish uchun JavaScript sintaksisidan foydalaning:" %}
```
<div id="app">
  {{ message }} <br>
  {{'Random number: ' + Math.ceil(Math.random()*6) }}
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>

<script>

  const app = Vue.createApp({
    data() {
      return {
        message: "Hello World!"
      }
    }
  })

 app.mount('#app')

</script>

```
{% endcode %}

### Boshlash

Ushbu qo'llanma sizga Vue asoslarini o'rgatadi.

Ushbu qo'llanmani tushunish uchun HTML, CSS va JavaScript bo'yicha boshlang'ich bilimlaringiz bo'lishi kerak.

Ushbu qo'llanmani davom ettirish uchun "Keyingi" tugmasini bosing.
