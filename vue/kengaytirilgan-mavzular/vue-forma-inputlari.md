# Vue Forma inputlari

{% hint style="success" %}
Biz ushbu qo'llanmada <mark style="color:green;">Vue Forms</mark> va <mark style="color:green;">v-model sahifalarida</mark> **shakl kiritishning** bir nechta misollarini ko'rdik .

Ushbu sahifa Vue-da radio tugmalari, tasdiqlash qutilari, ochiladigan ro'yxat va oddiy matn kiritish maydoni kabi ko'proq **shakl kiritish** misollari to'plamidir.
{% endhint %}

### radio tugmalari

Xuddi shu tanlovga tegishli bo'lgan radio tugmalar bir xil nomga ega bo'lishi kerak, shunda faqat bitta radio tugmachani tanlash mumkin.

Vue-dagi barcha kirishlarda bo'lgani kabi, biz radio tugmachasini kiritish qiymatini bilan ushlaymiz `v-model`, lekin `value`atribut ham tegda aniq o'rnatilishi kerak `<input type="radio">`.

Vue shaklida radio tugmalaridan shunday foydalanishimiz mumkin:

{% code title="App.vue:" %}
```html
<template>
  <h1>Radio Buttons in Vue</h1>
  <form @submit.prevent="registerAnswer">
    <p>What is your favorite animal?</p>
    <label>
      <input type="radio" name="favAnimal" v-model="inpVal" value="Cat"> Cat
    </label>
    <label>
      <input type="radio" name="favAnimal" v-model="inpVal" value="Dog"> Dog
    </label>
    <label>
      <input type="radio" name="favAnimal" v-model="inpVal" value="Turtle"> Turtle
    </label>
    <label>
      <input type="radio" name="favAnimal" v-model="inpVal" value="Moose"> Moose
    </label>
    <button type="submit">Submit</button>
  </form>
  <div>
    <h3>Submitted choice:</h3>
    <p id="pAnswer">{{ inpValSubmitted }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      inpVal: '',
      inpValSubmitted: 'Not submitted yet'
    }
  },
  methods: {
    registerAnswer() {
      if(this.inpVal) {
        this.inpValSubmitted = this.inpVal;
      }
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 0 20px 20px 20px;
    margin-top: 20px;
    display: inline-block;
  }
  button {
    margin: 10px;
  }
  label {
    display: block;
    width: 80px;
    padding: 5px;
  }
  label:hover {
    cursor: pointer;
    background-color: rgb(211, 244, 211);
    border-radius: 5px;
  }
  #pAnswer {
    background-color: lightgreen;
    padding: 5px;
  }
</style>
```
{% endcode %}

### katakchalar

Belgilash katakchasi kirishlari ( `<input type="checkbox">`) bilan bir xil massivga ulanganda `v-model`, belgilangan katakchalar uchun qiymatlar ushbu massivda yig'iladi:

{% code title="App.vue:" %}
```html
<template>
  <h1>Checkbox Inputs in Vue</h1>
  <form @submit.prevent="registerAnswer">
    <p>What kinds of food do you like?</p>
    <label>
      <input type="checkbox" v-model="likeFoods" value="Pizza"> Pizza
    </label>
    <label>
      <input type="checkbox" v-model="likeFoods" value="Rice"> Rice
    </label>
    <label>
      <input type="checkbox" v-model="likeFoods" value="Fish"> Fish
    </label>
    <label>
      <input type="checkbox" v-model="likeFoods" value="Salad"> Salad
    </label>
    <button type="submit">Submit</button>
  </form>
  <div>
    <h3>Submitted answer:</h3>
    <p id="pAnswer">{{ inpValSubmitted }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      likeFoods: [],
      inpValSubmitted: 'Not submitted yet'
    }
  },
  methods: {
    registerAnswer() {
      this.inpValSubmitted = this.likeFoods;
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 0 20px 20px 20px;
    margin-top: 20px;
    display: inline-block;
  }
  button {
    margin: 10px;
  }
  label {
    display: block;
    width: 80px;
    padding: 5px;
  }
  label:hover {
    cursor: pointer;
    background-color: rgb(211, 244, 211);
    border-radius: 5px;
  }
  #pAnswer {
    background-color: lightgreen;
    padding: 5px;
  }
</style> 
```
{% endcode %}

