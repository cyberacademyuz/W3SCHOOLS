# Vue Hodisa modifikatorlari

{% hint style="success" %}
**Vue-dagi voqea modifikatorlari** voqealar qanday usullarni ishga tushirishini o'zgartiradi va hodisalarni yanada samarali va sodda tarzda boshqarishga yordam beradi.

Voqea modifikatorlari Vue direktivasi bilan birgalikda ishlatiladi `v-on`, masalan:

* HTML shakllarining standart yuborish xatti-harakatlarini oldini olish ( `v-on:submit.prevent`)
* Sahifa yuklangandan keyin voqea faqat bir marta ishlashiga ishonch hosil qiling ( `v-on:click.once`)
* Usulni ishga tushirish uchun hodisa sifatida qaysi klaviatura tugmasidan foydalanishni belgilang ( `v-on:keyup.enter`)
{% endhint %}

### `v-on`Direktivni qanday o'zgartirish kerak

Voqea modifikatorlari voqeaga qanday munosabatda bo'lishni batafsilroq aniqlash uchun ishlatiladi.

Biz hodisa modifikatorlaridan avval ko‘rganimizdek tegni hodisaga ulash orqali foydalanamiz:

```
<button v-on:click="createAlert">Create alert</button>
```

Endi tugmani bosish hodisasi sahifa yuklangandan keyin faqat bir marta yonishi kerakligini aniqroq aniqlash uchun `.once`quyidagi kabi modifikatorni qo'shishimiz mumkin:

```
<button v-on:click.once="createAlert">Create alert</button>
```

Modifikator bilan bir misol `.once`:

Modifikator tegda faqat "klik" hodisasi birinchi marta sodir bo'lganda usulni ishlatish uchun `.once`ishlatiladi .`<button>`

```
<div id="app">
  <p>Click the button to create an alert:</p>
  <button v-on:click.once="creteAlert">Create Alert</button>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    methods: {
      createAlert() {
        alert("Alert created from button click")
      }
    }
  })
  app.mount('#app')
</script>

```

{% hint style="warning" %}
**Eslatma:** Hodisa modifikatorlaridan foydalanish o'rniga hodisani usul ichida boshqarish ham mumkin, ammo voqea modifikatorlari buni ancha osonlashtiradi.
{% endhint %}

### Turli xil `v-on`modifikatorlar

Voqea modifikatorlari turli vaziyatlarda qo'llaniladi. Biz klaviatura hodisalarini, sichqonchani bosish hodisalarini tinglashda hodisa modifikatorlaridan foydalanishimiz mumkin va hatto hodisa modifikatorlarini bir-biri bilan birgalikda ishlatishimiz mumkin.

Hodisa modifikatoridan `.once`klaviatura va sichqonchani bosish hodisalaridan keyin foydalanish mumkin.

### Klaviatura tugmalari hodisasi modifikatorlari

Bizda uch xil klaviatura hodisasi turlari mavjud `keydown`, `keypress`, va `keyup`.

Har bir asosiy hodisa turi bilan biz asosiy voqea sodir bo'lgandan keyin qaysi kalitni tinglashni aniq belgilashimiz mumkin. Bizda `.space`, `.enter`, `.w`va `.up`bir nechtasini nomlash kerak.

`console.log(event.key)`Muayyan kalitning qiymatini o'zingiz topish uchun siz asosiy voqeani veb-sahifaga yoki bilan konsolga yozishingiz mumkin:

Klaviatura `keydown`hodisasi "getKey" usulini ishga tushiradi va hodisa ob'ektidagi "kalit" qiymati konsolga va veb-sahifaga yoziladi.

```
<input v-on:keydown="getKey">
<p> {{ keyValue }} </p>
data() {
  return {
    keyValue = ''
  }
},
methods: {
  getKey(evt) {
    this.keyValue = evt.key
    console.log(evt.key)
  }
}
```

Shuningdek, biz hodisani faqat sichqonchani bosish yoki tugmani bosish tizim o'zgartiruvchi tugmalar bilan birgalikda sodir bo'lganda sodir bo'lishini cheklashni tanlashimiz mumkin `.alt`, yoki . Tizim o'zgartirish tugmasi Windows kompyuterlarida Windows kalitini yoki Apple kompyuterlarida buyruq tugmachasini ifodalaydi.`.ctrl.shift.meta.meta`

| Kalit modifikatorlar           | tafsilotlar                                                                                                                                                                                                                                                                                                                         |
| ------------------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `.[`_`Vue key alias`_`]`       | <p>Eng keng tarqalgan kalitlarning Vue-da o'z taxalluslari mavjud:</p><ul><li><code>.enter</code></li><li><code>.tab</code></li><li><code>.delete</code></li><li><code>.esc</code></li><li><code>.space</code></li><li><code>.up</code></li><li><code>.down</code></li><li><code>.left</code></li><li><code>.right</code></li></ul> |
| `.[`_`letter`_`]`              | Tugmachani bosganingizda keladigan harfni belgilang. Misol sifatida: `.s`"S" tugmachasini tinglash uchun kalit o'zgartirgichdan foydalaning.                                                                                                                                                                                        |
| `.[`_`system modifier key`_`]` | `.alt`, `.ctrl`, `.shift`yoki `.meta`. Bu tugmalar boshqa tugmalar bilan birgalikda yoki sichqonchani bosish bilan birgalikda ishlatilishi mumkin.                                                                                                                                                                                  |

