---
description: >-
  HTMLning <picture> elementi turli qurilmalar ekraniga mos bir nechta rasmlarni
  joylashtirish imkonini beradi.
---

# Picture elementi

<figure><img src="../../../.gitbook/assets/image (298).png" alt=""><figcaption></figcaption></figure>

## HTMLdagi \<picture> elementi

HTMLning \<picture> elementi veb dasturchilarga rasmlarni berishda bir necha moslashuvchanlik imkoniyatini beradi.

\<picture> elementi bir yoki bir nechta \<source> elementlarini o'z ichiga oladi, ularning har biri srcset attributi orqali turli rasmlarni ko'rsatadi. Brauzer shu tarzda \<img> tegiga berilgan rasmni yoki qurilma ekraninga mos keladigan rasmni ko'rsatishi mumkin.

Har bir \<source> elementi berilgan rasm qachon ekranga mos kelishini belgilab beruvchi media attributiga ega

{% code title="Turli ekran o'lchamlari uchun turli xil rasmlarni ko'rsatish:" %}
```
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg">
  <source media="(min-width: 465px)" srcset="img_car.jpg">
  <img src="img_girl.jpg">
</picture> 
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** \<img> elementini har doim \<picture> elementining oxirgi bola elementi sifatida kiriting.  `<img>`elementi `<picture>` elementini qo'llab-quvvatlamaydigan yoki `<source>`teglarning hech biri mos kelmagan holatda, brauzerlar tomonidan ishlatiladi.
{% endhint %}

## Picture elementidan qachon foydalanish kerak ?

&#x20;`<picture>` elementining ikkita asosiy maqsadi bor:

### 1. Bandwidth

Agar ekraningiz yoki qurilmangiz kichkina bo'lsa, katta hajmdagi rasmni yuklash shart emas. Brauzer attribut qiymatlariga mos keladigan birinchi  `<source>` elementidan foydalanadi va qolgan elementlarga e'tibor bermaydi.

### 2. Formatni qo'llab-quvvatlash

Ba'zi brauzerlar yoki qurilmalar barcha rasm formatlarini qo'llab-quvvatlamasligi mumkin.  `<picture>` elementidan foydalanib barcha formatdagi rasmlarni qo'shishingiz mumkin va brauzer ularning orasidan o'zi qo'llab quvvatlaydigan formatdagi birinchi rasmdan foydalanadi va qolgan elementlarga e'tibor bermaydi.

{% code title="Brauzer o'zi qo'llab quvvatlayidigan birinchi rasm formatidan foydalanadi:" %}
```
<picture>
  <source srcset="img_avatar.png">
  <source srcset="img_girl.jpg">
  <img src="img_beatles.gif" alt="Beatles" style="width:auto;">
</picture>
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Brauzer mos keladigan birinchi \<source> elementidan foydalanadi va qolgan barcha`<source>`elementlarga e'tibor bermaydi.
{% endhint %}

## HTML rasm teglari

| Teg        | Tavsif                                          |
| ---------- | ----------------------------------------------- |
| \<img>     | Rasm joylashtirish                              |
| \<map>     | Rasm xaritasini ifodalash                       |
| \<area>    | Rasn xaritasidagi bosiluvchi maydonni belgilash |
| \<picture> | Resurslarda bir nechta rasmlarni joylashtirish  |