### Ochiladigan ro'yxat

Ochiladigan ro'yxat ichida teglari `<select>`bo'lgan tegdan iborat `<option>`.

Vue-da ochiladigan ro'yxatni ishlatganda biz `<select>`tegni bilan bog'lashimiz `v-model`va teglarga qiymat berishimiz kerak `<option>`:

{% code title="App.vue:" %}
```html
<template>
  <h1>Drop-down List in Vue</h1>
  <form @submit.prevent="registerAnswer">
    <label for="cars">Choose a car:</label>
    <select  v-model="carSelected" id="cars">
      <option disabled value="">Please select one</option>
      <option>Volvo</option>
      <option>Saab</option>
      <option>Opel</option>
      <option>Audi</option>
    </select>
    <br><br>
    <input type="submit" value="Submit">
  </form>
  <div>
    <h3>Submitted answer:</h3>
    <p id="pAnswer">{{ inpValSubmitted }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      carSelected: '',
      inpValSubmitted: 'Not submitted yet'
    }
  },
  methods: {
    registerAnswer() {
      if(this.carSelected) {
        this.inpValSubmitted = this.carSelected;
      }
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 0 20px 20px 20px;
    margin-top: 20px;
    display: inline-block;
  }
  button {
    margin: 10px;
  }
  label {
    width: 80px;
    padding: 5px;
  }
  label:hover {
    cursor: pointer;
    background-color: rgb(211, 244, 211);
    border-radius: 5px;
  }
  #pAnswer {
    background-color: lightgreen;
    padding: 5px;
  }
</style>
```
{% endcode %}

### \<bir nechta tanlang>

`multiple`Tegdagi atribut bilan `<select>`ochiladigan ro'yxat kengaytiriladi va biz bir nechta variantni tanlashimiz mumkin.

Bir nechta variantni tanlash uchun Windows foydalanuvchilari "ctrl" tugmasini, macOS foydalanuvchilari esa "buyruq" tugmasini bosishlari kerak.

Vue-dan foydalanganda biz tegni bilan `<select multiple>`bog'lashimiz va teglarga qiymat berishimiz kerak :`<select>v-model<option>`

{% code title="App.vue:" %}
```html
<template>
  <h1>Select Multiple in Vue</h1>
  <p>Depending on your operating system, use the 'ctrl' or the 'command' key to select multiple options.</p>
  <form @submit.prevent="registerAnswer">
    <label for="cars">Choose one or more cars:</label><br>
    <select  v-model="carsSelected" id="cars" multiple>
      <option>Volvo</option>
      <option>Saab</option>
      <option>Opel</option>
      <option>Audi</option>
      <option>Kia</option>
    </select>
    <button type="submit">Submit</button>
  </form>
  <div>
    <h3>Submitted answer:</h3>
    <p id="pAnswer">{{ inpValSubmitted }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      carsSelected: [],
      inpValSubmitted: 'Not submitted yet'
    }
  },
  methods: {
    registerAnswer() {
      if(this.carsSelected) {
        this.inpValSubmitted = this.carsSelected;
      }
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 0 20px 20px 20px;
    margin-top: 20px;
    display: inline-block;
  }
  button, select {
    margin: 10px;
    display: block;
  }
  label {
    width: 80px;
    padding: 5px;
  }
  label:hover {
    cursor: pointer;
    background-color: rgb(211, 244, 211);
    border-radius: 5px;
  }
  #pAnswer {
    background-color: lightgreen;
    padding: 5px;
  }
</style>
```
{% endcode %}

### Faqat o'qish formasi kiritishlari

