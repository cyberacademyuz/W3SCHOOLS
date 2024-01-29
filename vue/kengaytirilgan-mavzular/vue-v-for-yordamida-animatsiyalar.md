# Vue v-for yordamida animatsiyalar

{% hint style="success" %}
Vue-dagi o'rnatilgan **`<TransitionGroup>`**komponent bizga sahifamizga qo'shilgan elementlarni jonlantirishga yordam beradi `v-for`.
{% endhint %}

### \<TransitionGroup> komponenti

Komponent `<TransitionGroup>`yordamida yaratilgan elementlar atrofida foydalaniladi `v-for`, ular qo'shilgan yoki o'chirilganda ushbu elementlarga individual animatsiyalarni beradi.

`v-for`Komponent ichida yaratilgan teglar atribut `<TransitionGroup>`bilan aniqlanishi kerak `key`.

Komponent `<TransitionGroup>`faqat HTML yorlig'i sifatida ko'rsatiladi, agar biz uni rekvizit yordamida ma'lum bir teg sifatida aniqlasak `tag`, masalan:

```html
<TransitionGroup tag="ol">
  <li v-for="x in products" :key="x">
    {{ x }}
  </li>
</TransitionGroup>
```

Bu Vue tomonidan ko'rsatilganidan keyin yuqoridagi kodning natijasi:

```html
<ol>
  <li>Apple</li>
  <li>Pizza</li>
  <li>Rice</li>
</ol>
```

Roʻyxatga yangi elementlar qoʻshilganda ularni jonlantirish uchun endi biz CSS kodini qoʻshishimiz mumkin:

```html
<style>
  .v-enter-from {
    opacity: 0;
    rotate: 180deg;
  }
  .v-enter-to {
    opacity: 1;
    rotate: 0deg;
  }
  .v-enter-active {
    transition: all 0.7s;
  }
</style>
```

Ushbu misolda, yangi elementlar ularni "mahsulotlar" qatoriga qo'shish orqali jonlantiriladi:

{% code title="App.vue:" %}
```html
<template>
  <h3>The <TransitionGroup> Component</h3>
  <p>New products are given animations using the <TransitionGroup> component.</p>
  <input type="text" v-model="inpName"> 
  <button @click="addEl">Add</button>
  <TransitionGroup tag="ol">
    <li v-for="x in products" :key="x">
      {{ x }}
    </li>
  </TransitionGroup>
</template>

<script>
  export default {
    data() {
      return {
        products: ['Apple','Pizza','Rice'],
        inpName: ''
      }
    },
    methods: {
      addEl() {
        const el = this.inpName;
        this.products.push(el);
        this.inpName = null;
      }
    }
  }
</script>

<style>
  .v-enter-from {
    opacity: 0;
    rotate: 180deg;
  }
  .v-enter-to {
    opacity: 1;
    rotate: 0deg;
  }
  .v-enter-active {
    transition: all 0.7s;
  }
</style>
```
{% endcode %}

### Elementlarni qo'shish va o'chirish

Boshqa elementlar orasidagi elementlarni olib tashlashda, boshqa elementlar olib tashlangan element joyiga tushadi. Element o'chirilganda qolgan ro'yxat elementlari qanday joylashishini jonlantirish uchun biz avtomatik ravishda yaratilgan `v-move`sinfdan foydalanamiz.

Lekin, avvalo, element olib tashlanganida boshqa elementlarning qanday joylashishi jonlantirilmaydigan **misolni** ko'rib chiqaylik:

{% code title="App.vue:" %}
```html
<template>
  <h3>The <TransitionGroup> Component</h3>
  <p>New products are given animations using the <TransitionGroup> component.</p>
  <button @click="addDie">Roll</button>
  <button @click="removeDie">Remove random</button><br>
  <TransitionGroup>
    <div v-for="x in dice" :key="x" class="diceDiv" :style="{ backgroundColor: 'hsl('+x*40+',85%,85%)' }">
      {{ x }}
    </div>
  </TransitionGroup>
</template>

<script>
  export default {
    data() {
      return {
        dice: [],
        inpName: ''
      }
    },
    methods: {
      addDie() {
        const newDie = Math.ceil(Math.random()*6);
        this.dice.push(newDie);
      },
      removeDie() {
        if(this.dice.length>0){
          this.dice.splice(Math.floor(Math.random()*this.dice.length), 1);
        }
      }
    },
    mounted() {
      this.addDie();
      this.addDie();
      this.addDie();
    }
  }
</script>

<style>
.v-enter-from {
  opacity: 0;
  translate: 200px 0;
  rotate: 360deg;
}
.v-enter-to {
  opacity: 1;
  translate: 0 0;
  rotate: 0deg;
}
.v-enter-active,
.v-leave-active {
  transition: all 0.7s;
}
.v-leave-from { opacity: 1; }
.v-leave-to { opacity: 0; }
.diceDiv {
  margin: 10px;
  width: 30px;
  height: 30px;
  line-height: 30px;
  vertical-align: middle;
  text-align: center;
  border: solid black 1px;
  border-radius: 5px;
  display: inline-block;
}
</style>
```
{% endcode %}

