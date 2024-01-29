# Vue Animatsiyalar

{% hint style="success" %}
Vue-dagi o'rnatilgan komponent bizga elementlar yoki komponentlar **`<Transition>`**bilan qo'shilgan yoki o'chirilganda animatsiya qilishimizga yordam beradi `v-if`.`v-show`

Boshqa hollarda oddiy CSS o'tishlari va animatsiyalaridan foydalanishda hech qanday yomon narsa yo'q.
{% endhint %}

### CSS o'tish va animatsiyaga qisqacha kirish

Qo'llanmaning ushbu qismi asosiy CSS [animatsiyalari](https://www-w3schools-com.translate.goog/css/css3\_animations.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) va [o'tishlari](https://www-w3schools-com.translate.goog/css/css3\_transitions.asp?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) haqida bilimlarni talab qiladi .

Ammo animatsiyalarni yaratish uchun Vue-ga xos o'rnatilgan `<Transition>`komponentdan foydalanishdan oldin, keling, oddiy CSS animatsiyalari va o'tishlarini Vue bilan qanday ishlatish mumkinligiga ikkita misolni ko'rib chiqaylik.

{% code title="App.vue:" %}
```html
<template>
  <h1>Basic CSS Transition</h1>
  <button @click="this.doesRotate = true">Rotate</button>
  <div :class="{ rotate: doesRotate }"></div>
</template>

<script>
export default {
  data() {
    return {
      doesRotate: false
    }
  }
}
</script>

<style scoped>
  .rotate {
    rotate: 160deg;
    transition: rotate 1s;
  }
  div {
    border: solid black 2px;
    background-color: lightcoral;
    width: 60px;
    height: 60px;
  }
  h1, button, div {
    margin: 10px;
  }
</style> 
```
{% endcode %}

Yuqoridagi misolda biz tegga aylanish uchun sinf `v-bind`berish uchun foydalanamiz. `<div>`Aylanish 1 soniya davom etishining sababi, u CSS `transition`xususiyati bilan aniqlangan.

Quyidagi misolda biz ob'ektni CSS `animation`xususiyati bilan qanday ko'chirishimiz mumkinligini ko'rib chiqamiz.

{% code title="App.vue:" %}
```html
<template>
  <h1>Basic CSS Animation</h1>
  <button @click="this.doesMove = true">Start</button>
  <div :class="{ move: doesMove }"></div>
</template>

<script>
export default {
  data() {
    return {
      doesMove: false
    }
  }
}
</script>

<style scoped>
  .move {
    animation: move .5s alternate 4 ease-in-out;
  }
  @keyframes move {
    from {
      translate: 0 0;
    }
    to {
      translate: 70px 0;
    }
  }
  div {
    border: solid black 2px;
    background-color: lightcoral;
    border-radius: 50%;
    width: 60px;
    height: 60px;
  }
  h1, button, div {
    margin: 10px;
  }
</style>
```
{% endcode %}

### \<Transition> komponenti

Yuqoridagi ikkita misolda bo'lgani kabi oddiy CSS o'tishlari va animatsiyalaridan foydalanishda hech qanday yomon narsa yo'q.

Yaxshiyamki, Vue bizga o‘rnatilgan `<Transition>`komponentni taqdim etadi, agar biz elementni ilovamizdan olib tashlangan yoki ilovamizga qo‘shilgan holda `v-if`yoki bilan jonlantirmoqchi bo‘lsak `v-show`, chunki buni oddiy CSS animatsiyasi bilan qilish qiyin.

Avval tugma teg qo'shadigan yoki olib tashlaydigan dastur yarataylik `<p>`:

{% code title="App.vue:" %}
```html
<template>
  <h1>Add/Remove <p> Tag</h1>
  <button @click="this.exists = !this.exists">{{btnText}}</button><br>
  <p v-if="exists">Hello World!</p>
</template>

<script>
export default {
  data() {
    return {
      exists: false
    }
  },
  computed: {
    btnText() {
      if(this.exists) {
        return 'Remove';
      }
      else {
        return 'Add';
      }
    }
  }
}
</script>

<style scoped>
  p {
    background-color: lightgreen;
    display: inline-block;
    padding: 10px;
  }
</style>
```
{% endcode %}

`<Transition>`Keling, komponentni teg atrofida o'rab olamiz `<p>`va tegni olib tashlashni qanday jonlantirishimiz mumkinligini ko'rib chiqamiz `<p>`.

Komponentdan foydalanganda `<Transition>`biz avtomatik ravishda elementlar qo'shilgan yoki o'chirilganda jonlantirish uchun foydalanishimiz mumkin bo'lgan olti xil CSS sinfini olamiz.

Quyidagi misolda biz avtomatik ravishda mavjud bo'lgan sinflardan foydalanamiz `v-leave-from`va teg o'chirilganda `v-leave-to`o'chib ketadigan animatsiyani yaratamiz :`<p>`

{% code title="App.vue:" %}
```html
<template>
  <h1>Add/Remove <p> Tag</h1>
  <button @click="this.exists = !this.exists">{{btnText}}</button><br>
  <Transition>
    <p v-if="exists">Hello World!</p>
  </Transition>
</template>

<script>
export default {
  data() {
    return {
      exists: false
    }
  },
  computed: {
    btnText() {
      if(this.exists) {
        return 'Remove';
      }
      else {
        return 'Add';
      }
    }
  }
}
</script>

<style scoped>
  .v-leave-from {
    opacity: 1;
  }
  .v-leave-to {
    opacity: 0;
  }
  p {
    background-color: lightgreen;
    display: inline-block;
    padding: 10px;
    transition: opacity 0.5s;
  }
</style>
```
{% endcode %}

### Oltita \<O'tish> sinfi

Komponentdan foydalanganda biz uchun avtomatik ravishda oltita sinf mavjud `<Transition>`.

`<Transition>`Komponent ichidagi element **qo'shilganligi** sababli , biz ushbu o'tishni jonlantirish uchun ushbu birinchi uchta sinfdan foydalanishimiz mumkin:

1. v-kirish-dan
2. v-kirish-faol
3. v-kirish

Komponent ichida element **olib tashlanganligi**`<Transition>` sababli biz keyingi uchta sinfdan foydalanishimiz mumkin:

4. v-dan ketish
5. v-ketmoq-faol
6. v-qoldirish

**Eslatma:** Komponentning ildiz darajasida faqat bitta element bo'lishi mumkin `<Transition>`.

`<p>`Keling, teg qo'shilganda ham, o'chirilganda ham jonlantirishimiz uchun ushbu sinflarning to'rttasidan foydalanamiz .

{% code title="App.vue:" %}
```html
<template>
  <h1>Add/Remove <p> Tag</h1>
  <button @click="this.exists = !this.exists">{{btnText}}</button><br>
  <Transition>
    <p v-if="exists">Hello World!</p>
  </Transition>
</template>

<script>
export default {
  data() {
    return {
      exists: false
    }
  },
  computed: {
    btnText() {
      if(this.exists) {
        return 'Remove';
      }
      else {
        return 'Add';
      }
    }
  }
}
</script>

<style scoped>
  .v-enter-from {
    opacity: 0;
    translate: -100px 0;
  }
  .v-enter-to {
    opacity: 1;
    translate: 0 0;
  }
  .v-leave-from {
    opacity: 1;
    translate: 0 0;
  }
  .v-leave-to {
    opacity: 0;
    translate: 100px 0;
  }
  p {
    background-color: lightgreen;
    display: inline-block;
    padding: 10px;
    transition: all 0.5s;
  }
</style>
```
{% endcode %}

Elementni **qo‘shish** yoki **olib tashlash vaqtida** uslub yoki animatsiyani o‘rnatish uchun ham `v-enter-active`va tugmalaridan foydalanishimiz mumkin :`v-leave-active`

{% code title="App.vue:" %}
```html
<template>
  <h1>Add/Remove <p> Tag</h1>
  <button @click="this.exists = !this.exists">{{btnText}}</button><br>
  <Transition>
    <p v-if="exists">Hello World!</p>
  </Transition>
</template>

<script>
export default {
  data() {
    return {
      exists: false
    }
  },
  computed: {
    btnText() {
      if(this.exists) {
        return 'Remove';
      }
      else {
        return 'Add';
      }
    }
  }
}
</script>

<style scoped>
  .v-enter-active {
    background-color: lightgreen;
    animation: added 1s;
  }
  .v-leave-active {
    background-color: lightcoral;
    animation: added 1s reverse;
  }
  @keyframes added {
    from {
      opacity: 0;
      translate: -100px 0;
    }
    to {
      opacity: 1;
      translate: 0 0;
    }
  }
  p {
    display: inline-block;
    padding: 10px;
    border: dashed black 1px;
  }
</style>
```
{% endcode %}

### O'tish "nomi" Prop

Agar sizda bir nechta `<Transition>`komponentlar mavjud bo'lsa-da, lekin siz kamida bitta `<Transition>`komponent boshqa animatsiyaga ega bo'lishini istasangiz, `<Transition>`ularni bir-biridan ajratish uchun komponentlar uchun turli nomlar kerak bo'ladi.

`<Transition>`Biz rekvizit bilan komponent nomini tanlashimiz mumkin `name`va bu o'tish sinflarining nomini ham o'zgartiradi, shuning uchun biz ushbu komponent uchun turli CSS animatsiya qoidalarini o'rnatishimiz mumkin.

```html
<Transition name="swirl">
```

Agar o'tish prop qiymati **'swirl'**`name` ga o'rnatilgan bo'lsa , avtomatik ravishda mavjud sinflar endi **'v-'** o'rniga **'swirl-'** bilan boshlanadi :

1. **aylanma** -kirish-dan
2. **swirl** -enter-faol
3. **aylanish** -kirish
4. **aylanma** - tark etmoq
5. **aylanma** - tark etish - faol
6. **aylanma** - tark etmoq

Quyidagi misolda biz komponentlarga turli animatsiyalarni `name`berish uchun tayanchdan foydalanamiz. `<Transition>`Bitta `<Transition>`komponentga nom berilmagan va shuning uchun "v-" bilan boshlanadigan avtomatik ravishda yaratilgan CSS sinflari yordamida animatsiyalar beriladi. Boshqa `<Transition>`komponentga "swirl" nomi berilgan, shuning uchun unga "swirl-" bilan boshlanadigan avtomatik ravishda yaratilgan CSS sinflari bilan animatsiya qoidalari berilishi mumkin.

{% code title="App.vue:" %}
```html
<template>
  <h1>Add/Remove <p> Tag</h1>
  <p>The second transition in this example has the name prop "swirl", so that we can keep the transitions apart with different class names.</p>
  <hr>
  <button @click="this.p1Exists = !this.p1Exists">{{btn1Text}}</button><br>
  <Transition>
    <p v-if="p1Exists" id="p1">Hello World!</p>
  </Transition>
  <hr>
  <button @click="this.p2Exists = !this.p2Exists">{{btn2Text}}</button><br>
  <Transition name="swirl">
    <p v-if="p2Exists" id="p2">Hello World!</p>
  </Transition>
</template>

<script>
export default {
  data() {
    return {
      p1Exists: false,
      p2Exists: false
    }
  },
  computed: {
    btn1Text() {
      if(this.p1Exists) {
        return 'Remove';
      }
      else {
        return 'Add';
      }
    },
    btn2Text() {
      if(this.p2Exists) {
        return 'Remove';
      }
      else {
        return 'Add';
      }
    }
  }
}
</script>

<style scoped>
  .v-enter-active {
    background-color: lightgreen;
    animation: added 1s;
  }
  .v-leave-active {
    background-color: lightcoral;
    animation: added 1s reverse;
  }
  @keyframes added {
    from {
      opacity: 0;
      translate: -100px 0;
    }
    to {
      opacity: 1;
      translate: 0 0;
    }
  }
  .swirl-enter-active {
    animation: swirlAdded 1s;
  }
  .swirl-leave-active {
    animation: swirlAdded 1s reverse;
  }
  @keyframes swirlAdded {
    from {
      opacity: 0;
      rotate: 0;
      scale: 0.1;
    }
    to {
      opacity: 1;
      rotate: 360deg;
      scale: 1;
    }
  }
  #p1, #p2 {
    display: inline-block;
    padding: 10px;
    border: dashed black 1px;
  }
  #p2 {
    background-color: lightcoral;
  }
</style>
```
{% endcode %}

### JavaScript o'tish ilgaklari

Yuqorida aytib o'tilganidek, har bir Transition klassi biz ba'zi JavaScript kodlarini ishga tushirishimiz mumkin bo'lgan voqeaga mos keladi.

| Transition Class | JavaScript Event                                                              |
| ---------------- | ----------------------------------------------------------------------------- |
| v-enter-from     | `before-enter`                                                                |
| v-enter-active   | `enter`                                                                       |
| v-enter-to       | <p><code>after-enter</code><br><code>enter-cancelled</code></p>               |
| v-leave-from     | `before-leave`                                                                |
| v-leave-active   | `leave`                                                                       |
| v-leave-to       | <p><code>after-leave</code><br><code>leave-cancelled</code> (v-show only)</p> |

`after-enter`Quyidagi misolda voqea sodir bo'lganda, qizil elementni ko'rsatadigan usul ishlaydi `<div>`.

{% code title="App.vue:" %}
```html
<template>
  <h1>JavaScript Transition Hooks</h1>
  <p>This code hooks into "after-enter" so that after the initial animation is done, a method runs that displays a red div.</p>
  <button @click="pVisible=true">Create p-tag!</button><br>
  <Transition @after-enter="onAfterEnter">
    <p v-show="pVisible" id="p1">Hello World!</p>
  </Transition>
  <br>
  <div v-show="divVisible">This appears after the "enter-active" phase of the transition.</div>
</template>

<script>
export default {
  data() {
    return {
      pVisible: false,
      divVisible: false
    }
  },
  methods: {
    onAfterEnter() {
      this.divVisible = true;
    }
  }
}
</script>

<style scoped>
  .v-enter-active {
    animation: swirlAdded 1s;
  }
  @keyframes swirlAdded {
    from {
      opacity: 0;
      rotate: 0;
      scale: 0.1;
    }
    to {
      opacity: 1;
      rotate: 360deg;
      scale: 1;
    }
  }
  #p1, div {
    display: inline-block;
    padding: 10px;
    border: dashed black 1px;
  }
  #p1 {
    background-color: lightgreen;
  }
  div {
    background-color: lightcoral;
  }
</style>
```
{% endcode %}

Hodisa ishga tushishi `<p>`uchun elementning oʻtish bosqichini toʻxtatish uchun quyidagi misoldagi “Oʻchirish” tugmasidan foydalanishingiz mumkin :`enter-cancelled`

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'enter-cancelled' Event</h1>
  <p>Click the toggle button again before the enter animation is finished to trigger the 'enter-cancelled' event.</p>
  <button @click="pVisible=!pVisible">Toggle</button><br>
  <Transition @enter-cancelled="onEnterCancelled">
    <p v-if="pVisible" id="p1">Hello World!</p>
  </Transition>
  <br>
  <div v-if="divVisible">You interrupted the "enter-active" transition.</div>
</template>

<script>
export default {
  data() {
    return {
      pVisible: false,
      divVisible: false
    }
  },
  methods: {
    onEnterCancelled() {
      this.divVisible = true;
    }
  }
}
</script>

<style scoped>
  .v-enter-active {
    animation: swirlAdded 2s;
  }
  @keyframes swirlAdded {
    from {
      opacity: 0;
      rotate: 0;
      scale: 0.1;
    }
    to {
      opacity: 1;
      rotate: 720deg;
      scale: 1;
    }
  }
  #p1, div {
    display: inline-block;
    padding: 10px;
    border: dashed black 1px;
  }
  #p1 {
    background-color: lightgreen;
  }
  div {
    background-color: lightcoral;
  }
