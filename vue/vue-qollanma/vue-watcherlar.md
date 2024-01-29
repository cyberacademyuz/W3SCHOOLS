# Vue Watcherlar

{% hint style="success" %}
Kuzatuvchi - bir xil nomdagi ma'lumotlar xususiyatini kuzatuvchi usul**.**

Har safar ma'lumotlar xususiyati qiymati o'zgarganda **kuzatuvchi** ishlaydi.

Agar ma'lum bir ma'lumot xususiyati qiymati amalni talab qilsa, **kuzatuvchidan** foydalaning.
{% endhint %}

### Kuzatuvchi kontseptsiyasi

Kuzatuvchilar - bu biz o'rganadigan Vue misolidagi to'rtinchi konfiguratsiya variantidir. Biz ko'rib chiqqan dastlabki uchta konfiguratsiya variantlari "ma'lumotlar", "usullar" va "hisoblangan".

"Ma'lumotlar"da bo'lgani kabi, "usullar" va "hisoblangan" kuzatuvchilar ham Vue misolida ajratilgan nomga ega: " **tomosha qilish** ".

{% code title="sintaksis" %}
```
const app = Vue.createApp({
  data() {
    ...
  },
  watch: {
    ...
  },
  computed: {
    ...
  },
  methods: {
    ...
  }
})
```
{% endcode %}

Yuqoridagi yashil maydonda aytib o'tilganidek, kuzatuvchi xuddi shu nomdagi ma'lumotlar xususiyatini kuzatadi.

Biz hech qachon kuzatuvchi usulini chaqirmaymiz. U faqat xususiyat qiymati o'zgarganda avtomatik ravishda chaqiriladi.

Yangi xususiyat qiymati har doim kuzatuvchi usuliga kirish argumenti sifatida mavjud va eski qiymat ham.

Element `<input type="range">`"rangeVal" qiymatini o'zgartirish uchun ishlatiladi. Kuzatuvchi foydalanuvchining noqonuniy deb hisoblangan 20 dan 60 gacha bo'lgan qiymatlarni tanlashiga yo'l qo'ymaslik uchun ishlatiladi.

```
<input type="range" v-model="rangeVal">
<p>{{ rangeVal }}</p>
```

```
const app = Vue.createApp({
  data() {
    rangeVal: 70
  },
  watch: {
    rangeVal(val){
      if( val>20 && val<60) {
        if(val<40){
          this.rangeVal = 20;
        }
        else {
          this.rangeVal = 60;
        }
      }
    }
  }
})
```

### Yangi va eski qadriyatlarga ega kuzatuvchi

Yangi xususiyat qiymatiga qo'shimcha ravishda, oldingi xususiyat qiymati ham kuzatuvchi usullariga kirish argumenti sifatida avtomatik ravishda mavjud bo'ladi.



`<div>`Biz sichqoncha ko'rsatgichining x-pozitsiyasini "xPos" ni "updatePos" usuli bilan yozib olish uchun elementga bosish hodisasini o'rnatdik . Kuzatuvchi eski va yangi kiritish argumentlaridan foydalangan holda kuzatuvchi usuliga yangi x-pozitsiyasi va oldingisi o'rtasidagi piksellardagi farqni hisoblab chiqadi.

```
<div v-on:click="updatePos"></div>
<p>{{ xDiff }}</p>
```

```
const app = Vue.createApp({
  data() {
    xPos: 0,
    xDiff: 0
  },
  watch: {
    xPos(newVal,oldVal){
      this.xDiff = newVal-oldVal
    }
  },
  methods: {
    updatePos(evt) {
      this.xPos = evt.offsetX
    }
  }
})
```

Shuningdek, biz yangi va eski qiymatlardan foydalanuvchiga kiritilgan maʼlumotlar notoʻgʻri boʻlgandan toʻgʻrigacha boʻlgan vaqtda fikr bildirish uchun foydalanishimiz mumkin:



Elementning qiymati `<input>`kuzatuvchiga ulanadi. Agar qiymat "@" belgisini o'z ichiga olsa, u haqiqiy elektron pochta manzili hisoblanadi. Foydalanuvchi kiritilgan kiritilgan maʼlumotlar toʻgʻri, notoʻgʻri yoki oxirgi marta bosish orqali haqiqiy boʻlganligini bildirish uchun fikr-mulohaza matnini oladi.

```
<input v-type="email" v-model="inpAddress">
<p v-bind:class="myClass">{{ feedbackText }}</p>
const app = Vue.createApp({
  data() {
    inpAddress: '',
    feedbackText: '',
    myClass: 'invalid'
  },
  watch: {
    inpAddress(newVal,oldVal) {
      if( !newVal.includes('@') ) {
        this.feedbackText = 'The e-mail address is NOT valid';
        this.myClass = 'invalid';
      }
      else if( !oldVal.includes('@') && newVal.includes('@') ) {
        this.feedbackText = 'Perfect! You fixed it!';
        this.myClass = 'valid';
      }
      else {
        this.feedbackText = 'The e-mail address is valid :)';
      }
    }
  }
})
```

### Kuzatuvchilar va usullar

Kuzatuvchilar va usullar funktsiyalar sifatida yozilgan, ammo juda ko'p farqlar mavjud:

* **Metodlar** HTML dan chaqiriladi.
* **Voqea sodir bo'lganda usullar** ko'pincha chaqiriladi.
* **Methods** avtomatik ravishda hodisa ob'ektini kirish sifatida qabul qiladi.
* **Shuningdek, biz tanlagan boshqa qiymatlarni usulga** kiritish sifatida yuborishimiz mumkin .
* **Kuzatuvchilar** faqat kuzatilgan ma'lumotlar xususiyati qiymati o'zgarganda chaqiriladi va bu avtomatik ravishda sodir bo'ladi.
* **Kuzatuvchilar** avtomatik ravishda tomosha qilingan mulkdan yangi va eski qiymatni oladi.
* Biz kirish sifatida **kuzatuvchi** bilan boshqa qiymatlarni yuborishni tanlay olmaymiz .

### Kuzatuvchilar va hisoblangan xususiyatlar

Kuzatuvchilar va hisoblangan xususiyatlar funksiya sifatida yoziladi.

Kuzatuvchilar va hisoblangan xususiyatlar, qaramlik o'zgarganda avtomatik ravishda chaqiriladi va hech qachon HTMLdan chaqiriladi.

Hisoblangan xususiyatlar va kuzatuvchilar o'rtasidagi ba'zi farqlar:

* **Kuzatuvchilar** faqat bitta xususiyatga, ular tomosha qilish uchun o'rnatilgan xususiyatga bog'liq.
* **Hisoblangan xususiyatlar** ko'p xususiyatlarga bog'liq bo'lishi mumkin.
* **Hisoblangan xususiyatlar** dinamik xususiyatdan tashqari ma'lumotlar xususiyatlari kabi ishlatiladi.
* **Kuzatuvchilar** HTML dan havola qilinmaydi.
