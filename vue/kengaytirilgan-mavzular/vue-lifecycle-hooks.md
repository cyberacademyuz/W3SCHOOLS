# Vue Lifecycle hooks

{% hint style="success" %}
**Vue-dagi hayot aylanish ilgaklari** komponentning hayot aylanishining ma'lum bosqichlari bo'lib, unda biz narsalarni qilish uchun kod qo'shishimiz mumkin.
{% endhint %}

### Hayotiy aylanish ilgaklari

Har safar komponent o'z hayot aylanishining yangi bosqichiga yetganda, ma'lum bir funktsiya ishlaydi va biz ushbu funktsiyaga kod qo'shishimiz mumkin. Bunday funktsiyalar hayot aylanish ilgaklari deb ataladi, chunki biz o'z kodimizni ushbu bosqichga "ulashimiz" mumkin.

Bularning barchasi komponentning hayotiy tsikli ilgaklari:

1. `beforeCreate`
2. `created`
3. `beforeMount`
4. `mounted`
5. `beforeUpdate`
6. `updated`
7. `beforeUnmount`
8. `unmounted`
9. `errorCaptured`
10. `renderTracked`
11. `renderTriggered`
12. `activated`
13. `deactivated`
14. `serverPrefetch`

Quyida ushbu hayot aylanishi kancalarining misollari keltirilgan.

### "BeforeCreate" kancasi

Yashash `beforeCreate`davri kancasi komponent ishga tushirilishidan oldin sodir bo'ladi, shuning uchun bu Vue komponent ma'lumotlarini, hisoblangan xususiyatlarni, usullarni va voqea tinglovchilarini sozlashdan oldin sodir bo'ladi.

Kanca, `beforeCreate`masalan, global voqea tinglovchisini o'rnatish uchun ishlatilishi mumkin, ammo biz hayot tsikli kancasidan komponentga tegishli bo'lgan `beforeCreate`ma'lumotlar, kuzatuvchilar va usullar kabi elementlarga kirishga urinishdan qochishimiz kerak, chunki ular hali bu bosqichda yaratilmagan. .

Bundan tashqari, DOM elementlariga hayot aylanishi kancasidan kirishga harakat qilish mantiqiy emas `beforeCreate`, chunki ular komponent bo'lgunga qadar yaratilmaydi `mounted.`

{% code title="CompOne.vue:" lineNumbers="true" %}
```html
<template>
    <h2>Component</h2>
    <p>This is the component</p>
    <p id="pResult">{{ text }}</p>
</template>

<script>
export default {
	data() {
		return {
			text: '...'
		}
	},
  beforeCreate() {
		this.text = 'initial text'; // This line has no effect
    console.log("beforeCreate: The component is not created yet.");
  }
}
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'beforeCreate' Lifecycle Hook</h1>
  <p>We can see the console.log() message from 'beforeCreate' lifecycle hook, but there is no effect from the text change we try to do to the Vue data property, because the Vue data property is not created yet.</p>
  <button @click="this.activeComp = !this.activeComp">Add/Remove Component</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: false
    }
  }
}
</script>

<style>
#app > div {
  border: dashed black 1px;
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
  background-color: lightgreen;
}
#pResult {
  background-color: lightcoral;
  display: inline-block;
}
</style>
```
{% endcode %}

Yuqoridagi misolda 15-qator `CompOne.vue`hech qanday ta'sir ko'rsatmaydi, chunki bu qatorda biz Vue ma'lumotlar xususiyati ichidagi matnni o'zgartirishga harakat qilamiz, lekin Vue ma'lumotlar xususiyati aslida hali yaratilmagan. `console.log()`Shuningdek, 16-qatordagi qo'ng'iroq natijasini ko'rish uchun brauzer konsolini ochishni unutmang .

### "Yaratilgan" kanca

Yashash `created`davri kancasi komponent ishga tushirilgandan so'ng sodir bo'ladi, shuning uchun Vue allaqachon komponent ma'lumotlarini, hisoblangan xususiyatlarini, usullarini va voqea tinglovchilarini o'rnatgan.