</style>
```
{% endcode %}

### "Ko'rinish" tayanchi

`appear`Agar bizda sahifa yuklanganda jonlantirmoqchi bo'lgan elementimiz bo'lsa, komponentdagi rekvizitdan foydalanishimiz kerak `<Transition>`.

```html
<Transition appear>
  ...
</Transition>
```

Ushbu misolda `appear`rekvizit sahifa birinchi marta yuklanganda animatsiyani boshlaydi:

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'appear' Prop</h1>
  <p>The 'appear' prop starts the animation when the p tag below is rendered for the first time as the page opens. Without the 'appear' prop, this example would have had no animation.</p>
  <Transition appear>
    <p id="p1">Hello World!</p>
  </Transition>
</template>

<style scoped>
  .v-enter-active {
    animation: swirlAdded 1s;
  }
  @keyframes swirlAdded {
    from {
      opacity: 0;
      rotate: 0;
      scale: 0.1;
    }
    to {
      opacity: 1;
      rotate: 360deg;
      scale: 1;
    }
  }
  #p1 {
    display: inline-block;
    padding: 10px;
    border: dashed black 1px;
    background-color: lightgreen;
  }
</style>
```
{% endcode %}

### Elementlar orasidagi o'tish

Komponentdan bir nechta elementlar o'rtasida almashish uchun ham foydalanish mumkin, agar biz va `<Transition>`yordamida bir vaqtning o'zida faqat bitta element ko'rsatilishiga ishonch hosil qilamiz :`<v-if><v-else-if>`

