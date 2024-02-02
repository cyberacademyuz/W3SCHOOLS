---
<<<<<<< HEAD
description: HTML atributlari HTML elementlari (teglar)ga qo'shimcha ma'lumot beradi.
=======
description: HTML atributlari HTML elementlari (teglar) haqida qo'shimcha ma'lumot beradi.
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f
---

# Atributlar

### <mark style="color:green;">HTML atributlari</mark>

* Barcha HTML elementlar atributlarga ega bo'lishi mumkin.
* Atributlar elementlar haqida qo'shimcha ma'lumot beradi.
* Atributlar har doim ochiluvchi teg ichida yoziladi.
* Atributlar odatda atributning nomi va qiymati ko'rinishida keladi: `name="value"`.

## <mark style="color:green;">href atributi</mark>

<mark style="color:red;">`<a>`</mark> tegi havolani ifodalaydi. <mark style="color:red;">`href`</mark> atributi havola boradigan sahifaning URL manzilni o'z ichiga oladi.

```html
<a href="https://www.w3schools.com">Visit W3Schools</a>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_link" %}

Bizning <mark style="color:green;">HTML Havolalar</mark> bo'limimizda havolalar haqida ko'proq ma'lumotga ega bo'lasiz.

## <mark style="color:green;">src atributi</mark>

<<<<<<< HEAD
<mark style="color:red;">`<img>`</mark> tegi HTML sahifaga rasmn joylashtirish uchun ishlatiladi. `src` atributi esa rasm ko'rsatilishi uchun uning uning  joylashuvini o'z ichiga oladi.
=======
<mark style="color:red;">`<img>`</mark> tegi rasmni HTML sahifaga joylashtirish uchun ishlatiladi. `src` atributi esa rasmning joylashuvini belgilaydi.
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f

```html
<img src="img_girl.jpg">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_img_src" %}

Atributda URL manzilini ko'rsatishning 2 xil yo'li bor:

_**1. To'liq URL**_ - boshqa web-saytda joylashgan rasmning havolasi. Misol: `src="https://www.w3schools.com/images/img_girl.jpg"`

_**Eslatma**_: Boshqa web-saytdagi rasmlar mualliflik huquqi asosida himoyalangan bo'lishi mumkin. Agar undan foydalanish uchun muallifdan ruxsat olmagan bo'lsangiz, mualliflik huquqi to'g'risidagi qonunlarni buzgan bo'lishingiz mumkin.

<<<<<<< HEAD
_**2. Nisbiy URL**_ - veb-sayt ichidagi rasm uchun havolalar. Bunda URL ichida domen nomi yozilmaydi. Agar URL qiyshiq chiziqsiz ( / ) boshlansa, rasm aynan shu sahifada joylashganini bildiradi. Misol: `src="img_girl.jpg"`. Agar URL qiyshiq chiziq bilan boshlansa, rasm biror bir papka ichida ekanligini bildiradi Misol: `src="/images/img_girl.jpg"`.
=======
_**2. Nisbiy URL**_ - veb-saytning ichidagi rasm uchun havolalar. Bunda URL ichida domen nomi yozilmaydi. Agar URL qiyshiq chiziqsiz ( / ) boshlansa, rasm aynan shu sahifada joylashganini bildiradi. Misol: `src="img_girl.jpg"`. Agar URL qiyshiq chiziq bilan boshlansa, rasm biror bir papka ichida ekanligini bildiradi Misol: `src="/images/img_girl.jpg"`.
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f

_**Maslahat**_: Deyarli har doim nisbiy URL manzillaridan foydalanish samarali usul hisoblanadi.

## <mark style="color:green;">Width va height atributlari</mark>

<<<<<<< HEAD
Shuningdek, `<img>` tegida rasmning bo'yi va enini piksellarda belgilaydigan `width` va `height` atributlari ham mavjud.
=======
Shuningdek, <mark style="color:red;">`<img>`</mark> tegida rasmning balandligi va kengligini piksellarda belgilaydigan `width` va `height` atributlari ham mavjud.
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f

