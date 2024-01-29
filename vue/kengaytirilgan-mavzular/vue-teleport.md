# Vue Teleport

{% hint style="success" %}
Vue `<Teleport>`yorlig'i kontentni DOM strukturasidagi boshqa joyga ko'chirish uchun ishlatiladi.
{% endhint %}

### \<Teleport> va 'to' atributi

`<Teleport>`Ba'zi kontentni DOM strukturasidagi boshqa joyga ko'chirish uchun biz kontent atrofidagi Vue tegidan va uni qaerga ko'chirishni aniqlash uchun "to" atributidan foydalanamiz .

```html
<Teleport to="body">
  <p>Hello!</p>
</Teleport>
```

'to' atribut qiymati CSS belgisi sifatida berilgan, shuning uchun agar biz yuqoridagi koddagi kabi ba'zi kontentni tana tegiga yubormoqchi bo'lsak, shunchaki yozamiz `<Teleport to="body">`.

Sahifani yuklangandan so'ng tekshirish orqali kontent asosiy tegga ko'chirilganligini ko'rishimiz mumkin.

{% code title="CompOne.vue:" %}
```html
<template>
  <div>
    <h2>Component</h2>
    <p>This is the inside of the component.</p>
    <Teleport to="body">
      <div id="redDiv">Hello!</div>
    </Teleport>
  </div>
</template>
```
{% endcode %}

`<div>`Agar biz sahifamizni o'ng tugmasini bosib, "Tekshirish" ni tanlasak, qizil element komponentdan tashqariga va teg oxiriga ko'chirilganligini ko'rishimiz mumkin `<body>`.

<figure><img src="https://www.w3schools.com/vue/img_teleport-DOM.png" alt=""><figcaption></figcaption></figure>

Shuningdek, bizda, masalan, identifikatori bo'lgan teg bo'lishi mumkin `<div id="receivingDiv">`va biz teleport/ko'chirmoqchi bo'lgan kontentdan `<div>`foydalanib, ba'zi tarkibni teleportatsiya qilishimiz mumkin.`<Teleport to="#receivingDiv">`

### Teleportlangan elementlarning skripti va uslubi

Ba'zi kontent tegli komponentdan ko'chirilgan bo'lsa ham , va `<Teleport>`teglaridagi komponent ichidagi tegishli kod ko'chirilgan kontent uchun ishlaydi.`<script><style>`

Teglar `<style>`va teglardagi tegishli kod kompilyatsiyadan keyin komponent ichida bo'lmasa ham `<script>`teleportlangan teg uchun ishlaydi .`<div>`

{% code title="CompOne.vue:" %}
```html
<template>
  <div>
    <h2>Component</h2>
    <p>This is the inside of the component.</p>
    <Teleport to="body">
      <div 
        id="redDiv" 
        @click="toggleVal = !toggleVal" 
        :style="{ backgroundColor: bgColor }"
      >
        Hello!<br>
        Click me!
      </div>
    </Teleport>
  </div>
</template>

<script>
export default {
  data() {
    return {
      toggleVal: true
    }
  },
  computed: {
    bgColor() {
      if (this.toggleVal) {
        return 'lightpink'
      }
      else {
        return 'lightgreen'
      }
    }
  }
}
</script>

<style scoped>
#redDiv {
  margin: 10px;
  padding: 10px;
  display: inline-block;
}

#redDiv:hover {
  cursor: pointer;
}
</style>
```
{% endcode %}
