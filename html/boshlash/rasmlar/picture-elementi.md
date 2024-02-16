---
description: >-
  HTMLning <picture> elementi turli qurilmalar ekraniga mos bir nechta rasmlarni
  joylashtirish imkonini beradi.
---

# Picture elementi

<figure><img src="../../../.gitbook/assets/image (298).png" alt=""><figcaption></figcaption></figure>

## <mark style="color:green;">HTMLning</mark> <mark style="color:green;"></mark><mark style="color:green;">`<picture>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

HTMLning <mark style="color:red;">`<picture>`</mark> elementi veb dasturchilarga rasmlarni berishda bir necha moslashuvchanlik imkoniyatini beradi.

<mark style="color:red;">`<picture>`</mark> elementi bir yoki bir nechta <mark style="color:red;">`<source>`</mark> elementlarini o'z ichiga oladi, ularning har biri <mark style="color:red;">`srcset`</mark> attributi orqali turli rasmlarni ko'rsatadi. Brauzer shu tarzda <mark style="color:red;">`<img>`</mark> tegiga berilgan rasmni yoki qurilma ekraninga mos keladigan rasmni ko'rsatishi mumkin.

Har bir <mark style="color:red;">\<source></mark> elementi berilgan rasm qachon ekranga mos kelishini belgilab beruvchi <mark style="color:red;">`media`</mark> attributiga ega

{% code title="Turli ekran o'lchamlari uchun turli xil rasmlarni ko'rsatish:" %}
```html
<picture>
  <source media="(min-width: 650px)" srcset="img_food.jpg">
  <source media="(min-width: 465px)" srcset="img_car.jpg">
  <img src="img_girl.jpg">
</picture> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_picture1" %}

{% hint style="warning" %}
**Eslatma:** <mark style="color:red;">`<img>`</mark> elementini har doim <mark style="color:red;">`<picture>`</mark> elementining oxirgi bola elementi sifatida kiriting.  <mark style="color:red;">`<img>`</mark> elementi <mark style="color:red;">`<picture>`</mark> elementini qo'llab-quvvatlamaydigan yoki <mark style="color:red;">`<source>`</mark> teglarning hech biri mos kelmagan holatda, brauzerlar tomonidan ishlatiladi.
{% endhint %}

## <mark style="color:green;">Picture elementidan qachon foydalanish kerak ?</mark>

&#x20;<mark style="color:red;">`<picture>`</mark> elementining ikkita asosiy maqsadi bor:

### 1. Bandwidth

Agar ekraningiz yoki qurilmangiz kichkina bo'lsa, katta hajmdagi rasmni yuklash shart emas. Brauzer attribut qiymatlariga mos keladigan birinchi  <mark style="color:red;">`<source>`</mark> elementidan foydalanadi va qolgan elementlarga e'tibor bermaydi.

### 2. Formatni qo'llab-quvvatlash

Ba'zi brauzerlar yoki qurilmalar barcha rasm formatlarini qo'llab-quvvatlamasligi mumkin.  <mark style="color:red;">`<picture>`</mark> elementidan foydalanib barcha formatdagi rasmlarni qo'shishingiz mumkin va brauzer ularning orasidan o'zi qo'llab quvvatlaydigan formatdagi birinchi rasmdan foydalanadi va qolgan elementlarga e'tibor bermaydi.

{% code title="Brauzer o'zi qo'llab quvvatlayidigan birinchi rasm formatidan foydalanadi:" %}
```html
<picture>
  <source srcset="img_avatar.png">
  <source srcset="img_girl.jpg">
  <img src="img_beatles.gif" alt="Beatles" style="width:auto;">
</picture>
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_picture_format" %}

{% hint style="warning" %}
**Eslatma:** Brauzer mos keladigan birinchi <mark style="color:red;">`<source>`</mark> elementidan foydalanadi va qolgan barcha<mark style="color:red;">`<source>`</mark>elementlarga e'tibor bermaydi.
{% endhint %}

## HTML rasm teglari

| Teg        | Tavsif                                          |
| ---------- | ----------------------------------------------- |
| \<img>     | Rasm joylashtirish                              |
| \<map>     | Rasm xaritasini ifodalash                       |
| \<area>    | Rasn xaritasidagi bosiluvchi maydonni belgilash |
| \<picture> | Resurslarda bir nechta rasmlarni joylashtirish  |
