# Vue v-bind

{% hint style="success" %}
Allaqachon Vue-ning asosiy sozlamalari Vue misolidan iborat ekanligini va biz unga `<div id="app">` tegidan `{{}}` yoki `v-bind` direktivasi orqali murojaat qilishimizz mumkinligini ko'rdingiz.

Ushbu sahifada `v-bind` direktivasini batafsilroq tushuntiramiz.
{% endhint %}

### `v-bind` direktivasi

&#x20;`v-bind` direktivasi HTML atributini Vue dagi ma'lumotlarga bog'lash imkonini beradi. Bu atribut qiymatini dinamik tarzda o'zgartirishni osonlashtiradi.

{% code title="sintaksis" %}
```
<div v-bind:[attribute]="[Vue data]"></div>
```
{% endcode %}

`<img>` tegning `src` atributi qiymati Vue namunasi ma'lumotlar xususiyati "url" dan olingan:

```
<img v-bind:src="url">
```

### CSS ulanishi

`v-bind`Biz direktivadan in-line uslublarini bajarish va sinflarni dinamik ravishda o'zgartirish uchun foydalanishimiz mumkin . Buni qanday qilishni ushbu bo'limda qisqacha ko'rsatamiz va keyinroq ushbu qo'llanmada [CSS Binding sahifasida](https://www-w3schools-com.translate.goog/vue/vue\_css-binding.php?\_x\_tr\_sl=de&\_x\_tr\_tl=uz&\_x\_tr\_hl=ru&\_x\_tr\_pto=wapp) buni batafsilroq tushuntiramiz.

### Bog'lash uslubi

Vue bilan chiziqli uslublar uslub atributini Vue bilan bog'lash orqali amalga oshiriladi `v-bind`.

v-bind direktivasiga qiymat sifatida biz CSS xususiyati va qiymatiga ega JavaScript obyektini yozishimiz mumkin:

Shrift o'lchami Vue ma'lumotlarining "size" xususiyatiga bog'liq.

```
<div v-bind:style="{ fontSize: size }">
  Text example
</div>
```

Agar xohlasak, shrift o'lchami raqami qiymatini shrift o'lchami birligidan ajratishimiz mumkin, masalan:

Shrift o'lchami raqami qiymati Vue ma'lumotlar xususiyati "size" saqlanadi.

```
<div v-bind:style="{ fontSize: size + 'px' }">
  Text example
</div>
```

Biz CSS xususiyati nomini CSS sintaksisi (kabob-rejismoz) bilan tire ichida yozishimiz ham mumkin, ammo bu tavsiya etilmaydi:

CSS-ning fontSize xususiyati "shrift o'lchami" deb ataladi.

```
<div v-bind:style="{ 'font-size': size + 'px' }">
  Text example
</div>
```

Fon rangi Vue misolidagi "bgVal" ma'lumotlar xususiyati qiymatiga bog'liq.

```
<div v-bind:style="{ backgroundColor: 'hsl('+bgVal+',80%,80%)' }">
  Notice the background color on this div tag.
</div>
```

Fon rangi "isImportant" ma'lumotlar xususiyati qiymati "haqiqiy" yoki "noto'g'ri" ekanligiga qarab **JavaScript shartli (uchlik) ifodasi** bilan o'rnatiladi .

```
<div v-bind:style="{ backgroundColor: isImportant ? 'lightcoral' : 'lightgray' }">
  Conditional background color
</div>
```

### Sinfni bog'lash

`v-bind`Biz sinf atributini o'zgartirish uchun foydalanishimiz mumkin .

ning qiymati `v-bind:class`o'zgaruvchi bo'lishi mumkin:

Ism `class`"className" Vue ma'lumotlar xususiyatidan olingan:

```
<div v-bind:class="className">
  The class is set with Vue
</div>
```

ning qiymati `v-bind:class`ham ob'ekt bo'lishi mumkin, bu erda sinf nomi faqat "true" ga o'rnatilgan bo'lsa kuchga kiradi:

Atribut `class`"myClass" klassi "haqiqiy" yoki "noto'g'ri" ga o'rnatilganligiga qarab tayinlanadi yoki tayinlanmaydi:

```
<div v-bind:class="{ myClass: true }">
  The class is set conditionally to change the background color
</div>
```

Qiymati `v-bind:class`ob'ekt bo'lsa, sinf Vue xususiyatiga qarab tayinlanishi mumkin:

Atribut class"isImportant" xususiyatiga qarab tayinlanadi, agar u "haqiqat" yoki "noto'g'ri" bo'lsa:

```
<div v-bind:class="{ myClass: isImportant }">
  The class is set conditionally to change the background color
</div>
```

### uchun qisqa qo'l`v-bind`

'' stenografiyasi `v-bind:`oddiygina '`:`'.

Bu erda biz ' ' o'rniga ' ' yozamiz `v-bind:`:

```
<div :class="{ impClass: isImportant }">
  The class is set conditionally to change the background color
</div>
```

`v-bind:`Biz chalkashmaslik uchun ushbu qo'llanmada sintaksisdan foydalanishni davom ettiramiz.
