---
description: Rasmlar veb-sahifaning dizayni va ko'rinishini yaxshilaydi.
---

# Rasmlar

<figure><img src="../../../.gitbook/assets/image (389).png" alt=""><figcaption></figcaption></figure>

{% code title="Misol" %}
```
<img src="pic_trulli.jpg" alt="Italian Trulli">
```
{% endcode %}

{% code title="Misol" %}
```
<img src="img_girl.jpg" alt="Girl in a jacket">
```
{% endcode %}

{% code title="Misol:" %}
```
<img src="img_chania.jpg" alt="Flowers in Chania">
```
{% endcode %}

## HTML Rasmlar sintaksisi

HTMLda `<img>` tegi rasmni veb-sahifaga joylashtirish uchun ishlatiladi.

Rasmlar texnik jihatdan veb-sahifaga joylashtirilmaydi; ular veb-sahifalarga havola sifatida ulanadi.  `<img>` tegi ulaniladigan rasmni saqlash uchun joy yaratadi.

`<img>` tegi toq teg hisoblanib faqatgina attributlarni o'z ichiga oladi va tag yopilmaydi.

`<img>` tegi 2 ta attribut talab qiladi.

* `src` - Rasmning joyashuvi
* `alt` - Rasm uchun alternativ matn

{% code title="Sintaksis" %}
```
 <img src="url" alt="alternatetext"> 
```
{% endcode %}

## src attributi

`src` atributi rasm uchun uning joylashuvi (URL) ni talab qiladi

**Eslatma:** Veb-sahifa yuklanganda, brauzer rasmni veb-serverdan oladi va uni sahifaga kiritadi. Shuning uchun, rasm havolasi to'g'ri ekanligiga ishonch hosil qiling, aks holda foydalanuvchilaringiz havola noto'g'ri ulanganda chiqadigan belgini ko'rishadi. Agar brauzer rasmni topa olmasa, belgi va `alt` attributidagi matn ko'rsatiladi.

{% code title="Misol" %}
```
<img src="img_chania.jpg" alt="Flowers in Chania"> 
```
{% endcode %}

## alt attributi