Formada kiritishlardan foydalanish `v-model`ikki tomonlama bog'lanishni yaratadi, ya'ni Vue ma'lumotlar namunasi o'zgarsa, kirish `value`atributi ham o'zgaradi.

Faqat oʻqish uchun moʻljallangan shakl kiritishlari uchun `<input type="file">`atributni `value`Vue maʼlumotlar misolidan oʻzgartirib boʻlmaydi, shuning uchun biz dan foydalana olmaymiz `v-model`.

Faqat oʻqish uchun moʻljallangan shakl kiritishlari uchun, masalan , Vue maʼlumotlar namunasini yangilaydigan usulni chaqirish uchun `<input type="file">`foydalanishimiz kerak :`@change`

{% code title="App.vue:" %}
```html
<template>
  <h1>Input Type File</h1>
  <form @submit.prevent="registerAnswer">
    <label>Choose a file:
      <input @change="updateVal" type="file">
    </label>
    <button type="submit">Submit</button>
  </form>
  <div>
    <h3>Submitted answer:</h3>
    <p id="pAnswer">{{ inpValSubmitted }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      fileInp: null,
      inpValSubmitted: 'Not submitted yet'
    }
  },
  methods: {
    registerAnswer() {
      if(this.fileInp) {
        this.inpValSubmitted = this.fileInp;
      }
    },
    updateVal(e) {
      this.fileInp = e.target.value;
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 0 20px 20px 20px;
    margin-top: 20px;
    display: inline-block;
  }
  button {
    margin: 10px;
    display: block;
  }
  #pAnswer {
    background-color: lightgreen;
    padding: 5px;
  }
</style> 
```
{% endcode %}

{% hint style="success" %}
**Ma'lumot:** Yuqoridagi misolda yuborilgan fayl nomi `C:\fakepath\`oldida fayl yo'lini oladi. Bu zararli dastur foydalanuvchining fayl tuzilishini taxmin qilishiga yo'l qo'ymaslik uchun.
{% endhint %}

### Boshqa shakl kiritishlari

Yuqorida aytib o'tilgan shakl kiritishlari bilan biz atribut uchun qiymat berishimiz kerak edi `value`, ammo quyidagi shakl kiritishlari bilan foydalanuvchi qiymatni beradi:

* `<input type="color">`
* `<input type="date">`
* `<input type="datetime-local">`
* `<input type="number">`
* `<input type="password">`
* `<input type="range">`
* `<input type="search">`
* `<input type="tel">`
* `<input type="text">`
* `<input type="time">`
* `<textarea>`

Foydalanuvchi ushbu turdagi shakl kiritishlari uchun qiymatni allaqachon berganligi sababli, Vue-da biz qilishimiz kerak bo'lgan narsa kirishni ma'lumotlar xususiyatiga ulashdir `v-model`.

Vue-da shunday foydalanish mumkin `<input type="range">`:

{% code title="App.vue:" %}
```html
<form @submit.prevent="registerAnswer">
  <label>How tall are you?<br>
    <input v-model="heightInp" type="range" min="50" max="235"> {{ heightInp }} cm
  </label>
  <button type="submit">Submit</button>
</form> 
```
{% endcode %}

Va Vue-da qanday foydalanish kerak `<input type="color">`:

{% code title="App.vue:" %}
```html
<form @submit.prevent="registerAnswer">
  <label>Choose a color: 
    <input v-model="colorInp" type="color">
  </label>
  <button type="submit">Submit</button>
</form>
 
```
{% endcode %}

Va Vue-da qanday foydalanish kerak `<textarea>`:

{% code title="App.vue:" %}
```html
<form @submit.prevent="registerAnswer">
  <label>
    <p>What do you think about our product?</p> 
    <textarea v-model="txtInp" placeholder="Write something.." rows="4" cols="35"></textarea>
  </label>
  <button type="submit">Submit</button>
</form>
```
{% endcode %}
