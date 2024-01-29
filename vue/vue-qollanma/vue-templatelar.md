# Vue Templatelar

{% hint style="success" %}
Vue-dagi shablon bu bizning Vue ilovamizning HTML qismi deb ataydigan narsadir **.**

\<template> tegi keyinchalik \*.vue fayllarida kodimizni yaxshiroq tuzilish uchun ishlatiladi **.**

Vue misolida **shablonni** konfiguratsiya opsiyasi sifatida ishlatish va HTML kodini ichiga qo'yish mumkin.
{% endhint %}

### TheVue Template

Keling, konfiguratsiya opsiyasi sifatida "shablon" dan foydalanadigan misolni ko'rib chiqaylik. Bu oddiy misol, biz HTML qismini hozirgina "shablon" konfiguratsiya opsiyasiga o'tkazdik:



Ichkaridagi HTML mazmuni `<div id="app">`qo'shtirnoq ostidagi "shablon" konfiguratsiya opsiyasiga o'tkaziladi `` `...` ``. Biz ko'p HTML qatorlarini orqaga tikilgan iqtibos ichiga yozishimiz mumkin.

```
<div id="app"></div>

<script src="https://unpkg.com/vue@3/dist/vue.global.js"></script>
<script>
  const app = Vue.createApp({
    template:
      `<h1>{{ message }}</h1>
      <p>This is a second line of HTML code, inside backtick quotes</p>`,
    data() {
      return {
        message: "Hello World!"
      }
    }
  })
app.mount('#app')
</script>
```

### Yagona fayl komponentlari (SFCs)

Yuqoridagi kod misolida ko'rib turganingizdek, Vue ilovamizning HTML qismi ham Vue misolida to'planishi mumkin, ammo bu HTML faylida umumiy ko'rinishni olishni osonlashtirmaydi.

Yaxshiroq ko‘rinish olish, yirikroq loyihalarni boshqarishni osonlashtirish va yaxshi rivojlanish muhitiga ega bo‘lish uchun biz endi Vue kodimizni SFC yoki \*.vue fayllarida yozishga o‘tamiz.

Barcha \*.vue fayllari faqat uch qismdan iborat:

* `<template>`HTML tarkibi qayerda.
* `<script>`Vue kodimiz uchun.
* `<style>`qaerda biz CSS uslubini yozamiz.

Lekin loyihamizda \*.vue fayllaridan foydalanishimizdan oldin kompyuterimizni boshqa usulda sozlashimiz kerak. Ushbu qo'llanmaning keyingi sahifalarida buni tushuntirib beradi.
