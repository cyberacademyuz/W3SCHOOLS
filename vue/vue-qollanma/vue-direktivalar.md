# Vue Direktivalar

{% hint style="success" %}
Vue direktivalari - bu HTML tegiga qo'shimcha funksionallik beradigan `v-` prefiksli maxsus HTML atributlaridir.

Vue direktivalari dinamik va moslashuvchan UI yaratish uchun Vue kodiga ulanadi.

Vue bilan moslashuvchan sahifalar yaratish ancha oson va odatiy JavaScript metodlari bilan solishtirganda kamroq kod talab qiladi.
{% endhint %}

### Turli xil Vue direktivalari

Ushbu qo'llanmada biz foydalanadigan turl Vue direktivalari keltirilgan.

| Direktiva                                                                                                                                 | Ta'rif                                                                                                                                                                                                                                                                           |
| ----------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| [`v-bind`](https://www-w3schools-com.translate.goog/vue/vue\_v-bind.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)   | HTML tegidagi atributni Vue kodidagi ma'lumotlar o'zgaruvchisiga ulaydi.                                                                                                                                                                                                         |
| [`v-if`](https://www-w3schools-com.translate.goog/vue/vue\_v-if.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)       | Shartga qarab HTML teglarini yaratadi. `v-else-if` va `v-else` direktivalari `v-if` direktivasi bilan birga ishlatiladi.                                                                                                                                                         |
| [`v-show`](https://www-w3schools-com.translate.goog/vue/vue\_v-show.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)   | Berilgan shartga qarab HTML elementini ko'rinishi yoki ko'rinmasligini belgilaydi.                                                                                                                                                                                               |
| [`v-for`](https://www-w3schools-com.translate.goog/vue/vue\_v-for.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)     | For-loop yordamida Vue kodidagi array asosida teglar ro'yxatini yaratadi.                                                                                                                                                                                                        |
| [`v-on`](https://www-w3schools-com.translate.goog/vue/vue\_v-on.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp)       | HTML tegidagi hodisani JavaScript expressioni yoki Vue kodida metodga ulaydi. Shuningdek, [**event-modifier**](https://www.w3schools.com/vue/vue\_event-modifiers.php)lar yordamida sahifamizning ma'lum bir hodisaga qanday munosabatda bo'lishini aniqroq aniqlashimiz mumkin. |
| [`v-model`](https://www-w3schools-com.translate.goog/vue/vue\_v-model.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) | `<form>`, `<input>`va `<button>` kabi teglari bilan HTML formalarida ishlatiladi. Input elementi va Vue maʼlumotlar xususiyati oʻrtasida ikki tomonlama bogʻlanish hosil qiladi.                                                                                                 |

#### Misol: `v-bind` direktivasi

Brauzer `<div>` elementini Vue kodidan qaysi classga ulash kerakligini topadi.

```
<!DOCTYPE html>
<html lang="en">
<head>
  <style>
    .pinkBG {
      background-color: lightpink;
    }
  </style>
</head>
<body>

  <div id="app">
    <div v-bind:class="vueClass"></div>
  </div>

  <script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
  <script>
    const app = Vue.createApp({
      data() {
        return {
          vueClass: "pinkBG"
        }
      }
    })
    app.mount('#app')
  </script>
</body>
</html>

```

{% hint style="warning" %}
**Eslatma:** Yuqoridagi misol Vue kodisiz ancha sodda yozilishi mumkin, ammo sabr qiling. Vue-ning haqiqiy afzalliklarini moslashuvchan sahifalar yaratganimizda keyingi misollarda ko'rasiz.
{% endhint %}

### W3schoolsda Vue-ni o'rganish

W3Schools.com saytida Vue-ni o'rganayotganda kod va natijani ko'rstuvchi "O'zingiz sinab ko'ring" vositamizdan foydalanishingiz mumkin. Bu keyingi mavzularga o'tish davomida har bir qismni tushunishingizni osonlashtiradi.

Qo'llanmani davom ettirish uchun "Keyingi" tugmasini bosing.