{% code title="App.vue:" %}
```html
<template>
  <h1>Transition Between Elements</h1>
  <p>Click the button to get a new image.</p>
  <p>The new image is added before the previous is removed. We will fix this in the next example with mode="out-in".</p>
  <button @click="newImg">Next image</button><br>
  <Transition>
    <img src="/img_pizza.svg" v-if="imgActive === 'pizza'">
    <img src="/img_apple.svg" v-else-if="imgActive === 'apple'">
    <img src="/img_cake.svg" v-else-if="imgActive === 'cake'">
    <img src="/img_fish.svg" v-else-if="imgActive === 'fish'">
    <img src="/img_rice.svg" v-else-if="imgActive === 'rice'">
  </Transition>
</template>

<script>
export default {
  data() {
    return {
      imgActive: 'pizza',
      imgs: ['pizza', 'apple', 'cake', 'fish', 'rice'],
      indexNbr: 0
    }
  },
  methods: {
    newImg() {
      this.indexNbr++;
      if(this.indexNbr >= this.imgs.length) {
        this.indexNbr = 0;
      }
      this.imgActive = this.imgs[this.indexNbr];
    }
  }
}
</script>

<style scoped>
  .v-enter-active {
    animation: swirlAdded 1s;
  }
  .v-leave-active {
    animation: swirlAdded 1s reverse;
  }
  @keyframes swirlAdded {
    from {
      opacity: 0;
      rotate: 0;
      scale: 0.1;
    }
    to {
      opacity: 1;
      rotate: 360deg;
      scale: 1;
    }
  }
  img {
    width: 100px;
    margin: 20px;
  }
  img:hover {
    cursor: pointer;
  }
</style> 
```
{% endcode %}

