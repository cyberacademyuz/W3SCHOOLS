---
description: Rasm xaritalari bilan ramning bosiluvchi maydonini yaratishingiz mumkin
---

# Rasm xaritalari

## <mark style="color:green;">Rasm xaritalari</mark>

HTMLning <mark style="color:red;">`<map>`</mark> tegi rasmning xaritasini belgilab beradi. Rasm xaritasi rasmning bosiluvchi maydoni hisoblanadi. Bu maydo bir yoki bir nechta <mark style="color:red;">`<area>`</mark> teglari bilan belgilanadi.

Quyidagi rasmda joylashgan kompyuter, telefon yoki qahva finjonini bosib ko'ring:

![](<../../../.gitbook/assets/image (339).png>)

{% code title="Bu yuqoridagi rasm xaritasining HTML kodi" %}
```html
 <img src="workplace.jpg" alt="Workplace" usemap="#workmap">

<map name="workmap">
  <area shape="rect" coords="34,44,270,350" alt="Computer" href="computer.htm">
  <area shape="rect" coords="290,172,333,250" alt="Phone" href="phone.htm">
  <area shape="circle" coords="337,300,44" alt="Coffee" href="coffee.htm">
</map> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_map2" %}

## <mark style="color:green;">Bu qanday ishlaydi ?</mark>

Rasm xaritasining g'oyasi shundaki, siz rasmning qayerini bosganingizga qarab turli xil amallarni bajarishingiz kerak.

Rasm xaritasini yaratish uchun sizga rasm va bosiladigan maydonlarni belgilab beruvchi HTML kod kerak bo'ladi.

## <mark style="color:green;">Tasvir</mark>

Rasn  <mark style="color:red;">`<img>`</mark> tegi yordamida kiritiladi. Uning boshqa rasmlardan yagona farq shundaki, siz unga <mark style="color:red;">`usemap`</mark> attributini qo'shishingiz kerak:

```html
<img src="workplace.jpg" alt="Workplace" usemap="#workmap">
```

<mark style="color:red;">`usemap`</mark> qiymati rasm xaritasi nomidan keyin <mark style="color:red;">`#`</mark> hesh teg bilan boshlanadi va rasm va rasm xaritasi o'rtasida aloqa yaratish uchun ishlatiladi.

{% hint style="warning" %}
**Maslahat:** Rasm xaritasi sifatida istalgan rasmdan foydalanishingiz mumkin!
{% endhint %}

## <mark style="color:green;">Rasmlar xaritasini yaratish</mark>

Keyin, <mark style="color:red;">`<map>`</mark> elementini qo'shing.

<mark style="color:red;">`<map>`</mark> elementi rasm haritaisini yaratish uchun ishlatiladi va talab qilinuvchi name attributi bilan bog'lanadi.

```html
<map name="workmap">
```

<mark style="color:red;">`name`</mark> attributi <mark style="color:red;">`<img>`</mark> elementining <mark style="color:red;">`usemap`</mark> attributi kabi bir xil qiymatga ega bo'lishi shart.

## <mark style="color:green;">Maydonlar</mark>

Keyin, bosiluvchi maydonnin qo'shing.

Bosiluvchi maydon <mark style="color:red;">`<area>`</mark> elementi bilan beriladi.

### <mark style="color:green;">Shakl</mark>

Bosiluvchi maydonning shaklini belgilashingiz shart va quyidagi qiymatlardan birini tanlashingiz mumkin:

* <mark style="color:red;">`rect`</mark>- to'rtburchak maydonni belgilaydi
* <mark style="color:red;">`circle`</mark>- doira maydonini belgilaydi
* <mark style="color:red;">`poly`</mark>- ko'pburchakli maydonni belgilaydi
* <mark style="color:red;">`default`</mark>- butun hududni belgilaydi

Rasmning bosiladigan maydonini joylashtirish uchun ba'zi koordinatalarni ham berishingiz kerak.

### <mark style="color:green;">Shape="rect"</mark>

<mark style="color:red;">`shape="rect"`</mark> uchun kordinatalar juft hisoblanib, biri x boshqasi y o'qi uchun bo'ladi.

