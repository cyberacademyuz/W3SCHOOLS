# Vue Template Refs

{% hint style="success" %}
Vue **Andoza Reflari** muayyan DOM elementlariga murojaat qilish uchun ishlatiladi.

Atribut **`ref`**HTML tegiga o'rnatilganda, natijada olingan DOM elementi ob'ektga qo'shiladi **`$refs`**.

Biz Vue-dagi **`ref`**atribut va **`$refs`**obyektni getElementById() yoki querySelector() kabi oddiy JavaScript-dagi usullarga muqobil sifatida ishlatishimiz mumkin.
{% endhint %}

### 'ref' atributi va '$refs' ob'ekti

Atributga ega HTML teglari `ref`ob'ektga qo'shiladi `$refs`va ularga teg ichidan keyinroq kirish mumkin `<script>`.

Element ichidagi matn `<p>`o'zgartiriladi.

<pre class="language-html" data-title="App.vue:"><code class="lang-html">&#x3C;template>
  &#x3C;h1>Example&#x3C;/h1>
  &#x3C;p>Click the button to put "Hello!" as the text in the green p element.&#x3C;/p>
  &#x3C;button @click="changeVal">Change Text&#x3C;/button>
  &#x3C;p ref="pEl">This is the initial text&#x3C;/p>
&#x3C;/template>

&#x3C;script>
  export default {
    methods: {
      changeVal() {
<strong>        this.$refs.pEl.innerHTML = "Hello!";
</strong>      }
    }
  }
&#x3C;/script>
</code></pre>

`$refs`Quyida ob'ekt bir tegning qiymatini boshqa tegga nusxalash uchun ishlatiladigan yana bir misol.

Birinchi tegdagi matn `<p>`ikkinchi tegga ko'chiriladi `<p>`.

{% code title="App.vue:" %}
```html
<template>
  <h1>Example</h1>
  <p ref="p1">Click the button to copy this text into the paragraph below.</p>
  <button @click="transferText">Transfer text</button>
  <p ref="p2">...</p>
</template>

<script>
  export default {
    methods: {
      transferText() { 
        this.$refs.p2.innerHTML = this.$refs.p1.innerHTML;
      }
    }
  };
</script>
```
{% endcode %}

### "$refs" dan kirish qiymatini oling

`$refs`Biz xohlagan xususiyatga kirish uchun ob'ektga qo'shilgan HTML elementiga o'tishimiz mumkin .

Element `<p>`kiritish maydonida yozilgan narsa bilan bir xil tarkibga ega bo'ladi.

{% code title="App.vue:" %}
```html
<template>
  <h1>Example</h1>
  <p>Start writing inside the input element, and the text will be copied into the last paragraph by the use of the '$refs' object.</p>
  <input ref="inputEl" @input="getRefs" placeholder="Write something..">
  <p ref="pEl"></p>
</template>

<script>
  export default {
    methods: {
      getRefs() { 
        this.$refs.pEl.innerHTML = this.$refs.inputEl.value;
      }
    }
  };
</script> 
```
{% endcode %}

### v-for bilan 'ref'

`v-for`Atributi bilan yaratilgan HTML elementlari ob'ektga massiv sifatida `ref`qo'shiladi .`$refs`

Tugma ob'ekt ichida massiv elementi sifatida saqlangan uchinchi ro'yxat elementini ko'rsatadi `$refs`.

{% code title="App.vue:" %}
```html
<template>
  <h1>Example</h1>
  <p>Click the button to reveal the 3rd list element stored as an array element in the $refs object.</p>
  <button @click="getValue">Get the 3rd list element</button><br>
  <ul>
    <li v-for="x in liTexts" ref="liEl">{{ x }}</li>
  </ul>
  <pre>{{ thirdEl }}</pre>
</template>

<script>
  export default {
    data() {
      return {
        thirdEl: ' ',
        liTexts: ['Apple','Banana','Kiwi','Tomato','Lichi']
      }
    },
    methods: {
      getValue() { 
        this.thirdEl = this.$refs.liEl[2].innerHTML;
        console.log("this.$refs.liEl = ",this.$refs.liEl);
      }
    }
  };
</script>

<style>
pre {
  background-color: lightgreen;
  display: inline-block;
}
</style>
```
{% endcode %}
