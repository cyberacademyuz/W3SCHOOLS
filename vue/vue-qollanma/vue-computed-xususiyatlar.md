# Vue Computed xususiyatlar

{% hint style="success" %}
**Hisoblangan xususiyatlar** ma'lumotlar xususiyatlariga o'xshaydi, faqat ular boshqa xususiyatlarga bog'liq.

**Hisoblangan xususiyatlar** usullar kabi yoziladi, lekin ular hech qanday kiritish argumentlarini qabul qilmaydi.

**Hisoblangan xususiyatlar** bog'liqlik o'zgarganda avtomatik ravishda yangilanadi, usullar, masalan, hodisani boshqarish kabi, biror narsa sodir bo'lganda chaqiriladi.

**Hisoblangan xususiyatlar** boshqa narsaga bog'liq bo'lgan narsani chiqarishda ishlatiladi.
{% endhint %}

### Hisoblangan xususiyatlar dinamikdir

Hisoblangan xususiyatning katta afzalligi shundaki, u dinamik bo'lib, masalan, bir yoki bir nechta ma'lumotlar xususiyatlarining qiymatiga qarab o'zgaradi.

Hisoblangan xususiyatlar biz o'rganadigan Vue misolidagi uchinchi konfiguratsiya variantidir. Biz ko'rib chiqqan dastlabki ikkita konfiguratsiya opsiyasi "ma'lumotlar" va "usullar" dir.

"Ma'lumotlar" va "usullar" kabi hisoblangan xususiyatlar Vue misolida ham zaxiralangan nomga ega: " **hisoblangan** ".

{% code title="sintaksis" %}
```
const app = Vue.createApp({
  data() {
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

### Hisoblangan xususiyat "ha" yoki "yo'q"

Aytaylik, biz xaridlar ro‘yxatidagi narsalarni yaratish uchun shaklni xohlaymiz va biz yangi element muhim yoki muhim emasligini belgilashni xohlaymiz. Oldingi misolda qilganimizdek, katakcha belgilansa, biz "to'g'ri" yoki "noto'g'ri" fikr bildirishimiz mumkin:

Matn holatni aks ettirishi uchun kiritish elementi dinamik holga keltiriladi.

```
<input type="checkbox" v-model="chbxVal"> {{ chbxVal }}
```

```
data() {
  return {
    chbxVal: false
  }
}
```

Biroq, agar siz kimdandir biror narsa muhimmi deb so'rasangiz, ular "to'g'ri" yoki "noto'g'ri" o'rniga "ha" yoki "yo'q" deb javob berishlari mumkin. Shunday qilib, shaklimizni oddiy tilga mosroq qilish uchun (intuitivroq) tasdiqlash katakchasida "to'g'ri" yoki "noto'g'ri" o'rniga fikr-mulohaza sifatida "ha" yoki "yo'q" bo'lishi kerak.

Tasavvur qiling-a, hisoblangan xususiyat bu bizga yordam beradigan mukammal vositadir.

Hisoblangan "isImportant" xususiyati bilan biz endi belgilash katakchasi yoqilganda va o'chirilganda foydalanuvchiga matnli fikr-mulohazalarni sozlashimiz mumkin.

```
<input type="checkbox" v-model="chbxVal"> {{ isImportant }}
data() {
  return {
    chbxVal: false
  }
},
computed: {
  isImportant() {
    if(this.chbxVal){
      return 'yes'
    }
    else {
      return 'no'
  }
}
```

### Hisoblangan xususiyatlar va usullar

Hisoblangan xususiyatlar va usullar funktsiyalar sifatida yoziladi, ammo ular boshqacha:

* **Methods** HTML dan chaqirilganda ishlaydi, lekin bog'liqlik o'zgarganda **hisoblangan xususiyatlar avtomatik ravishda yangilanadi.**
* **Hisoblangan xususiyatlar** ma'lumotlar xususiyatlaridan foydalanganimiz kabi ishlatiladi, lekin ular dinamikdir.
