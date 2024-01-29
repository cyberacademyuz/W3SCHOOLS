# Vue Formalar

{% hint style="success" %}
Vue bizga javob berish va shaklni tekshirish kabi qo'shimcha funksiyalarni qo'shish orqali shakllar bilan foydalanuvchi tajribasini yaxshilashning oson yo'lini beradi.

Vue `v-model`shakllar bilan ishlashda direktivadan foydalanadi.
{% endhint %}

### Vue bilan bizning birinchi formamiz

Shakl yaratishda Vue-dan qanday foydalanish mumkinligini ko'rish uchun oddiy xarid ro'yxati misolidan boshlaylik.

Aloqador teglar va atributlar bilan HTML formatidagi shakllar haqida qoʻshimcha maʼlumot olish uchun bizning HTML shakllari boʻyicha oʻquv qoʻllanmamizga qarang.

1\. Standart HTML forma elementlarini qo‘shing:

```
<form>
  <p>Add item</p>
  <p>Item name: <input type="text" required></p>
  <p>How many: <input type="number"></p>
  <button type="submit">Add item</button>
</form>
```

2\. Joriy element nomi, raqami va xaridlar roʻyxati bilan Vue nusxasini yarating va `v-model`unga kirishlarimizni ulash uchun foydalaning.

```
<div id="app">
  <form>
    <p>Add item</p>
    <p>Item name: <input type="text" required v-model="itemName"></p>
    <p>How many: <input type="number" v-model="itemNumber"></p>
    <button type="submit">Add item</button>
  </form>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        itemName: null,
        itemNumber: null,
        shoppingList: [
          { name: 'Tomatoes', number: 5 }
        ]
      }
    }
  })
  app.mount('#app')
</script>
```

3\. Xaridlar ro'yxatiga element qo'shish usulini chaqiring va yuborilganda brauzerning standart yangilanishini oldini oling.

```
<form v-on:submit.prevent="addItem">
```

4\. Buyumni xaridlar ro‘yxatiga qo‘shadigan va shaklni tozalaydigan usulni yarating:

```
methods: {
  addItem() {
    let item = {
      name: this.itemName,
      number: this.itemNumber
      }
    this.shoppingList.push(item);
    this.itemName = null
    this.itemNumber = null
  }
}
```

`v-for`5. Shakl ostida avtomatik yangilanadigan xaridlar roʻyxatini koʻrsatish uchun foydalaning :

```
<p>Shopping list:</p>
<ul>
  <li v-for="item in shoppingList">{{item.name}}, {{item.number}}</li>
</ul>
```

Quyida bizning birinchi Vue formamiz uchun yakuniy kod mavjud.

Ushbu misolda biz xaridlar ro'yxatiga yangi narsalarni qo'shishimiz mumkin.

```
<div id="app">
  <form v-on:submit.prevent="addItem">
    <p>Add item</p>
    <p>Item name: <input type="text" required v-model="itemName"></p>
    <p>How many: <input type="number" v-model="itemNumber"></p>
    <button type="submit">Add item</button>
  </form>

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
        shoppingList: [
          { name: 'Tomatoes', number: 5 }
        ]
      }
    },
    methods: {
      addItem() {
        let item = {
          name: this.itemName,
          number: this.itemNumber
        }
        this.shoppingList.push(item)
        this.itemName = null
        this.itemNumber = null
      }
    }
  })
  app.mount('#app')
</script>
```

{% hint style="success" %}
`v-model`Yuqoridagi misolda ikki tomonlama bog'lanishga e'tibor bering :

* `v-model`HTML kiritish o'zgarganda Vue namunasi ma'lumotlarini yangilaydi
* `v-model`shuningdek, Vue namunasi ma'lumotlari o'zgarganda HTML kiritishni yangilaydi

`v-model`Shakl misollari haqida ko'proq ma'lumot olish va ko'rish uchun "Keyingi" tugmasini bosing.
{% endhint %}