Shunday qilib,  <mark style="color:red;">`34,44`</mark> koordinatalar rasmning chap tomonidan 34 piksel va yuqorisidan 44 piksel masofada joylashadi:

![](<../../../.gitbook/assets/image (334).png>)

<mark style="color:red;">`270,350`</mark> koordinatalar rasmning chap tomonidan 34 piksel va yuqorisidan 44 piksel masofada joylashadi:

![](<../../../.gitbook/assets/image (314).png>)

Endi bizda bosiladigan to'rtburchaklar maydonini yaratish uchun yetarli ma'lumotlar bor:

```html
<area shape="rect" coords="34, 44, 270, 350" href="computer.htm"> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_map3" %}

Bu bosiluvchi maydon hisoblanadi va foydalanuvchini "computer.htm" sahifasiga o'tkazadi.

![](<../../../.gitbook/assets/image (341).png>)

### Shape="circle"

Aylana maydonni qo'shish uchun avval aylana markazining koordinatalarini toping:

`337,300`

![](<../../../.gitbook/assets/image (820).png>)

Keyin aylananing radiusini belgilang:

<mark style="color:red;">`44`</mark>piksel

![](<../../../.gitbook/assets/image (329).png>)

Ana endi bosiladigan aylana maydonni yaratish uchun yetarli ma'lumotlarga egasiz:

```html
<area shape="circle" coords="337, 300, 44" href="coffee.htm">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_map4" %}

Bu bosiladigan maydon hisoblanib, foydalanuvchini "coffe.htm" sahifasiga o'tkazadi:

![](<../../../.gitbook/assets/image (321).png>)

### <mark style="color:green;">Shape="poly"</mark>

<mark style="color:red;">`shape="poly"`</mark> to'g'ri chiziqlar bilan hosil qilingan shaklni yaratadigan bir nechta kordinata nuqtalarini o'z ichiga oladi.

Bu har qanday shaklni yaratish uchun ishlatilishi mumkin.

Huddi, kruvasan shakli kabi!

Qanday qilib ushbu rasmdagi kruvasanni bosiladigan havola qilish mumkin ?

![](<../../../.gitbook/assets/image (297).png>)

Kruvasanning barcha qirralari uchun x va y koordinatalarini topishimiz kerak:

![](<../../../.gitbook/assets/image (358).png>)

Kordinatalar juft qilib yoziladi, biri x boshqasi y o'qi uchun bo'ladi:

```html
<area shape="poly" 
 coords="140,121,181,116,204,160,204,222,191,270,140,329,85,355,58,352,37,322,40,259,103,161,128,147"
 href="croissant.htm"> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_map_croissant" %}

Bu bosiladigan maydon hisoblanib, foydalanuvchini "coffe.htm" sahifasiga o'tkazadi:

![](<../../../.gitbook/assets/image (325).png>)

## <mark style="color:green;">Rasm haritasi va Javascript</mark>

Bosluvchi maydonni javascript yordamida ham yaratish mumkin.

JavaScript funksiyasini ishlashi uchun <mark style="color:red;">`<area>`</mark> elementiga <mark style="color:red;">`click`</mark> hodisasini qo'shing:

{% code title="Bu yerda biz maydon bosilganda JavaScript funksiyasini bajarish uchun onclick atributidan foydalanamiz:" %}
```html
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

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_images_map5" %}

## <mark style="color:green;">Bo'lim xulosasi</mark>

Rasm xaritasini belgilash uchun <mark style="color:red;">`<map>`</mark> elementidan foydalaning

Rasm xaritasidagi bosiluvchi maydonni belgilash uchun <mark style="color:red;">`<area>`</mark> elementidan foydalaning

Rasm xaritasini bog'lash uchun <mark style="color:red;">`<img>`</mark> elementining usemap attributidan foydalaning

## <mark style="color:green;">Rasmga aloqador teglar</mark>

| Teg        | Tavsif                                          |
| ---------- | ----------------------------------------------- |
| \<img>     | Rasm joylashtirish                              |
| \<map>     | Rasm xaritasini ifodalash                       |
| \<area>    | Rasn xaritasidagi bosiluvchi maydonni belgilash |
| \<picture> | Resurslarda bir nechta rasmlarni joylashtirish  |