Biz DOM elementlariga hayot aylanishi kancasidan kirishga urinishdan qochishimiz kerak `created`, chunki komponent bo'lmaguncha DOM elementlariga kirish mumkin emas `mounted`.

Hayotiy `created`tsikl kancasi HTTP so'rovlari bilan ma'lumotlarni olish yoki dastlabki ma'lumotlar qiymatlarini o'rnatish uchun ishlatilishi mumkin. Quyidagi misolda bo'lgani kabi, "text" ma'lumotlar xususiyatiga boshlang'ich qiymat beriladi:

{% code title="CompOne.vue:" lineNumbers="true" %}
```html
<template>
    <h2>Component</h2>
    <p>This is the component</p>
    <p id="pResult">{{ text }}</p>
</template>

<script>
export default {
	data() {
		return {
			text: '...'
		}
	},
  created() {
		this.text = 'initial text';
    console.log("created: The component just got created.");
  }
}
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'created' Lifecycle Hook</h1>
  <p>We can see the console.log() message from 'created' lifecycle hook, and the text change we try to do to the Vue data property works, because the Vue data property is already created at this stage.</p>
  <button @click="this.activeComp = !this.activeComp">Add/Remove Component</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: false
    }
  }
}
</script>

<style>
#app > div {
  border: dashed black 1px;
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
  background-color: lightgreen;
}
#pResult {
  background-color: lightcoral;
  display: inline-block;
}
</style>
```
{% endcode %}

### "Mountdan oldin" ilgagi

Yashash davri kancasi `beforeMount`komponent bo'lishidan oldin sodir bo'ladi `mounted`, shuning uchun komponent DOMga qo'shilishidan oldin.

Biz DOM elementlariga hayot aylanishi kancasidan kirishga urinishdan qochishimiz kerak `beforeMount`, chunki komponent bo'lmaguncha DOM elementlariga kirish mumkin emas `mounted`.

Quyidagi misol biz komponentdagi DOM elementlariga hali kira olmasligimizni ko'rsatadi, 11-qator `CompOne.vue`ishlamayapti va brauzer konsolida xatolik yuzaga keladi:

{% code title="CompOne.vue:" lineNumbers="true" %}
```html
<template>
    <h2>Component</h2>
    <p>This is the component</p>
    <p ref="pEl" id="pEl">We try to access this text from the 'beforeMount' hook.</p>
</template>

<script>
export default {
  beforeMount() {
    console.log("beforeMount: This is just before the component is mounted.");
    this.$refs.pEl.innerHTML = "Hello World!"; // <-- We cannot reach the 'pEl' DOM element at this stage 
  }
}
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'beforeMount' Lifecycle Hook</h1>
  <p>We can see the console.log() message from the 'beforeMount' lifecycle hook, but the text change we try to do to the 'pEl' paragraph DOM element does not work, because the 'pEl' paragraph DOM element does not exist yet at this stage.</p>
  <button @click="this.activeComp = !this.activeComp">Add/Remove Component</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: false
    }
  }
}
</script>

<style>
#app > div {
  border: dashed black 1px;
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
  background-color: lightgreen;
}
#pEl {
  background-color: lightcoral;
  display: inline-block;
}
</style>
```
{% endcode %}

### "O'rnatilgan" ilgak

Komponent DOM daraxtiga qo'shilgandan so'ng, `mounted()`funktsiya chaqiriladi va biz o'z kodimizni ushbu bosqichga qo'shishimiz mumkin.

Bu komponentga tegishli bo'lgan DOM elementlari bilan bog'liq ishlarni bajarishimiz kerak bo'lgan birinchi imkoniyat, masalan, atribut `ref`va `$refs`ob'ektdan foydalanish, quyida ikkinchi misolda bo'lgani kabi.

