# Vue metodlar

{% hint style="success" %}
Vue usullari "methods" xususiyati ostida Vue misoliga tegishli funksiyalardir.

`v-on`Vue usullaridan murakkabroq narsalarni qilish uchun hodisalarni boshqarish ( ) bilan foydalanish juda yaxshi .

Vue usullari voqealarni boshqarishdan boshqa narsalarni qilish uchun ham ishlatilishi mumkin.
{% endhint %}

### Vue "metods" xususiyati

Biz ushbu qo'llanmada qiymatlarni saqlashimiz mumkin bo'lgan "ma'lumotlar" xususiyatidan bir Vue xususiyatidan allaqachon foydalanganmiz.

Vue misoliga tegishli funktsiyalarni saqlashimiz mumkin bo'lgan "metods" deb nomlangan yana bir Vue xususiyati mavjud. Usul Vue misolida shunday saqlanishi mumkin:

```
const app = Vue.createApp({
  data() {
    return {
      text: ''
    }
  },
  methods: {
    writeText() {
      this.text = 'Hello Wrold!'
    }
  }
})
```

{% hint style="success" %}
**Maslahat:**`this.` Usul ichidan ma'lumotlar xususiyatiga murojaat qilish uchun biz prefiks sifatida yozishimiz kerak .
{% endhint %}

Elementni bosganimizda "writeText" usulini chaqirish uchun `<div>`quyidagi kodni yozishimiz mumkin:

```
<div v-on:click="writeText"></div>
```

Misol quyidagicha ko'rinadi:

Direktiv elementda "klik" hodisasini tinglash uchun `v-on`ishlatiladi . `<div>`"Click" hodisasi sodir bo'lganda, "writeText" usuli chaqiriladi va matn o'zgartiriladi.

```
<div id="app">
  <p>Click on the box below:</p>
  <div v-on:click="writeText">
    {{ text }}
  </div>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        text: ''
      }
    },
    methods: {
      writeText() {
        this.text = 'Hello World!'
      }
    }
  })
  app.mount('#app')
</script>
```

### Voqea obyekti bilan usulni chaqiring

Voqea sodir bo'lganda, usul chaqiriladi, **hodisa ob'ekti** sukut bo'yicha usul bilan uzatiladi. Bu juda qulay, chunki hodisa ob'ekti juda ko'p foydali ma'lumotlarni o'z ichiga oladi, masalan, maqsadli ob'ekt, hodisa turi yoki "bosish" yoki "sichqonchani siljitish" hodisasi sodir bo'lganda sichqonchaning holati.

Direktiv elementda "mousemove" hodisasini tinglash uchun `v-on`ishlatiladi . `<div>`"Mousemove" hodisasi sodir bo'lganda, "mousePos" usuli chaqiriladi va hodisa ob'ekti sukut bo'yicha usul bilan yuboriladi, shuning uchun biz sichqoncha ko'rsatkichi o'rnini olishimiz mumkin.

`this.`Usuldan Vue namunasi ma'lumotlar xususiyati ichidagi "xPos" ga murojaat qilish uchun biz prefiksdan foydalanishimiz kerak.

```
<div id="app">
  <p>Move the mouse pointer over the box below:</p>
  <div v-on:mousemove="mousePos"></div>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        xPos: 0,
        yPos: 0
      }
    },
    methods: {
      mousePos(event) {
        this.xPos = event.offsetX
        this.yPos = event.offsetY
      }
    }
  })
  app.mount('#app')
</script>
```

Yuqoridagi misolni faqat bitta satrga kengaytirsak, sichqoncha ko'rsatgichining x-yo'nalishiga qarab fon rangini o'zgartirishimiz ham mumkin. Biz qo'shishimiz kerak bo'lgan yagona narsa - `v-bind`uslub atributidagi fon rangini o'zgartirish:

Bu erda yuqoridagi misoldan farq shundaki, fon rangi "xPos" bilan bog'langan bo'lib, `v-bind`hsl "hue" qiymati "xPos" ga teng bo'ladi.

```
<div
  v-on:mousemove="mousePos"
  v-bind:style="{backgroundColor:'hsl('+xPos+',80%,80%)'}">
</div>
```

Quyidagi misolda hodisa ob'ekti tegdan matnni olib, `<textarea>`uni biz daftar ichida yozayotgandek ko'rsatish uchun.

Direktiv tegda matn maydoni elementi ichidagi matn o'zgarganda sodir bo'ladigan "kirish" hodisasini tinglash uchun `v-on`ishlatiladi .`<textarea>`

"Input" hodisasi sodir bo'lganda, "writeText" usuli chaqiriladi va hodisa ob'ekti sukut bo'yicha usul bilan yuboriladi, shuning uchun biz tegdan matnni olamiz `<textarea>`. Vue misolidagi "matn" xususiyati "writeText" usuli bilan yangilanadi. Ikki jingalak qavslar sintaksisi bilan "matn" qiymatini ko'rsatish uchun span elementi o'rnatiladi va bu Vue tomonidan avtomatik ravishda yangilanadi.