`.s`Foydalanuvchi \<textarea> tegi ichiga 's' yozganda ogohlantirish yaratish uchun modifikatordan foydalaning.

```
<div id="app">
  <p>Try pressing the 's' key:</p>
  <textarea v-on:keyup.s="createAlert"></textarea>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    methods: {
      createAlert() {
        alert("You pressed the 'S' key!")
      }
    }
  })
  app.mount('#app')
</script>
```

### Klaviatura hodisasi modifikatorlarini birlashtiring

Voqea modifikatorlari ham bir-biri bilan birgalikda ishlatilishi mumkin, shuning uchun usul chaqirilishi uchun bir vaqtning o'zida bir nechta narsa sodir bo'lishi kerak.

Teg ichida "s" va "ctrl" bir vaqtning o'zida bosilganda ogohlantirish yaratish uchun `.s`va modifikatorlaridan birgalikda foydalaning .`.ctrl<textarea>`

```
<div id="app">
  <p>Try pressing the 's' key:</p>
  <textarea v-on:keydown.ctrl.s="createAlert"></textarea>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    methods: {
      createAlert() {
        alert("You pressed the 'S' and 'Ctrl' keys, in combination!")
      }
    }
  })
  app.mount('#app')
</script>
```

### Sichqoncha tugmasi modifikatorlari

Sichqonchani bosish bilan reaksiyaga kirishish uchun biz yozishimiz mumkin `v-on:click`, lekin sichqonchaning qaysi tugmasi bosilganligini belgilash uchun , `.left`yoki `.center`modifikatorlardan `.right`foydalanishimiz mumkin.

{% hint style="warning" %}
**Trackpad foydalanuvchilari:** O'ng tugmani yaratish uchun ikkita barmoq bilan yoki kompyuteringizdagi trek panelining pastki o'ng tomonida bosishingiz kerak bo'lishi mumkin.
{% endhint %}

Foydalanuvchi elementni sichqonchaning o'ng tugmasi bilan bosganda fon rangini o'zgartiring `<div>`:

```
<div id="app">
  <div v-on:click.right="changeColor"
       v-bind:style="{backgroundColor:'hsl('+bgColor+',80%,80%)'}">
    <p>Press right mouse button here.</p>
  </div>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        bgColor: 0
      }
    },
    methods: {
      changeColor() {
        this.bgColor+=50
      }
    }
  })
  app.mount('#app')
</script>

```

Sichqoncha tugmasi hodisalari tizimni o'zgartirish tugmasi bilan ham birgalikda ishlashi mumkin.

Foydalanuvchi `<div>`"ctrl" tugmasi bilan elementni o'ng tugmasini bosganida fon rangini o'zgartiring:

```
<div id="app">
  <div v-on:click.right.ctrl="changeColor"
       v-bind:style="{backgroundColor:'hsl('+bgColor+',80%,80%)'}">
    <p>Press right mouse button here.</p>
  </div>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        bgColor: 0
      }
    },
    methods: {
      changeColor() {
        this.bgColor+=50
      }
    }
  })
  app.mount('#app')
</script>

```

O'ng tugmasini bosganimizda standart ochiladigan menyu paydo bo'lishining oldini olish uchun hodisa modifikatori `.prevent`modifikatorga qo'shimcha sifatida ishlatilishi mumkin .`.right`

Elementning fon rangini o'zgartirish uchun sichqonchaning o'ng tugmachasini bosganingizda ochiladigan menyu paydo bo'lishining oldini oladi `<div>`:

```
<div id="app">
  <div v-on:click.right.prevent="changeColor"
       v-bind:style="{backgroundColor:'hsl('+bgColor+',80%,80%)'}">
    <p>Press right mouse button here.</p>
  </div>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        bgColor: 0
      }
    },
    methods: {
      changeColor() {
        this.bgColor+=50
      }
    }
  })
  app.mount('#app')
</script>
```

`event.preventDefault()`Usul ichidan foydalanib, sichqonchaning o'ng tugmachasini bosgandan so'ng ochiladigan menyu paydo bo'lishining oldini olish mumkin edi , lekin Vue `.prevent`modifikatori yordamida kodni o'qish osonroq va saqlash osonroq bo'ladi.

Shuningdek, siz sichqonchaning chap tugmachasini bosish orqali boshqa modifikatorlar bilan birgalikda javob berishingiz mumkin, masalan `click.left.shift`:

`<img>`Tasvirni o'zgartirish uchun "shift" klaviatura tugmachasini ushlab turing va tegdagi sichqonchaning chap tugmasini bosing.

```
<div id="app">
  <p>Hold 'Shift' key and press left mouse button:</p>
  <img v-on:click.left.shift="changeImg" v-bind:src="imgUrl">
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        imgUrlIndex: 0,
        imgUrl: 'img_tiger_square.jpeg',
        imgages: [
          'img_tiger_square.jpeg',
          'img_moose_square.jpeg',
          'img_kangaroo_square.jpeg'
        ]
      }
    },
    methods: {
      changeImg() {
        this.imgUrlIndex++
        if(this.imgUrlIndex>=3){
          this.imgUrlIndex=0
        }
        this.imgUrl = this.images[this.imgUrlIndex]
      }
    }
  })
  app.mount('#app')
</script>
```
