# Vue v-show

{% hint style="success" %}
Elementni qanday qilib ko'rinadigan yoki ko'rinmasligini o'rganing `v-show`.

`v-show`foydalanish oson, chunki shart HTML teg atributida to'g'ri yozilgan.
{% endhint %}

### shartli ko'rinish

Ko'rsatma `v-show`shart "noto'g'ri" bo'lsa, CSS "display" xususiyati qiymatini "yo'q" ga o'rnatish orqali elementni yashiradi.

HTML atributi sifatida yozgandan so'ng, `v-show`teg ko'rinadigan yoki ko'rinmasligini hal qilish uchun shart qo'yishimiz kerak.

{% code title="sintaksis:" %}
```
<div v-show="showDiv">This div tag can be hidden</div>
```
{% endcode %}

Yuqoridagi kodda "showDiv" xususiyat qiymati sifatida "true" yoki "yolg'on" bo'lgan mantiqiy Vue ma'lumotlar xususiyatini ifodalaydi. Agar "showDiv" "to'g'ri" bo'lsa, div tegi ko'rsatiladi va "noto'g'ri" bo'lsa teg ko'rsatilmaydi.

\<div> elementini faqat showDiv xususiyati "true"ga o'rnatilgan bo'lsa ko'rsating.

{% code title="" %}
```
<div id="app">
  <div v-show="showDiv">This div tag can be hidden</div>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        showDiv: true
      }
    }
  })
  app.mount('#app')
</script>
```
{% endcode %}

### `v-show`va boshqalar`v-if`

`v-show`va o'rtasidagi farq `v-if`shundaki, `v-if`elementni shartga qarab yaratadi (ko'rsatadi), lekin `v-show`allaqachon yaratilgan element bilan `v-show`faqat uning ko'rinishini o'zgartiradi.

`v-show`Shuning uchun, ob'ektning ko'rinishini almashtirishda foydalanish yaxshiroqdir , chunki brauzer uchun buni qilish osonroq va bu tezroq javob va yaxshi foydalanuvchi tajribasiga olib kelishi mumkin.

`v-if`Over ishlatishning sababi `v-show`va bilan `v-if`ishlatilishi mumkin .`v-else-ifv-else`

Quyidagi misolda `v-show`ular `v-if`ikki xil \<div> elementida alohida ishlatiladi, lekin bir xil Vue xususiyatiga asoslangan. Siz misolni ochishingiz va kodni tekshirishingiz mumkin, u `v-show`\<div> elementini saqlaydi va faqat CSS ko'rsatish xususiyatini "yo'q" ga o'rnatadi, lekin `v-if`aslida \<div> elementini yo'q qiladi.

Ikki \<div> elementini faqat showDiv xususiyati "true"ga o'rnatilgan bo'lsa ko'rsating. Agar showDiv xususiyati "noto'g'ri" ga o'rnatilgan bo'lsa va biz brauzer yordamida misol sahifasini tekshirsak, \<div> elementi yo'q qilinganligini ko'rishimiz mumkin `v-if`, lekin \<div> elementi `v-show`CSS-ni ko'rsatish xususiyati "none" ga o'rnatilgan.

```
<div id="app">
  <div v-show="showDiv">Div tag with v-show</div>
  <div v-if="showDiv">Div tag with v-if</div>
</div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    data() {
      return {
        showDiv: true
      }
    }
  })
  app.mount('#app')
</script>
```