### mode="chiqish"

Yuqoridagi misolda oldingi rasm o'chirilishidan oldin keyingi rasm qo'shiladi.

Biz `mode="out-in"`komponentda prop va prop qiymatidan foydalanamiz `<Transition>`, shunda elementni olib tashlash keyingi element qo'shilishidan oldin tugaydi.

ga qo'shimcha ravishda `mode="out-in"`, bu misolda biz oldingi misolda ishlatgan "newImg" usuli o'rniga "imgActive" hisoblangan qiymati ham qo'llaniladi.

{% code title="App.vue:" %}
```html
<template>
  <h1>mode="out-in"</h1>
  <p>Click the button to get a new image.</p>
  <p>With mode="out-in", the next image is not added until the current image is removed. Another difference from the previous example, is that here we use computed prop instead of a method.</p>
  <button @click="indexNbr++">Next image</button><br>
  <Transition mode="out-in">
    <img src="/img_pizza.svg" v-if="imgActive === 'pizza'">
    <img src="/img_apple.svg" v-else-if="imgActive === 'apple'">
    <img src="/img_cake.svg" v-else-if="imgActive === 'cake'">
    <img src="/img_fish.svg" v-else-if="imgActive === 'fish'">
    <img src="/img_rice.svg" v-else-if="imgActive === 'rice'">
  </Transition>
</template>

<script>
export default {
  data() {
    return {
      imgs: ['pizza', 'apple', 'cake', 'fish', 'rice'],
      indexNbr: 0
    }
  },
  computed: {
    imgActive() {
      if(this.indexNbr >= this.imgs.length) {
        this.indexNbr = 0;
      }
      return this.imgs[this.indexNbr];
    }
  }
}
</script>

<style scoped>
  .v-enter-active {
    animation: swirlAdded 0.7s;
  }
  .v-leave-active {
    animation: swirlAdded 0.7s reverse;
  }
  @keyframes swirlAdded {
    from {
      opacity: 0;
      rotate: 0;
      scale: 0.1;
    }
    to {
      opacity: 1;
      rotate: 360deg;
      scale: 1;
    }
  }
  img {
    width: 100px;
    margin: 20px;
  }
  img:hover {
    cursor: pointer;
  }
</style>
```
{% endcode %}

