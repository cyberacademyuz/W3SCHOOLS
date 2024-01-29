# Vue v-model

{% hint style="success" %}
Oddiy JavaScript bilan solishtirganda, Vue-da shakllar bilan ishlash osonroq, chunki `v-model`direktiv barcha turdagi kirish elementlari bilan bir xil tarzda bog'lanadi.

`v-modelvalue`Vue misolidagi kirish elementi atributi va ma'lumotlar qiymati o'rtasida bog'lanish hosil qiladi . Kirishni o'zgartirsangiz, ma'lumotlar yangilanadi va ma'lumotlar o'zgarganda, kirish ham yangilanadi (ikki tomonlama ulanish).
{% endhint %}

### Ikki tomonlama bog'lash

Oldingi sahifadagi xarid roʻyxati misolida koʻrganimizdek, `v-model`bizga ikki tomonlama bogʻlanishni taʼminlaydi, yaʼni shakl kiritish elementlari Vue maʼlumotlar namunasini yangilaydi va Vue namunasi maʼlumotlaridagi oʻzgarish kirishlarni yangilaydi.

Quyidagi misol, shuningdek, bilan ikki tomonlama bog'lanishni ko'rsatadi `v-model`.

Ikki tomonlama ulanish: Vue ma'lumotlar xususiyati qiymati yangilanishini ko'rish uchun kiritish maydoniga yozishga harakat qiling. Shuningdek, Vue ma'lumotlar xususiyati qiymatini o'zgartirish, kodni ishga tushirish va kiritish maydoni qanday yangilanganligini ko'rish uchun to'g'ridan-to'g'ri kodga yozishga harakat qiling.

```
<div id="app">
  <input type="text" v-model="inpText">
  <p> {{ inpText }} </p>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        inpText: 'Initial text'
      }
    }
  })
  app.mount('#app')
</script>
```

{% hint style="warning" %}
**Eslatma:** Ikki tomonlama bog'lash funksiyasiga aslida va `v-model`kombinatsiyasi bilan erishish mumkin :`v-bind:valuev-on:input`

* `v-bind:value`Vue namunasi ma'lumotlaridan kirish elementini yangilash uchun,
* va `v-on:input`kirishdan Vue misol ma'lumotlarini yangilash uchun.

Lekin `v-model`foydalanish ancha oson, shuning uchun biz shunday qilamiz.
{% endhint %}

### Dinamik tasdiqlash qutisi

Oldingi sahifadagi xaridlar ro'yxatiga element muhim yoki muhim emasligini belgilash uchun katakchani qo'shamiz.

Belgilash katagiga biz har doim joriy "muhim" holatini aks ettiruvchi, "to'g'ri" yoki "noto'g'ri" o'rtasida dinamik ravishda o'zgarib turadigan matnni qo'shamiz.

`v-model`Biz foydalanuvchilarning o'zaro ta'sirini yaxshilash uchun ushbu dinamik katakchani va matnni qo'shish uchun foydalanamiz .

Bizga kerak:

* Vue misoli ma'lumotlar xususiyatidagi "muhim" deb nomlangan mantiqiy qiymat
* foydalanuvchi element muhimligini tekshirishi mumkin bo'lgan katakcha
* foydalanuvchi element muhimligini ko'rishi uchun dinamik fikr-mulohaza matni

Quyida xaridlar ro'yxatidan ajratilgan "muhim" xususiyat qanday ko'rinishini ko'rib chiqamiz.

Belgilash qutisi matni dinamik bo'lib, matn joriy tasdiqlash qutisi kiritish qiymatini aks ettiradi.

```
<div id="app">
  <form>
    <p>
      Important item?
      <label>
        <input type="checkbox" v-model="important">
        {{ important }}
      </label>
    </p>
  </form>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
       important: false
      }
    }
  })
  app.mount('#app')
</script>
```

Keling, ushbu dinamik xususiyatni xaridlar ro'yxati misolimizga kiritaylik.

```
<div id="app">
  <form v-on:submit.prevent="addItem">
    <p>Add item</p>
    <p>Item name: <input type="text" required v-model="itemName"></p>
    <p>How many: <input type="number" v-model="itemNumber"></p>
    <p>
      Important?
      <label>
        <input type="checkbox" v-model="itemImportant">
        {{ important }}
      </label>
    </p>
    <button type="submit">Add item</button>
  </form>
  <hr>
  <p>Shopping list:</p>
  <ul>
    <li v-for="item in shoppingList">{{item.name}}, {{item.number}}</li>
  </ul>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        itemName: null,
        itemNumber: null,
        important: false,
        shoppingList: [
          { name: 'Tomatoes', number: 5, important: false }
        ]
      }
    },
    methods: {
      addItem() {
        let item = {
          name: this.itemName,
          number: this.itemNumber
          important: this.itemImportant
        }
        this.shoppingList.push(item)
        this.itemName = null
        this.itemNumber = null
        this.itemImportant = false
      }
    }
  })
  app.mount('#app')
</script>
```