```html
<img src="img_girl.jpg" width="500" height="600">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_img" %}

### <mark style="color:green;">Alt atributi</mark>

<<<<<<< HEAD
&#x20;<mark style="color:red;">`<img>`</mark> tegida ta'lab qilinadigan <mark style="color:red;">`alt`</mark> atributi rasm biror sababga ko'ra ko'rinmay qolsa, rasmning o'rniga unga berilgan matnni ko'rsatadi. Rasm ko'rinmay qolishining sababi internetning sekinligi yoki <mark style="color:red;">`src`</mark> atributidagi xatolik yoki screen readerdan foydalanilganligi bo'lishi mumkin.
=======
&#x20;<mark style="color:red;">`<img>`</mark> tegining <mark style="color:red;">`alt`</mark> atributi rasm biror sababga ko'ra ko'rinmay qolsa, rasmning o'rniga unga berilgan matnni ko'rsatadi. Rasm ko'rinmay qolishining sababi internetning sekinligi yoki <mark style="color:red;">`src`</mark> atributidagi xatolik yoki screen readerdan foydalanilganligi bo'lishi mumkin.
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f

```html
<img src="img_girl.jpg" alt="Girl with a jacket">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_alt" %}

Agar mavjud bo'lmagan rasmni ko'rsatishga harakat qilsak, nima bo'lishini ko'ring:

```html
<img src="img_typo.jpg" alt="Girl with a jacket">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_alt_error" %}

Bizning <mark style="color:green;">rasmlar bo'limimiz</mark>da rasmlar haqida ko'proq bilib olasiz.

## <mark style="color:green;">Style atributi</mark>

Style atributi elementga rang, shrift, oʻlcham va boshqa ko'plab xususiyatlar berish uchun ishlatiladi.

**Misol uchun:**

```html
<p style="color:red;">This is a red paragraph.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_style" %}

Bizning <mark style="color:green;">Stillar bo'limimizda</mark> ular haqida ko'proq ma'lumot bilib olasiz.

## <mark style="color:green;">Lang atributi</mark>

Veb-sahifa qaysi tilda ekanligini bildirish uchun har doim <mark style="color:red;">`lang`</mark> atributini <mark style="color:red;">`<html>`</mark> tegiga beramiz. Bu qidiruv tizimlari va brauzerlarga yordam berish uchun mo'ljallangan.

Quyidagi misol sayt ingliz tilida ekanligini ifodalaydi:

```html
<!DOCTYPE html>
<html lang="en">
<body>
...
</body>
</html>
```

Mamlakat kodlari <mark style="color:red;">`lang`</mark> atributidagi til kodiga ham qo'shilishi mumkin. shunday qilib birinchi ikkita belgi HTML sahifasining tilini, oxirgi ikkita ikkita belgi esa mamlakatni belgilaydi.

Quyidagi misolda ingliz tili **til** sifatida, AQSH esa **mamlakat** sifatida ko'rsatilgan:

```html
<!DOCTYPE html>
<html lang="en-US">
<body>
...
</body>
</html>
```

<<<<<<< HEAD
Siz barcha til kodlarini <mark style="color:green;">HTMLning til kodlari bo'limi</mark>dan koʻrishingiz mumkin.
=======
Siz barcha til kodlarini <mark style="color:green;">**HTMLning til kodlari bo'limi**</mark>dan koʻrishingiz mumkin.
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f

## <mark style="color:green;">title (sarlavha) atributi</mark>

<mark style="color:red;">`title`</mark> atributi element haqida qo'shimcha ba'zi ma'lumotlarni belgilaydi.

<<<<<<< HEAD
Element ustiga sichqonchani olib borganingizda, o'ng tomonda title atributiga berilgan qo'shimcha ma'lumot ko'rsatiladi:
=======
Element ustiga sichqonchani olib borganingizda,o'ng tomonda <mark style="color:red;">`title`</mark> atributiga berilgan qo'shimcha ma'lumot ko'rsatiladi:
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f