### Dinamik komponentlar bilan o'tish

Dinamik komponentlar o'rtasida almashishni jonlantirish uchun komponentdan ham foydalanishimiz mumkin `<Transition>`:

{% code title="App.vue:" %}
```html
<template>
  <h1>Transition with Dynamic Components</h1>
  <p>The Transition component wraps around the dynamic component so that the switching can be animated.</p>
  <button @click="toggleValue = !toggleValue">Switch component</button>
  <Transition mode="out-in">
    <component :is="activeComp"></component>
  </Transition>
</template>

<script>
  export default {
    data () {
      return {
        toggleValue: true
      }
    },
    computed: {
      activeComp() {
        if(this.toggleValue) {
          return 'comp-one'
        }
        else {
          return 'comp-two'
        }
      }
    }
  }
</script>

<style>
  .v-enter-active {
    animation: slideIn 0.5s;
  }
  @keyframes slideIn {
    from {
      translate: -200px 0;
      opacity: 0;
    }
    to {
      translate: 0 0;
      opacity: 1;
    }
  }
  .v-leave-active {
    animation: slideOut 0.5s;
  }
  @keyframes slideOut {
    from {
      translate: 0 0;
      opacity: 1;
    }
    to {
      translate: 200px 0;
      opacity: 0;
    }
  }
  #app {
    width: 350px;
    margin: 10px;
  }
  #app > div {
    border: solid black 2px;
    padding: 10px;
    margin-top: 10px;
  }
</style>
```
{% endcode %}