{% code title="CompOne.vue:" %}
```html
<template>
    <h2>Component</h2>
    <p>Right after this component is added to the DOM, the mounted() function is called and we can add code to that mounted() function. In this example, an alert popup box appears after this component is mounted.</p>
    <p><strong>Note:</strong> The reason that the alert is visible before the component is visible is because the alert is called before the browser gets to render the component to the screen.</p>
</template>
  
<script>
  export default {
    mounted() {
      alert("The component is mounted!");
    }
  }
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'mounted' Lifecycle Hook</h1>
  <button @click="this.activeComp = !this.activeComp">Create component</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: false
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 20px;
    margin: 10px;
    width: 400px;
    background-color: lightgreen;
  }
</style>
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Bosqich `mounted`komponent DOMga qo'shilgandan so'ng sodir bo'ladi, lekin yuqoridagi misolda `alert()`komponentni ko'rishdan oldin ko'rinadi. Buning sababi shundaki, birinchi navbatda komponent DOMga qo'shiladi, lekin brauzer komponentni ekranga ko'rsatishdan oldin, bosqich `mounted`sodir bo'ladi va `alert()`ko'rinadigan bo'ladi va komponentni ko'rsatuvchi brauzerni to'xtatib turadi.
{% endhint %}

Quyida, ehtimol, foydaliroq bo'lgan misol keltirilgan: forma komponenti o'rnatilgandan so'ng kursorni kiritish maydoniga qo'yish, shuning uchun foydalanuvchi yozishni boshlashi mumkin.

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Form Component</h2>
  <p>When this component is added to the DOM tree, the mounted() function is called, and we put the cursor inside the input element.</p>
  <form @submit.prevent>
    <label>
      <p>
        Name: <br>
        <input type="text" ref="inpName">
      </p>
    </label>
    <label>
      <p>
        Age: <br>
        <input type="number">
      </p>
    </label>
    <button>Submit</button>
  </form>
  <p>(This form does not work, it is only here to show the mounted lifecycle hook.)</p>
</template>

<script>
  export default {
    mounted() {
      this.$refs.inpName.focus();
    }
  }
</script>
```
{% endcode %}

### "BeforeUpdate" kancasi

Hayotiy `beforeUpdate`tsikl kancasi komponentimiz ma'lumotlari o'zgarganda, lekin yangilanish ekranga ko'rsatilishidan oldin chaqiriladi. Hayotiy `beforeUpdate`tsikl kancasi hayot aylanishi kancasidan oldin sodir bo'ladi `updated`.

Kancaning o'ziga xos tomoni `beforeUpdate`shundaki, biz dasturni yangi yangilanishsiz o'zgartirishimiz mumkin, shuning uchun biz cheksiz tsikldan qochamiz. Hayotiy tsikl kancasida ilovaga o'zgartirish kiritmaslikning sababi shu `updated`, chunki bu ilgak yordamida cheksiz tsikl yaratiladi. Quyidagi uchinchi misolga qarang, qizil rangda.

Funksiya ishlaganligini ko'rsatish uchun hujjatga teg `beforeUpdate()`qo'shadi .`<li>beforeUpdate()`

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component</h2>
  <p>This is the component</p>
</template>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'beforeUpdate' Lifecycle Hook</h1>
  <p>Whenever there is a change in our page, the application is 'updated' and the 'beforeUpdate' hook happens just before that.</p>
  <p>It is safe to modify our page in the 'beforeUpdate' hook like we do here, but if we modify our page in the 'updated' hook, we will generate an infinite loop.</p>
  <button @click="this.activeComp = !this.activeComp">Add/Remove Component</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
  <ol ref="divLog"></ol>
</template>

<script>
export default {
  data() {
    return {
      activeComp: true
    }
  },
  beforeUpdate() {
    this.$refs.divLog.innerHTML += "<li>beforeUpdate: This happened just before the 'updated' hook.</li>";
  }
}
</script>

