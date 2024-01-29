# Vue Dinamik komponentlar

{% hint style="success" %}
**Dinamik komponentlar** brauzeringizdagi yorliqlar kabi sahifangizdagi sahifalarni "is" atributidan foydalangan holda aylantirish uchun ishlatilishi mumkin.
{% endhint %}

### Komponent tegi va "is" atributi

Dinamik komponentni yaratish uchun biz `<component>`faol komponentni ifodalash uchun tegdan foydalanamiz. 'is' atributi bilan qiymatga bog'langan `v-bind`va biz bu qiymatni faol bo'lishini xohlagan komponent nomiga o'zgartiramiz.

Ushbu misolda bizda komponent yoki komponent `<component>`uchun to'ldiruvchi vazifasini bajaradigan teg mavjud . 'is' atributi tegda o'rnatiladi va qiymat sifatida 'komp-bir' yoki 'komp-ikki' ni ushlab turadigan 'activeComp' hisoblangan qiymatini tinglaydi. Va bizda faol komponentlar o'rtasida hisoblangan qiymatni almashtirish uchun ma'lumotlar xususiyatini "to'g'ri" va "noto'g'ri" o'rtasida almashtiruvchi tugma mavjud.`comp-onecomp-two<component>`

{% code title="App.vue:" %}
```html
<template>
  <h1>Dynamic Components</h1>
  <p>App.vue switches between which component to show.</p>
  <button @click="toggleValue = !toggleValue">
    Switch component
  </button>
  <component :is="activeComp"></component>
</template>

<script>
  export default {
    data() {
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
```
{% endcode %}

### \<Jonli turing>

Quyidagi misolni bajaring. Qayta o'tganingizda, bitta komponentda kiritilgan o'zgarishlar unutilganini sezasiz. Buning sababi, komponent o'chirilgan va qayta o'rnatilgan bo'lib, komponent qayta yuklanadi.

Ushbu misol oldingi misol bilan bir xil, faqat komponentlar boshqacha. Siz `comp-one`"Olma" va "Cake" o'rtasida tanlov qilishingiz va `comp-two`xabar yozishingiz mumkin. Komponentga qaytganingizda ma'lumotlaringiz yo'qoladi.

Oldingi kiritilgan ma'lumotlarning holatini saqlab qolish uchun komponentga qaytishda teg `<KeepAlive>`atrofidagi tegdan foydalanamiz `<component>`.

Endi komponentlar foydalanuvchi kiritishlarini eslab qoladi.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h1>Dynamic Components&#x3C;/h1>
  &#x3C;p>App.vue switches between which component to show.&#x3C;/p>
  &#x3C;button @click="toggleValue = !toggleValue">
    Switch component
  &#x3C;/button>
<strong>  &#x3C;KeepAlive>
</strong>    &#x3C;component :is="activeComp">&#x3C;/component>
<strong>  &#x3C;/KeepAlive>
</strong>&#x3C;/template>
</code></pre>

### "O'z ichiga" va "tashqariga qo'yish" atributlari

Teg ichidagi barcha komponentlar `<KeepAlive>`sukut bo'yicha tirik qoladi.

Ammo biz tegdagi "o'z ichiga" yoki "chiqib qo'yish" atributlaridan foydalanib, faqat tirik qolish uchun ba'zi komponentlarni aniqlashimiz mumkin `<KeepAlive>`.

Agar tegda “include” yoki “chisted” atributlaridan foydalansak, `<KeepAlive>`“nom” varianti bilan komponentlar nomlarini ham berishimiz kerak:

<pre class="language-html" data-title="CompOne.vue:"><code class="lang-html">&#x3C;script>
  export default {
<strong>    name: 'CompOne',
</strong>    data() {
      return {
        imgSrc: 'img_question.svg'
      }
    }
  }
&#x3C;/script>
 
</code></pre>

, bilan `<KeepAlive include="CompOne">`faqat 'CompOne' komponenti o'z holatini, oldingi kiritilgan ma'lumotlarni eslab qoladi.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h1>Dynamic Components&#x3C;/h1>
  &#x3C;p>App.vue switches between which component to show.&#x3C;/p>
  &#x3C;button @click="toggleValue = !toggleValue">
    Switch component
  &#x3C;/button>
<strong>  &#x3C;KeepAlive include="CompOne">
</strong>    &#x3C;component :is="activeComp">&#x3C;/component>
<strong>  &#x3C;/KeepAlive>
</strong>&#x3C;/template>
</code></pre>

Qaysi komponentlarni saqlab qolish yoki yo'qligini tanlash uchun "chiqib chiqarish" dan ham foydalanishimiz mumkin.

, faqat `<KeepAlive exclude="CompOne">`"CompTwo" komponenti uning holatini eslab qoladi.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h1>Dynamic Components&#x3C;/h1>
  &#x3C;p>App.vue switches between which component to show.&#x3C;/p>
  &#x3C;button @click="toggleValue = !toggleValue">
    Switch component
  &#x3C;/button>
<strong>  &#x3C;KeepAlive exclude="CompOne">
</strong>    &#x3C;component :is="activeComp">&#x3C;/component>
<strong>  &#x3C;/KeepAlive>
</strong>&#x3C;/template> 
</code></pre>

Ikkala "o'z ichiga" va "tashqariga qo'yish" bir nechta komponentlar bilan vergul bilan ajratish orqali ishlatilishi mumkin.

Buni ko'rsatish uchun biz yana bitta komponentni qo'shamiz, shunda biz jami uchta komponentni olamiz.

bilan `<KeepAlive include="CompOne, CompThree">`"CompOne" va "CompThree" komponentlari o'z holatini eslab qoladi.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h1>Dynamic Components&#x3C;/h1>
  &#x3C;button @click="compNbr++">
    Next component
  &#x3C;/button>
<strong>  &#x3C;KeepAlive include="CompOne,CompThree">
</strong>    &#x3C;component :is="activeComp">&#x3C;/component>
<strong>  &#x3C;/KeepAlive>
</strong>&#x3C;/template>
</code></pre>

### "Maksimum" atributlari

`<KeepAlive>`Brauzer holatini eslab qolishi kerak bo'lgan komponentlar sonini cheklash uchun tegning atributi sifatida "max" dan foydalanishimiz mumkin .

, brauzer `<KeepAlive :max="2">`faqat oxirgi tashrif buyurilgan ikkita komponentning foydalanuvchi kiritishini eslab qoladi.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h1>Dynamic Components&#x3C;/h1>
  &#x3C;label>&#x3C;input type="radio" name="rbgComp" v-model="compName" :value="'comp-one'"> One&#x3C;/label>
  &#x3C;label>&#x3C;input type="radio" name="rbgComp" v-model="compName" :value="'comp-two'"> Two&#x3C;/label>
  &#x3C;label>&#x3C;input type="radio" name="rbgComp" v-model="compName" :value="'comp-three'"> Three&#x3C;/label>
<strong>  &#x3C;KeepAlive :max="2">
</strong>    &#x3C;component :is="activeComp">&#x3C;/component>
<strong>  &#x3C;/KeepAlive>
</strong>&#x3C;/template>
</code></pre>