```html
<p title="I'm a tooltip">This is a paragraph.</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_title" %}

### <mark style="color:green;">Tavsiyamiz: har doim kichik harfli atributlardan foydalaning</mark>

HTML standarti atribut nomlarini aynan kichik harfda yozilishini talab qilmaydi.

<<<<<<< HEAD
title atributi (va shu kabi barcha boshqa atributlar ham) **title** yoki **TITLE** kabi katta yoki kichik harflar bilan yozilishi mumkin.
=======
<mark style="color:red;">`title`</mark> atributi (va shu kabi barcha boshqa atributlar ham) **title** yoki **TITLE** kabi katta yoki kichik harflar bilan yozilishi mumkin.
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f

Biroq, W3C ning maslahati atributlarni kichik harfda yozishni tavsiya qiladi va **XHTML** kabi murakkab hujjat turlari kichik harf atributlarini talab qiladi.

W3Schools da biz har doim kichik harfdagi atribut nomlaridan foydalanamiz.

### <mark style="color:green;">Bizning taklif: har doim atribut qiymatlarini qo'shtirnoq (") ichiga oling.</mark>

HTML standarti atribut qiymatlarini aynan qo'shtirnoq ichida bo'lishini talab qilmaydi.

Biroq, W3C atribut qiymatlarini qo'shtirnoq ichida yozishni maslahat beradi va XHTML kabi murakkab hujjat turlari kodirovkalarni talab qiladi.

{% code title="Yaxshi kod:" %}
```html
<a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a>
```
{% endcode %}

{% code title="Yomon kod:" %}
```html
<a href=https://www.w3schools.com/html/>Visit our HTML tutorial</a>
```
{% endcode %}

Ba'zan siz qo'shtirnoqlardan foydalanishingiz shart. Ushbu misolda title atributi to'g'ri ko'rsatilmaydi, chunki unda bo'sh joy bor:

```html
<p title=About W3Schools>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_error" %}

W3Schools da biz har doim atribut qiymatlarini qo'shtirnoqlar ichida yozamiz.

### <mark style="color:green;">Bir tirnoq yoki qo'shtirnoq ?</mark>

<<<<<<< HEAD
HTMLda atribut qiymatlarini qo'shtirnoq ichida yozish eng keng tarqalgan usul, ammo bir tirnoq ham ishlatilishi mumkin.
=======
HTMLda atribut qiymatlarini qo'shtirnoq ichida yozish eng keng tarqalgan usul, ammo bir tirnoqdan ham foydalanish mumkin.
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f

Ba'zi hollarda, atribut qiymatidagi matnning bir qismida qo'shtirnoqdan foydalanilgan bo'lsa, umumiy atribut qiymayini birtirnoq ichida yozish kerak:

```html
<p title='John "ShotGun" Nelson'>
```

yoki aksincha

```html
<p title="John 'ShotGun' Nelson">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_attributes_single_double" %}

## <mark style="color:green;">Xulosa</mark>

* Barcha HTML elementlari atributlarga ega bo'lishi mumkin;&#x20;
* <mark style="color:red;">`<a>`</mark> tegining <mark style="color:red;">`href`</mark> atributi havola boradigan sahifaning URL manzilini belgilaydi; &#x20;
<<<<<<< HEAD
* <mark style="color:red;">`<img>`</mark> tegining <mark style="color:red;">`src`</mark> atributi ko'rsatiladigan rasmning joylashuvini belgilaydi; &#x20;
=======
* <mark style="color:red;">`<img>`</mark> tegining <mark style="color:red;">`src`</mark> atributi ko'rsatiladigan rasmning joylashuv manzilini belgilaydi; &#x20;
>>>>>>> c4ab4e2d3590bf1e3edb3e1adf84ce13ce15096f
* <mark style="color:red;">`<img>`</mark> tegining <mark style="color:red;">`width`</mark> va <mark style="color:red;">`height`</mark> atributlari rasmlarning o'lchami belgilaydi;&#x20;
* &#x20;<mark style="color:red;">`<img>`</mark> tegining alt atributi rasm ko'rinmay qolsa, uning o'rniga kiritilgan matnni taqdim etadi;&#x20;
* <mark style="color:red;">`style`</mark> atributi rang, shrift, o'lcham va boshqa shu kabi elementga qo'shimcha xususiyat berish uchun ishlatiladi;
* <mark style="color:red;">`<html>`</mark> tegining <mark style="color:red;">`lang`</mark> atributi websahifa tilini ifodalaydi;&#x20;
* <mark style="color:red;">`title`</mark> atributi element haqida ba'zi qo'shimcha ma'lumotlarni belgilaydi.

## <mark style="color:green;">HTML mashqlari</mark>

{% embed url="https://www.w3schools.com/html/exercise.asp?filename=exercise_html_attributes1" %}

## <mark style="color:green;">HTML atributiga tavsiya</mark>

{% embed url="https://www.w3schools.com/tags/ref_attributes.asp" %}