<style>
#app > div {
  border: dashed black 1px;
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
  background-color: lightgreen;
}
</style>
```
{% endcode %}

### "Yangilangan" kanca

`updated`Bizning komponentimiz DOM daraxtini yangilagandan so'ng, hayot aylanishi kancasi chaqiriladi.

Funktsiya `updated()`bilan xabar yozadi `console.log()`. Bu sahifa har safar yangilanganda sodir bo'ladi, bu misolda komponent har safar qo'shilgan yoki o'chirilganda.

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component</h2>
  <p>This is the component</p>
</template>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'updated' Lifecycle Hook</h1>
  <p>Whenever there is a change in our page, the application is updated and the updated() function is called. In this example we use console.log() in the updated() function that runs when our application is updated.</p>
  <button @click="this.activeComp = !this.activeComp">Add/Remove Component</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: true
    }
  },
  updated() {
    console.log("The component is updated!");
  }
}
</script>

<style>
#app {
  max-width: 450px;
}
#app > div {
  border: dashed black 1px;
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
  width: 80%;
  background-color: lightgreen;
}
</style> 
```
{% endcode %}

Natijani brauzer konsolida "Komponentni qo'shish/o'chirish" tugmasini 10 marta bosgandan so'ng ko'rishimiz mumkin:

![konsol ekran tasviri](https://www.w3schools.com/vue/img\_LCHooks\_updated.png)

{% hint style="warning" %}
**Eslatma:** Biz hayot tsikli kancasi chaqirilganda sahifaning o'zini o'zgartirmaslikdan ehtiyot bo'lishimiz kerak `updated`, chunki keyin sahifa qayta-qayta yangilanib, cheksiz tsikl hosil qiladi.
{% endhint %}

Keling, yuqoridagi eslatma bizni ogohlantirgandek bajarsak, nima bo'lishini ko'rib chiqaylik. Sahifa cheksiz yangilanadimi?:

Funktsiya `updated()`xatboshiga matn qo'shadi, bu esa o'z navbatida sahifani yana yangilaydi va funksiya cheksiz tsiklda qayta-qayta ishlaydi. Yaxshiyamki, brauzeringiz bu tsiklni oxir-oqibat to'xtatadi.

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component</h2>
  <p>This is the component</p>
</template>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'updated' Lifecycle Hook</h1>
  <p>Whenever there is a change in our page, the application is updated and the updated() function is called.</p>
  <p>The first change that causes the updated hook to be called is when we remove the component by clicking the button. When this happens, the update() function adds text to the last paragraph, which in turn updates the page again and again.</p>
  <button @click="this.activeComp = !this.activeComp">Add/Remove Component</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
  <div>{{ text }}</div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: true,
      text: "Hello, "
    }
  },
  updated() {
    this.text += "hi, ";
  }
}
</script>

<style>
#app {
  max-width: 450px;
}
#app > div {
  border: dashed black 1px;
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
  width: 80%;
  background-color: lightgreen;
}
</style>
```
{% endcode %}

Yuqoridagi kodni kompyuteringizda ishlab rejimida mahalliy sifatida ishga tushirganda, Chrome brauzer konsoli ogohlantirishi quyidagicha ko'rinadi:

<figure><img src="https://www.w3schools.com/vue/img_LCHooks_updateLoop.png" alt=""><figcaption></figcaption></figure>

### "BeforeUnmount" kancasi

Yashash davri kancasi `beforeUnmount`komponent DOMdan olib tashlanishidan oldin chaqiriladi.

Quyidagi misolda ko'rib turganimizdek, biz hali ham kancada DOM-dagi komponent elementlariga kirishimiz mumkin `beforeUnmount`.

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component</h2>
  <p ref="pEl">Strawberries!</p>
</template>
  
<script>
export default {
  beforeUnmount() {
    alert("beforeUnmount: The text inside the p-tag is: " + this.$refs.pEl.innerHTML);
  }
}
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>Lifecycle Hooks</h1>
  <button @click="this.activeComp = !this.activeComp">{{ btnText }}</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: true
    }
  },
  computed: {
    btnText() {
      if(this.activeComp) {
        return 'Remove component'
      }
      else {
        return 'Add component'
      }
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 20px;
    margin: 10px;
    width: 400px;
    background-color: lightgreen;
  }
</style>
```
{% endcode %}

