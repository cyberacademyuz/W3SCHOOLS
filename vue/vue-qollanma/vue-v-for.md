# Vue v-for

{% hint style="success" %}
**Oddiy JavaScript bilan** siz massiv asosida HTML elementlarini yaratishni xohlashingiz mumkin. Siz for-loopdan foydalanasiz va ichida siz elementlarni yaratishingiz, ularni sozlashingiz va keyin har bir elementni sahifangizga qo'shishingiz kerak. Va bu elementlar massivdagi o'zgarishlarga munosabat bildirmaydi.

**Vue bilan** siz ro'yxatda yaratmoqchi bo'lgan HTML elementidan boshlaysiz, `v-for`atribut sifatida Vue misolidagi massivga murojaat qiling va qolganlari bilan Vue-ga g'amxo'rlik qilishga ruxsat bering. Va bilan yaratilgan elementlar `v-for`massiv o'zgarganda avtomatik ravishda yangilanadi.
{% endhint %}

### ro'yxatni ko'rsatish

**Vue-da ro'yxatni ko'rsatish** direktiv yordamida amalga oshiriladi `v-for`, shuning uchun bir nechta HTML elementlari for-loop bilan yaratiladi.

Quyida `v-for`ishlatiladigan uchta bir oz farqli misollar mavjud.

Massiv elementlari asosida ro‘yxatni ko‘rsatish.

```
<ol>
  <li v-for="x in manyFoods">{{ x }}</li>
</ol>
```

### Massivga aylanish

Turli xil tasvirlarni ko'rsatish uchun massivni aylantiring:

Vue misolidagi massiv asosida oziq-ovqat tasvirlarini ko'rsatish.

```
<div>
  <img v-for="x in manyFoods" v-bind:src="x">
</div>
```

### Ob'ektlar massivi orqali aylanish

Ob'ektlar massivini aylantiring va ob'ekt xususiyatlarini ko'rsating:

Vue misolidagi massiv asosida har xil turdagi oziq-ovqatlarning tasvirlari va nomlarini ko'rsating.

```
<div>
  <figure v-for="x in manyFoods">
    <img v-bind:src="x.url">
    <figcaption>{{ x.name }}</figcaption>
  </figure>
</div>
```

### Indeksni oling

Massiv elementining indeks raqami JavaScript for-looplarida haqiqatan ham foydali bo'lishi mumkin. Yaxshiyamki, biz Vue-dan foydalanganda indeks raqamini `v-for`ham olishimiz mumkin.

Indeks raqamini olish uchun `v-for`qavs ichida ikkita vergul bilan ajratilgan so'zlarni berishimiz kerak: birinchi so'z massiv elementi, ikkinchi so'z esa ushbu massiv elementining indeksi bo'ladi.

Vue misolidagi "manyFoods" massividagi elementlarning indeks raqami va oziq-ovqat nomini ko'rsating.

```
<p v-for="(x, index) in manyFoods">
  {{ index }}: "{{ x }}" <br>
</p>
```

Agar massiv elementlari obyekt bo‘lsa, biz massiv elementi indeksini ham, massiv elementining o‘zidan olingan ma’lumotlarni ham ko‘rsatishimiz mumkin:

Massiv elementi indeks raqamini va "manyFoods" massividagi ob'ektlardan matnni ko'rsating.

```
<p v-for="(x, index) in manyFoods">
  {{ index }}: "{{ x.name }}", url: "{{ x.url }}" <br>
</p>
```