```
<div id="app">
  <textarea v-on:input="writeText" placeholder="Start writing.."></textarea>
  <span>{{ text }}</span>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        text: ''
      }
    },
    methods: {
      writeText(event) {
        this.text = event.target.value
      }
    }
  })
  app.mount('#app')
</script>
```

### O'tish argumentlari

Ba'zan biz voqea sodir bo'lganda usul bilan argument o'tkazmoqchimiz.

Aytaylik, siz o'rmon qo'riqchisi bo'lib ishlaysiz va siz buloqlarni ko'rishni hisobga olishni xohlaysiz. Ba'zan bir yoki ikkita, ba'zida bir kun davomida 10 dan ortiq siyish ko'rinadi. "+1" va "+5" ko'rinishlarini hisoblash uchun tugmachalarni va agar biz juda ko'p hisoblagan bo'lsak, "-1" tugmachasini qo'shamiz.

Bunday holda biz uchta tugma uchun bir xil usuldan foydalanishimiz mumkin va faqat boshqa tugmalardan argument sifatida boshqa raqam bilan usulni chaqirishimiz mumkin. Argument bilan usulni shunday chaqirishimiz mumkin:

```
<button v-on:click="addMoose(5)">+5</button>
```

Va "addMoose" usuli shunday ko'rinadi:

```
methods: {
  addMoose(number) {
    this.count = this.count + number
  }
}
```

To'liq misolda argumentni usul bilan o'tkazish qanday ishlashini ko'rib chiqamiz.

```
<div id="app">
  <img src="img_moose.jpg">
  <p>{{ "Moose count: " + count }}</p>
  <button v-on:click="addMoose(+1)">+1</button>
  <button v-on:click="addMoose(+5)">+5</button>
  <button v-on:click="addMoose(-1)">-1</button>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        count: 0
      }
    },
    methods: {
      addMoose(number) {
        this.count+=number
      }
    }
  })
 app.mount('#app')
</script>
```

### Argumentni ham, hodisa ob'ektini ham o'tkazish

Agar biz hodisa ob'ektini ham, boshqa argumentni ham o'tkazmoqchi bo'lsak, ajratilgan '' nom mavjud, `$event`biz usul chaqirilgan joyda foydalanishimiz mumkin, masalan:

```
<button v-on:click="addAnimal($event, 5)">+5</button>
```

Va Vue misolidagi usul shunday ko'rinadi:

```
methods: {
  addAnimal(e, number) {
    if(e.target.parentElement.id==="tigers"){
      this.tigers = this.tigers + number
    }
  }
}
```

Keling, hodisa ob'ektini ham, boshqa argumentni ham usul bilan qanday o'tkazishni ko'rish uchun misolni ko'rib chiqaylik.

Ushbu misolda bizning usulimiz hodisa ob'ektini ham, matnni ham qabul qiladi.

```
<div id="app">
  <img
    src="img_tiger.jpg"
    id="tiger"
    v-on:click="myMethod($event,'Hello')">
  <p>"{{ msgAndId }}"</p>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        msgAndId: ''
      }
    },
    methods: {
      myMethod(e,msg) {
        this.msgAndId = msg + ', '
        this.msgAndId += e.target.id
      }
    }
  })
 app.mount('#app')
</script>
```

### Kattaroq misol

Ushbu misolda biz har bir hayvon uchun uch xil o'sish bilan uchta turli hayvonlarni hisoblash uchun faqat bitta usuldan foydalanish mumkinligini ko'ramiz. Biz bunga hodisa ob'ektini ham, o'sish raqamini ham o'tkazish orqali erishamiz:

O'sish hajmi va hodisa ob'ekti tugma bosilganda usul bilan argument sifatida uzatiladi. Qaysi hayvonni sanash kerakligini aytish usuli bilan hodisa ob'ektini o'tkazish uchun zaxiralangan so'z ' `$event`' ishlatiladi.

```
<div id="app">
  <div id="tigers">
    <img src="img_tiger.jpg">
    <button v-on:click="addAnimal($event,1)">+1</button>
    <button v-on:click="addAnimal($event,5)">+5</button>
    <button v-on:click="addAnimal($event,1)">-1</button>
  </div>
  <div id="moose">
    <img src="img_moose.jpg">
    <button v-on:click="addAnimal($event,1)">+1</button>
    <button v-on:click="addAnimal($event,5)">+5</button>
    <button v-on:click="addAnimal($event,1)">-1</button>
  </div>
  <div id="kangaroos">
    <img src="img_kangaroo.jpg">
    <button v-on:click="addAnimal($event,1)">+1</button>
    <button v-on:click="addAnimal($event,5)">+5</button>
    <button v-on:click="addAnimal($event,1)">-1</button>
  </div>
  <ul>
    <li>Tigers: {{ tigers }} </li>
    <li>Moose: {{ moose }} </li>
    <li>Kangaroos: {{ kangaroos }} </li>
  </ul>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        tigers: 0,
        moose: 0,
        kangaroos: 0
      }
    },
    methods: {
      addAnimal(e,number) {
        if(e.target.parentElement.id==="tigers") {
          this.tigers+=number
        }
        else if(e.target.parentElement.id==="moose") {
          this.moose+=number
        }
        else {
          this.kangaroos+=number
        }
      }
    }
  })
 app.mount('#app')
</script>
```