### "O'chirilgan" ilgak

Hayotiy `unmounted`tsikl kancasi komponent DOMdan olib tashlanganidan keyin chaqiriladi.

Bu ilgak, masalan, voqea tinglovchilarini olib tashlash yoki taymerlar yoki intervallarni bekor qilish uchun ishlatilishi mumkin.

Agar komponent bo'lsa `unmounted`, `unmounted()`funksiya chaqiriladi va biz unga kodimizni qo'shishimiz mumkin:

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component</h2>
  <p>When this component is removed from the DOM tree, the unmounted() function is called and we can add code to that function. In this example we create an alert popup box when this component is removed.</p>
</template>

<script>
export default {
  unmounted() {
    alert("The component is removed (unmounted)!");
  }
}
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>Lifecycle Hooks</h1>
  <button @click="this.activeComp = !this.activeComp">{{ btnText }}</button>
  <div>
    <comp-one v-if="activeComp"></comp-one>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: true
    }
  },
  computed: {
    btnText() {
      if(this.activeComp) {
        return 'Remove component'
      }
      else {
        return 'Add component'
      }
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 20px;
    margin: 10px;
    width: 400px;
    background-color: lightgreen;
  }
</style>
 
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Bosqich `unmounted`komponent DOMdan olib tashlangandan keyin sodir bo'ladi, lekin yuqoridagi misolda `alert()`komponent yo'qolishidan oldin ko'rinadi. Buning sababi shundaki, birinchi navbatda komponent DOMdan o'chiriladi, lekin brauzer komponentni ekranga olib tashlashni amalga oshirishdan oldin, bosqich sodir bo'ladi va `unmounted`ko'rinadigan `alert()`bo'ladi va brauzer komponentni ko'rinadigan tarzda olib tashlashni to'xtatadi.
{% endhint %}

### "ErorCaptured" ilgagi

Hayotiy `errorCaptured`sikl kancasi bola/avlod komponentida xatolik yuz berganda chaqiriladi.

Ushbu ilgak xatolarni qayta ishlash, jurnalga yozish yoki foydalanuvchiga xatoni ko'rsatish uchun ishlatilishi mumkin.

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component</h2>
  <p>This is the component</p>
  <button @click="generateError">Generate Error</button>
</template>

<script>
export default {
  methods: {
    generateError() {
      this.$refs.objEl.innerHTML = "hi";
    }
  }
}
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'errorCaptured' Lifecycle Hook</h1>
  <p>Whenever there is an error in a child component, the errorCaptured() function is called on the parent.</p>
  <p>When the button inside the component is clicked, a method will run that tries to do changes to a $refs object that does not exist. This creates an error in the component that triggers the 'errorCaptured' lifecycle hook in the parent, and an alert box is displayed with information about the error.</p>
  <p>After clicking "Ok" in the alert box you can see the error in the browser console.</p>
  <div>
    <comp-one></comp-one>
  </div>
</template>

<script>
export default {
  errorCaptured() {
    alert("An error occurred");
  }
}
</script>

<style>
#app > div {
  border: dashed black 1px;
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
  background-color: lightgreen;
}
</style> 
```
{% endcode %}

Xato haqidagi ma'lumot funktsiyaga argument sifatida ham olinishi mumkin `errorCaptured()`va bu argumentlar:

1. xato
2. xatolikka sabab bo'lgan komponent
3. xato manba turi

Quyidagi misolda bu argumentlar funksiyada ushlangan `errorCaptured()`va konsolga yozilgan:

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component</h2>
  <p>This is the component</p>
  <button @click="generateError">Generate Error</button>
</template>

<script>
export default {
  methods: {
    generateError() {
      this.$refs.objEl.innerHTML = "hi";
    }
  }
}
</script>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'errorCaptured' Lifecycle Hook</h1>
  <p>Whenever there is an error in a child component, the errorCaptured() function is called on the parent.</p>
  <p>Open the browser console to see the captured error details.</p>
  <div>
    <comp-one></comp-one>
  </div>
</template>

<script>
export default {
  errorCaptured(error,compInst,errorInfo) {
    console.log("error: ", error);
    console.log("compInst: ", compInst);
    console.log("errorInfo: ", errorInfo);
  }
}
</script>

<style>
#app > div {
  border: dashed black 1px;
  border-radius: 10px;
  padding: 10px;
  margin-top: 10px;
  background-color: lightgreen;
}
</style>
```
{% endcode %}

