---
description: Rasm xaritalari bilan ramning bosiluvchi maydonini yaratishingiz mumkin
---

# Rasm xaritalari

## Rasm xaritalari

HTMLning \<mao> tegi rasmning xaritasini belgilab beradi. Rasm xaritasi rasmning bosiluvchi maydoni hisoblanadi. Bu maydo bir yoki bir nechta \<area> teglari bilan belgilanadi.

Quyidagi rasmda joylashgan kompyuter, telefon yoki qahva finjonini bosib ko'ring:

![](<../../../.gitbook/assets/image (339).png>)

{% code title="Bu yuqoridagi rasm xaritasining HTML kodi" %}
```
 <img src="workplace.jpg" alt="Workplace" usemap="#workmap">

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
</map> 
```
{% endcode %}

## Bu qanday ishlaydi ?

Rasm xaritasining g'oyasi shundaki, siz rasmning qayerini bosganingizga qarab turli xil amallarni bajarishingiz kerak.

Rasm xaritasini yaratish uchun sizga rasm va bosiladigan maydonlarni belgilab beruvchi HTML kod kerak bo'ladi.

## Tasvir

Rasn  `<img>` tegi yordamida kiritiladi. Uning boshqa rasmlardan yagona farq shundaki, siz unga `usemap` attributini qo'shishingiz kerak:

```
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">
```

Usemap qiymati rasm xaritasi nomidan keyin `#` hesh teg bilan boshlanadi va rasm va rasm xaritasi o'rtasida aloqa yaratish uchun ishlatiladi.

{% hint style="warning" %}
**Maslahat:** Rasm xaritasi sifatida istalgan rasmdan foydalanishingiz mumkin!
{% endhint %}

## Rasmlar xaritasini yaratish

Keyin, \<map> elementini qo'shing.

\<map> elementi rasm haritaisini yaratish uchun ishlatiladi va talab qilinuvchi name attributi bilan bog'lanadi.

```
<map name="workmap">
```

name attributi \<img> elementining usemap attributi kabi bir xil qiymatga ega bo'lishi shart.

## Maydonlar

Keyin, bosiluvchi maydonnin qo'shing.

Bosiluvchi maydon \<area> elementi bilan beriladi.

### Shakl

Bosiluvchi maydonning shaklini belgilashingiz shart va quyidagi qiymatlardan birini tanlashingiz mumkin:

* `rect`- to'rtburchak maydonni belgilaydi
* `circle`- doira maydonini belgilaydi
* `poly`- ko'pburchakli maydonni belgilaydi
* `default`- butun hududni belgilaydi

Rasmning bosiladigan maydonini joylashtirish uchun ba'zi koordinatalarni ham berishingiz kerak.

### Shape="rect"

`shape="rect"` uchun kordinatalar juft hisoblanib, biri x boshqasi y o'qi uchun bo'ladi.

Shunday qilib,  `34,44` koordinatalar rasmning chap tomonidan 34 piksel va yuqorisidan 44 piksel masofada joylashadi:

![](<../../../.gitbook/assets/image (334).png>)

`270,350` koordinatalar rasmning chap tomonidan 34 piksel va yuqorisidan 44 piksel masofada joylashadi:

![](<../../../.gitbook/assets/image (314).png>)

Endi bizda bosiladigan to'rtburchaklar maydonini yaratish uchun yetarli ma'lumotlar bor:

```
<area shape="rect" coords="34, 44, 270, 350" href="computer.htm"> 
```

Bu bosiluvchi maydon hisoblanadi va foydalanuvchini "computer.htm" sahifasiga o'tkazadi.

![](<../../../.gitbook/assets/image (341).png>)

### Shape="circle"

Aylana maydonni qo'shish uchun avval aylana markazining koordinatalarini toping:

`337,300`

![](<../../../.gitbook/assets/image (820).png>)

Keyin aylananing radiusini belgilang:

44 piksel

![](<../../../.gitbook/assets/image (329).png>)

Ana endi bosiladigan aylana maydonni yaratish uchun yetarli ma'lumotlarga egasiz:

```
<area shape="circle" coords="337, 300, 44" href="coffee.htm">
```

Bu bosiladigan maydon hisoblanib, foydalanuvchini "coffe.htm" sahifasiga o'tkazadi:

![](<../../../.gitbook/assets/image (321).png>)

### Shape="poly"

shape="poly" to'g'ri chiziqlar bilan hosil qilingan shaklni yaratadigan bir nechta kordinata nuqtalarini o'z ichiga oladi .

Bu har qanday shaklni yaratish uchun ishlatilishi mumkin.

Huddi, kruvasan shakli kabi!

Qanday qilib ushbu rasmdagi kruvasanni&#x20;



bosiladigan havolaga aylantirishimiz mumkin ?

![](<../../../.gitbook/assets/image (297).png>)

Kruvasanning barcha qirralari uchun x va y koordinatalarini topishimiz kerak:

![](<../../../.gitbook/assets/image (358).png>)

Kordinatalar juft qilib yoziladi, biri x boshqasi y o'qi uchun bo'ladi:

```html
<area shape="poly" 
 coords="140,121,181,116,204,160,204,222,191,270,140,329,85,355,58,352,37,322,40,259,103,161,128,147"
 href="croissant.htm"> 
```

Bu bosiladigan maydon hisoblanib, foydalanuvchini "coffe.htm" sahifasiga o'tkazadi:

![](<../../../.gitbook/assets/image (325).png>)

## Rasm haritasi va Javascript

Bosluvchi maydonni javascript yordamida ham yaratish mumkin.

JavaScript funktsiyasini ishlashi uchun \<area> elementiga `click` hodisasini qo'shing:

{% code title="Bu yerda biz maydon bosilganda JavaScript funksiyasini bajarish uchun onclick atributidan foydalanamiz:" %}
```
<map name="workmap">
  <area shape="circle" coords="337,300,44" href="coffee.htm" onclick="myFunction()">
</map>

<script>
function myFunction() {
  alert("You clicked the coffee cup!");
}
</script>
```
{% endcode %}

## Bo'lim xulosasi

Rasm xaritasini belgilash uchun \<map> elementidan foydalaning

Rasm xaritasidagi bosiluvchi maydonni belgilash uchun \<area> elementidan foydalaning

Rasm xaritasini bog'lash uchun \<img> elementining usemap attributidan foydalaning

## HTML rasm teglari

| Teg        | Tavsif                                          |
| ---------- | ----------------------------------------------- |
| \<img>     | Rasm joylashtirish                              |
| \<map>     | Rasm xaritasini ifodalash                       |
| \<area>    | Rasn xaritasidagi bosiluvchi maydonni belgilash |
| \<picture> | Resurslarda bir nechta rasmlarni joylashtirish  |