Yuqoridagi misolda ko'rib turganingizdek, biror narsa olib tashlanganida, olib tashlangan elementdan keyingi elementlar birdan yangi joylariga o'tadi. Element o'chirilganda qolgan elementlarni jonlantirish uchun biz avtomatik ravishda yaratilgan `v-move`sinfdan foydalanamiz.

Olib tashlangan element tark etayotganda sinf `v-move`boshqa elementlarni jonlantiradi, lekin bitta muammo bor: oʻchirilgan element hali ham mavjud va u oʻchirilgunga qadar oʻz oʻrnini egallaydi, shuning uchun sinf hech qanday taʼsir koʻrsatmaydi `v-move`. `v-move`Sinfga jonlantirish uchun biror narsa berish uchun biz `position: absolute;`sinfni sozlashimiz mumkin `v-leave-active`. Olib tashlash davrida o'rnatilgan bo'lsa `position: absolute;`, o'chirilgan element hali ham ko'rinadi, lekin o'z o'rnini egallamaydi.

Ushbu misolda oldingi misoldan yagona farq 14 va 17 qatorlarga qo'shilgan ikkita yangi CSS sinfidir:

{% code title="App.vue:" %}
```html
<style>
.v-enter-from {
  opacity: 0;
  translate: 200px 0;
  rotate: 360deg;
}
.v-enter-to {
  opacity: 1;
  translate: 0 0;
  rotate: 0deg;
}
.v-enter-active,
.v-leave-active,
.v-move {
  transition: all 0.7s;
}
.v-leave-active { position: absolute; }
.v-leave-from { opacity: 1; }
.v-leave-to { opacity: 0; }
.diceDiv {
  margin: 10px;
  width: 30px;
  height: 30px;
  line-height: 30px;
  vertical-align: middle;
  text-align: center;
  border: solid black 1px;
  border-radius: 5px;
  display: inline-block;
}
</style>
```
{% endcode %}

### Kattaroq misol

Yuqoridagi misolni yangi misol uchun asos qilib olaylik.

Ushbu misolda yangi element qo'shilganda yoki o'chirilganda yoki butun massiv tartiblanganda butun ro'yxat qanday jonlantirilganligi yanada aniqroq bo'ladi.

Ushbu misolda biz:

* Elementlarni ustiga bosish orqali olib tashlang
* Elementlarni tartiblang
* Ro'yxatning tasodifiy joyiga yangi narsalarni qo'shing

{% code title="App.vue:" %}
```html
<template>
  <h3>The <TransitionGroup> Component</h3>
  <p>Items inside the <TransitionGroup> component are animated when they are created or removed.</p>
  <button @click="addDie">Roll</button>
  <button @click="addDie10">Roll 10 dice</button>
  <button @click="dice.sort(compareFunc)">Sort</button>
  <button @click="dice.sort(shuffleFunc)">Shuffle</button><br>
  <TransitionGroup>
    <div 
    v-for="x in dice" 
    :key="x.keyNmbr" 
    class="diceDiv" 
    :style="{ backgroundColor: 'hsl('+x.dieNmbr*60+',85%,85%)' }"
    @click="removeDie(x.keyNmbr)">
      {{ x.dieNmbr }}
    </div>
  </TransitionGroup>
</template>

<script>
  export default {
    data() {
      return {
        dice: [],
        keyNumber: 0
      }
    },
    methods: {
      addDie() {
        const newDie = {
          dieNmbr: Math.ceil(Math.random()*6),
          keyNmbr: this.keyNumber
        };
        this.dice.splice(Math.floor(Math.random()*this.dice.length),0,newDie);
        this.keyNumber++;
      },
      addDie10() {
        for(let i=0; i<10; i++) {
          this.addDie();
        }
      },
      compareFunc(a,b){
        return a.dieNmbr - b.dieNmbr;
      },
      shuffleFunc(a,b){
        return Math.random()-0.5;
      },
      removeDie(key) {
        const pos = this.dice.map(e => e.keyNmbr).indexOf(key);
        this.dice.splice(pos, 1);
      }
    },
    mounted() {
      this.addDie10();
    }
  }
</script>

<style>
.v-enter-from {
  opacity: 0;
  scale: 0;
  rotate: 360deg;
}
.v-enter-to {
  opacity: 1;
  scale: 1;
  rotate: 0deg;
}
.v-enter-active,
.v-leave-active,
.v-move {
  transition: all 0.7s;
}
.v-leave-active { position: absolute; }
.v-leave-from { opacity: 1; }
.v-leave-to { opacity: 0; }
.diceDiv {
  margin: 10px;
  width: 30px;
  height: 30px;
  line-height: 30px;
  vertical-align: middle;
  text-align: center;
  border: solid black 1px;
  border-radius: 5px;
  display: inline-block;
}
.diceDiv:hover {
  cursor: pointer;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
}
#app {
  position: relative;
}
</style>
```
{% endcode %}