### "renderTracked" va "renderTriggered" hayot aylanish ilgaklari

`renderTracked`Reaktiv komponentni kuzatish yoki kuzatish uchun render funksiyasi o‘rnatilgan bo‘lsa, ilgak ishlaydi . Kanca `renderTracked`odatda reaktiv komponent ishga tushirilganda ishlaydi.

Ilgak `renderTriggered`bunday kuzatilgan reaktiv komponent o'zgarganda ishlaydi va shuning uchun ekran so'nggi o'zgarishlar bilan yangilanishi uchun yangi renderni ishga tushiradi.

{% hint style="warning" %}
Reaktiv **komponent** o'zgarishi mumkin bo'lgan komponentdir.

Render **funksiyasi** reaktiv komponentlarni kuzatib boradigan Vue tomonidan tuzilgan funksiyadir. Reaktiv komponent o'zgarganda, render funktsiyasi ishga tushadi va dasturni ekranga qayta ko'rsatadi.
{% endhint %}

`renderTracked`va ilgaklar `renderTriggered`disk raskadrovkada foydalanish uchun mo'ljallangan va faqat ishlab chiqish rejimida mavjud.

`alert()`va `console.log()`dan `renderTracked`va ilgaklarni ko'rish uchun `renderTriggered`quyidagi misoldagi kodni kompyuteringizga nusxalashingiz va dasturni ishlab chiqish rejimida ishga tushirishingiz kerak.

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component One</h2>
  <p>This is a component.</p>
  <button @click="counter++">Add One</button>
  <p>{{ counter }}</p>
</template>
  
<script>
export default {
  data() {
    return {
      counter: 0
    }
  },
  renderTracked(evt) {
    console.log("renderTracked: ",evt);
    alert("renderTracked");
  },
  renderTriggered(evt) {
    console.log("renderTriggered: ",evt)
    alert("renderTriggered");
  }
}
</script> 
```
{% endcode %}

{% code title="" %}
```html
<template>
  <h1>The 'renderTracked' and 'renderTriggered' Lifecycle Hooks</h1>
  <p>The 'renderTracked' and 'renderTriggered' lifecycle hooks are used for debugging.</p>
  <p><mark>This example only works in development mode, so to see the hooks run, you must copy this code and run it on you own computer in development mode.</mark></p>
  <div>
    <comp-one></comp-one>
  </div>
</template>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 20px;
    margin-top: 10px;
    background-color: lightgreen;
  }
</style>
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Yuqoridagi misoldagi kod nusxa ko'chirish va ishlab chiqish rejimida kompyuteringizda mahalliy sifatida ishga tushirish uchun mo'ljallangan, chunki `renderTracked`va `renderTriggered`ilgaklar faqat ishlab chiqish rejimida ishlaydi.
{% endhint %}

### "Faollashtirilgan" va "o'chirilgan" hayot aylanish ilgaklari

Ushbu sahifada yuqorida ko'rib turganimizdek, bizda komponent o'chirilganda yoki DOMga qo'shilganda `mounted`va hayot aylanish ilgaklari mavjud.`unmounted`