### Xarid ro'yxatida topilgan narsalarni belgilang

Xarid qilish ro'yxatiga qo'shilgan narsalar topilgan deb belgilanishi uchun funksionallikni qo'shamiz.

Bizga kerak:

* bosish orqali javob beradigan ro'yxat elementlari
* bosilgan elementning holatini "topildi" ga o'zgartirish va undan elementni vizual ravishda boshqa joyga ko'chirish va uni CSS orqali urish uchun foydalaning.

Biz topishimiz kerak bo'lgan barcha elementlardan iborat bitta ro'yxat va quyida topilgan elementlardan iborat bitta ro'yxat yaratamiz. Biz aslida birinchi ro‘yxatdagi barcha elementlarni va ikkinchi ro‘yxatdagi barcha elementlarni qo‘yishimiz mumkin va `v-show`elementni birinchi yoki ikkinchi ro‘yxatda ko‘rsatishni aniqlash uchun “topildi” Vue ma’lumotlar xususiyatidan foydalanishimiz mumkin.

Xaridlar ro'yxatiga narsalarni qo'shgandan so'ng, biz ularni topib olganimizdan so'ng ularni bosish orqali xarid qilishga boramiz. Agar biror narsani xato bilan bosgan bo'lsak, elementni yana bir marta bosish orqali uni "topilmagan" ro'yxatiga qaytarishimiz mumkin.

```
<div id="app">
  <form v-on:submit.prevent="addItem">
    <p>Add item</p>
    <p>Item name: <input type="text" required v-model="itemName"></p>
    <p>How many: <input type="number" v-model="itemNumber"></p>
    <p>
      Important?
      <label>
        <input type="checkbox" v-model="itemImportant">
        {{ important }}
      </label>
    </p>
    <button type="submit">Add item</button>
  </form>

  <p><strong>Shopping list:</strong></p>
  <ul id="ulToFind">
    <li v-for="item in shoppingList"
        v-bind:class="{ impClass: item.important }"
        v-on:click="item.found=!item.found"
        v-show="!item.found">
          {{ item.name }}, {{ item.number}}
    </li>
  </ul>
  <ul id="ulFound">
    <li v-for="item in shoppingList"
        v-bind:class="{ impClass: item.important }"
        v-on:click="item.found=!item.found"
        v-show="item.found">
          {{ item.name }}, {{ item.number}}
    </li>
  </ul>

</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        itemName: null,
        itemNumber: null,
        important: false,
        shoppingList: [
          { name: 'Tomatoes', number: 5, important: false, found: false }
        ]
      }
    },
    methods: {
      addItem() {
        let item = {
          name: this.itemName,
          number: this.itemNumber,
          important: this.itemImportant,
          found: false
        }
        this.shoppingList.push(item)
        this.itemName = null
        this.itemNumber = null
        this.itemImportant = false
      }
    }
  })
  app.mount('#app')
</script>
```

### Shaklning o'zini dinamik qilish uchun v-modeldan foydalaning

Biz mijoz menyudan buyurtma beradigan shaklni yaratishimiz mumkin. Mijoz uchun qulay bo'lishi uchun biz faqat mijoz ichimliklar buyurtma qilishni tanlaganidan keyin tanlash uchun ichimliklarni taqdim etamiz. Bu mijozga menyudagi barcha mahsulotlarni bir vaqtning o'zida taqdim etishdan ko'ra yaxshiroq deb bahslash mumkin. Ushbu misolda biz shaklning o'zini dinamik qilish uchun `v-model`va foydalanamiz.`v-show`

Bizga kerak:

* Tegishli kiritish teglari va "Buyurtma" tugmasi bo'lgan shakl.
* "Kechki ovqat", "Ichimlik" yoki "Desert" ni tanlash uchun radio tugmalari.
* Kategoriya tanlanganidan so'ng, ushbu toifadagi barcha elementlar bilan ochiladigan menyu paydo bo'ladi.
* Element tanlanganda uning rasmini ko'rasiz, qanchaligini tanlashingiz va uni buyurtmaga qo'shishingiz mumkin. Buyurtmaga ob'ekt qo'shilganda shakl qayta tiklanadi.