Agar foydalanuvchi biron sababga ko'ra rasmni ko'ra olmasa (internet sekinligi, `src` atributidagi xatolik yoki foydalanuvchi ekranni o'qish vositasidan foydalansa) `alt` atributi rasm uchun berilgan matnni ko'rsatadi.

Alt attributiga kiritilgan matn rasmni tasvirlab berishi kerak:

{% code title="Misol" %}
```
<img src="img_chania.jpg" alt="Flowers in Chania"> 
```
{% endcode %}

Agar brauzer rasmni topa olmasa, `alt` attributining qiymatiga kiritilgan matnni ko'rsatadi:

{% code title="Misol" %}
```
<img src="wrongname.gif" alt="Flowers in Chania"> 
```
{% endcode %}

{% hint style="warning" %}
**Maslahat:** Ekranni oʻqib beruvchi dasturlar HTML kodni oʻqiydi va foydalanuvchiga kontentni “eshitish” imkonini beradi. Ekranni o'qib beruvchi dasturlar ko'rish qobiliyati zaif yoki o'rganish imkoniyati cheklangan odamlar uchun foydalidir.
{% endhint %}

## Rasm o'lchami - Width va Height

`style` attributidan foydalanib rasmning eni va balandlik o'lchamini berishingiz mumkin.

{% code title="Misol:" %}
```
<img src="img_girl.jpg" alt="Girl in a jacket" style="width:500px;height:600px;"> 
```
{% endcode %}

`width` va `height` attributlari bilan ham buni boshqacharoq ko'rinishda amalga oshirishingiz mumkin.

{% code title="Misol:" %}
```
<img src="img_girl.jpg" alt="Girl in a jacket" width="500" height="600"> 
```
{% endcode %}

`width` va `height` attributlari rasmning eni va balandlgini pixellarda qabul qiladi.

{% hint style="warning" %}
**Eslatma:** Har doim rasmning eni va balandligini belgilang. Agar uning eni va balandligi ko'rsatilmagan bo'lsa, rasm yuklanayotganda veb-sahifa miltillashi mumkin.
{% endhint %}

## Width va Height yoki Stylemi ?

width, height va style atributlarining barchasi HTMLda to'g'ri ishlaydi.

Lekin, biz `style` atributdan foydalanishni maslahat beramiz. U CSS orqali o'zgartirilgan o'lchamlar sabab rasmning o'lchami o'zgarib ketishini oldini oladi:

{% code title="Misol:" %}
```
<!DOCTYPE html>
<html>
<head>
<style>
img {
  width: 100%;
}
</style>
</head>
<body>

<img src="html5.gif" alt="HTML5 Icon" width="128" height="128">

<img src="html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;">

</body>
</html> 
```
{% endcode %}

## Boshqa papkadagi rasmlar

Agar sizning rasmlaringiz boshqa  ichkipapkalarda bo'lsa papka nomini `src` attributiga kiritishingiz kerak:

{% code title="Misol:" %}
```
<img src="/images/html5.gif" alt="HTML5 Icon" style="width:128px;height:128px;"> 
```
{% endcode %}

## Boshqa server/veb-saytdagi rasmlar

Ba'zi web saytlar boshqa serverdagi rasmlarni ko'rsatadi.

Boshqa serverdagi rasmni ko'rsatish uchun `src` atributida to'liq URL manzilni ko'rsatishingiz kerak:

{% code title="Misol" %}
```
<img src="https://www.w3schools.com/images/w3schools_green.jpg" alt="W3Schools.com"> 
```
{% endcode %}

**Tashqi rasmlar bo'yicha eslatmalar:** tashqi rasmlar mualliflik huquqi ostida bo'lishi mumkin. Agar siz undan foydalanishga ruxsat olmagan bo'lsangiz, mualliflik huquqi qonunlarini buzgan bo'lishingiz mumkin. Bundan tashqari, siz tashqi rasmlarni nazorat qila olmaysiz; ular to'satdan olib tashlanishi yoki o'zgartirilishi mumkin.

## Animatsiyali rasmlar

HTML animatsiyali GIFlarni qabul qiladi:

```
<img src="programming.gif" alt="Computer Man" style="width:48px;height:48px;">
```

## Havola sifatidagi rasm

Rasmdan havola sifatida foydalanish uchun `<img>` tegini `<a>` tegining ichiga joylash kerak:

```
 <a href="default.asp">
  <img src="smiley.gif" alt="HTML tutorial" style="width:42px;height:42px;">
</a> 
```

## Floating (suzuvchi) rasm

Rasm matnning o'ng yoki chap tomonida turishi uchun CSSning `float` xususiyatidan foydalaning:

```
<p>
<img src="smiley.gif" alt="Smiley face" style="float:right;width:42px;height:42px;">
The image will float to the right of the text.
</p>

<p>
<img src="smiley.gif" alt="Smiley face" style="float:left;width:42px;height:42px;">
The image will float to the left of the text.
</p> 
```

## Rasmlarning umumiy format turlari

Bu yerda barcha brauzerlarda (Chrome, Edge, Firefox, Safari, Opera) qo'llab-quvvatlanadigan eng keng tarqalgan rasm format turlari ko'rsatilgan:

| Qisqartma | Fayl formati                          | Fayl kengaytmasi                 |
| --------- | ------------------------------------- | -------------------------------- |
| APNG      | Animated Portable Network Graphics    | .apng                            |
| GIF       | Graphics Interchange Format           | .gif                             |
| ICO       | Microsoft Icon                        | .ico, .cur                       |
| JPEG      | Joint Photographic Expert Group image | .jpg, .jpeg, .jfif, .pjpeg, .pjp |
| PNG       | Portable Network Graphics             | .png                             |
| SVG       | Scalable Vector Graphics              | .svg                             |

## Bo'lim hulosasi

* Rasmni ko'rsatish uchun HTMLning `<img>` elementidan foydalaning
* Rasmning joylashuvini ko'rsatish uchun HTMLning `src` attributidan foydalaning
* Rasm ko'rinmay qolganida u haqidagi matnni ko'rsatish uchun HTMLning `alt` attributidan foydalaning
* Rasmning o'lchamini berish uchun HTMLning width va height attributlaridan yoki CSS ning width va height xususiyatlaridan foydalaning
* Rasm o'ng yoki chap tomonga turishi uchun CSS ning float xususiyatidan foydalaning

{% hint style="warning" %}
**Eslatma:** Katta hajmdagi rasmlarni yuklash biroz vaqt talab qilishi va veb-sahifangizni sekinlashtirishi mumkin. Rasmlardan ehtiyotkorlik bilan foydalaning.
{% endhint %}

## HTML Rasm teglari

| Teg        | Tavsif                                          |
| ---------- | ----------------------------------------------- |
| \<img>     | Rasmni joylashtirish                            |
| \<map>     | Rasm xaritasini ifodalash                       |
| \<area>    | Rasm xaritasidagi bosiluvchi maydonni belgilash |
| \<picture> | Resurslarda bir nechta rasmlarni joylashtirish  |