va hayot aylanish ilgaklari keshlangan `activated`dinamik `deactivated`komponent qo'shilgan yoki o'chirilganda uchun, lekin DOMdan emas. Teg [`<KeepAlive>`](https://www-w3schools-com.translate.goog/vue/vue\_dynamic-components.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp#KeepAlive)quyidagi misolda dinamik komponentni keshlash uchun ishlatiladi.

{% code title="CompOne.vue:" %}
```html
<template>CompOne.vue:
  <h2>Component</h2>
  <p>Below is a log with every time the 'mounted' or 'activated' hooks run.</p>
  <ol ref="olEl"></ol>
  <p>You can also see when these hooks run in the console.</p>
</template>
  
<script>
export default {
  mounted() {
    console.log("mounted");
    const liEl = document.createElement("li");
    liEl.innerHTML = "mounted";
    this.$refs.olEl.appendChild(liEl);
  },
  activated() {
    console.log("activated");
    const liEl = document.createElement("li");
    liEl.innerHTML = "activated";
    this.$refs.olEl.appendChild(liEl);
  }
}
</script>

<style>
  li {
    background-color: lightcoral;
    width: 5em;
  }
</style>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'activated' Lifecycle Hook</h1>
  <p>In this example for the 'activated' hook we check if the component is cached properly with <KeepAlive>.</p>
  <p>If the component is cached properly with <KeepAlive> we expect the 'mounted' hook to run once the first time the component is included (must be added to the DOM the first time), and we expect the 'activated' hook to run every time the component is included (also the first time).</p>
  <button @click="this.activeComp = !this.activeComp">Include component</button>
  <div>
    <KeepAlive>
      <comp-one v-if="activeComp"></comp-one>
    </KeepAlive>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: false
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 20px;
    margin-top: 10px;
    background-color: lightgreen;
  }
</style>
```
{% endcode %}

Keling, yuqoridagi misolni `activated`va `deactivated`ilgaklar qanday ishlashini ko'rish uchun kengaytiramiz. Keling, `mounted`va `unmounted`ilgaklardan ham foydalanamiz, shunda biz `mounted`keshlangan komponent birinchi marta qo'shilganda ilgak bir marta ishlashini va kanca `unmounted`hech qachon keshlangan komponent uchun ishlamasligini ko'rishimiz mumkin.

{% code title="CompOne.vue:" %}
```html
<template>
  <h2>Component</h2>
  <p>Below is a log with every time the 'activated', 'deactivated', 'mounted' or 'unmounted' hooks run.</p>
  <ol ref="olEl"></ol>
  <p>You can also see when these hooks run in the console.</p>
</template>
  
<script>
export default {
  mounted() {
    this.logHook("mounted");
  },
  unmounted() {
    this.logHook("unmounted");
  },
  activated() {
    this.logHook("activated");
  },
  deactivated() {
    this.logHook("deactivated");
  },
  methods: {
    logHook(hookName) {
      console.log(hookName);
      const liEl = document.createElement("li");
      liEl.innerHTML = hookName;
      this.$refs.olEl.appendChild(liEl);
    }
  }
}
</script>

<style>
  li {
    background-color: lightcoral;
    width: 5em;
  }
</style>
```
{% endcode %}

{% code title="App.vue:" %}
```html
<template>
  <h1>The 'activated' and 'deactivated' Lifecycle Hooks</h1>
  <p>In this example for the 'activated' and 'deactivated' hooks we also see when and if the 'mounted' and 'unmounted' hooks are run.</p>
  <button @click="this.activeComp = !this.activeComp">Include component</button>
  <div>
    <KeepAlive>
      <comp-one v-if="activeComp"></comp-one>
    </KeepAlive>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeComp: false
    }
  }
}
</script>

<style scoped>
  div {
    border: dashed black 1px;
    border-radius: 10px;
    padding: 20px;
    margin-top: 10px;
    background-color: lightgreen;
  }
</style>
```
{% endcode %}

### "serverPrefetch" hayot aylanish ilgagi

"serverPrefetch" kancasi faqat server tomonida renderlash (SSR) paytida chaqiriladi.

"ServerPrefetch" kancasi uchun misolni tushuntirish va yaratish nisbatan uzoqroq kirish va sozlashni talab qiladi va bu ushbu qo'llanmaning doirasidan tashqarida.
