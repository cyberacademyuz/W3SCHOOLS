---
description: >-
  HTMLning <head> elementi quyidagi elementlarni o'z ichiga oladi: <title>,
  <style>, <meta>, <link>, <script> va <base>.
---

# Head

## HTMLdagi \<head> element

`<head>` elementi metadatalar uchun konteyner hisoblanib, `<html>` va `<body>` teglari orasida joylashadi.

HTMLdagi metadata bu HTML sahifa haqidagi ma'lumotlardir. Metadatalar ekranda ko'rsatilmaydi.

Metadata odatda websayt nomini, belgilar to'plamini, stillarni, skriptlarni va boshqa meta-ma'lumotlarni o'z ichiga oladi.

## HTMLdagi \<title> elementi

`<title>` elementi veb-sahifaning nomini ifodalaydi. Uning ichida faqat matn bo'lishi kerak va u brazuerning sarlavha qismida yoki sahifaning tabida ko'rsatiladi.

HTML fayllarda `<title>` elementi talab qilinadi!

Sahifa sarlavhasi qidiruv tizimini optimallashtirish (SEO) uchun juda muhim hisoblanadi! Sahifa sarlavhasi qidiruv tizimlarining algoritmlari tomonidan qidiruv natijalarida sahifalarni ro'yxatga olish tartibini aniqlash uchun ishlatiladi.

`<title>` elementi:

* brauzerning toolbaridagi sarlavhani ko'rsatadi
* sahifa brauzerdagi sevimlilar bo'limiga qo'shilganda sahifa uchun nom beradi
* qidiruv tizimlarining natijalarida sahifa sarlavhasini ko'rsatadi

Shunday ekan, sarlavhani iloji boricha aniq va tushunarli qilishga harakat qiling!

Oddiy HTML kod:

```html
<!DOCTYPE html>
<html>
<head>
  <title>A Meaningful Page Title</title>
</head>
<body>

HTML kontenti......

</body>
</html> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_title" %}

## \<style> elementi

\<style> elementi bitta sahifaga tegishli CSS xuxusiyatlarini yozish uchun ishlatiladi.

```html
<style>
  body {background-color: powderblue;}
  h1 {color: red;}
  p {color: blue;}
</style> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_style" %}

## \<link> elementi

`<link>` elementi html fayl bilan tashqi fayl o'rtasini bog'lash uchun ishlatiladi.

`<link>` tegidan eng ko'p CSS fayllarni ulash uchun foydalaniladi.

```html
<link rel="stylesheet" href="mystyle.css">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_link" %}

{% hint style="warning" %}
**Maslahat**: CSS haqida barchasini o'rganish uchun bizning [CSS Qo'llanma](broken-reference) sahifamizga o'ting.
{% endhint %}

## \<meta> elementi

`<meta>` elementi odatda belgilar to'plamini, sahifa ta'rifini, kalit so'zlarni, sahifa muallifini va viewport sozlamalarini kiritish uchun ishlatiladi.

Metadata-lar sahifada ko'rsatilmaydi, lekin brauzerlar (ma'lumotlarni qanday ko'rsatish yoki sahifani qayta yuklash uchun), qidiruv tizimlari (kalit so'zlar uchun) va boshqa veb-xizmatlar tomonidan ishlatiladi.

## Misollar

Ishlatilgan belgilar to'plamini ko'rsatish

```html
<meta charset="UTF-8">
```

Qidiruv tizimlari uchun kalit so'zlar ko'rsatish

```html
<meta name="keywords" content="HTML, CSS, JavaScript">
```

Veb-sahifangiz ta'rifini ko'rsatish

```html
<meta charset="UTF-8">
```

Veb sahifangizning ta'rigini

```html
<meta name="description" content="Free Web tutorials">
```

Sahifa muallifini ko'rsatish

```html
<meta name="author" content="John Doe">
```

Sahifani har 30 soniyada qayta yuklash

```html
<meta http-equiv="refresh" content="30">
```

Veb sahifangiz barcha qurilmalarda to'g'ri ko'rsatilishi uchun viewportni sozlash

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

\<meta> teglariga misol:

```html
<meta charset="UTF-8">
<meta name="description" content="Free Web tutorials">
<meta name="keywords" content="HTML, CSS, JavaScript">
<meta name="author" content="John Doe">
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_meta" %}

## Viewportni sozlash

Viewport veb-sahifaning foydalanuvchiga ko'rinadigan qismidir. Bu qurilmaga qarab farq qiladi - u mobil telefonda kompyuter ekraniga qaraganda kichikroq bo'ladi.

Barcha veb-sahifalaringizga quyidagi \<meta> elementini kiritishingiz kerak:

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

Bu brauzerga sahifa o'lchamlari va masshtabini to'g'rlash bo'yicha ko'rsatmalar beradi.

&#x20;`width=device-width` sahifaning kengligini qurilmaning ekran kengligiga nisbatan to'g'irlaydi (bu qurilmaga qarab o'zgaradi).

Ushbu `initial-scale=1.0` esa sahifa birinchi marta yuklanganida boshlang'ich o'lcham holatini beradi.

_Bu bir sahifaning viewport berilgan va berilmagan holatdagi ko'rinishiga misol:_

&#x20;                              [![](<../../.gitbook/assets/image (210).png>)](https://www.w3schools.com/html/example\_withoutviewport.htm)               [![](<../../.gitbook/assets/image (37).png>)](https://www.w3schools.com/html/example\_withviewport.htm)

{% hint style="warning" %}
**Maslahat**: Agar siz ushbu sahifani telefon yoki planshet orqali koʻrayotgan boʻlsangiz, farqni koʻrish uchun quyidagi rasmlar ustiga bosing.
{% endhint %}

## HTMLning \<script> elementi

HTMLning \<script> tegi client-side scriptlar yozish uchun ishlatiladi.&#x20;

Ushbu misoldagi JavaScript kod id="demo" ga ega HTML elementga "Hello JavaScript!" so'zini yozadi.

```html
<script>
    function myFunction() {
  document.getElementById("demo").innerHTML = "Hello JavaScript!";
}
</script>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_script" %}

## \<base> elementi

`<base>` elementi sahifaga bo'g'liq URLlar uchun asosiy sayt URLini yoki tashqi sayt URLini ifodalaydi.

`<base>` tegida `href` va `target` atributlaridan biri yoki ikklasi ham bo'lishi kerak.

Faylda faqat bitta `<base>` elementi bo'lishi kerak!

<pre class="language-html"><code class="lang-html">&#x3C;head>
<strong>    &#x3C;base href="https://www.w3schools.com/" target="_blank">
</strong>&#x3C;/head>

&#x3C;body>
    &#x3C;img src="images/stickman.gif" width="24" height="39" alt="Stickman">
    &#x3C;a href="tags/tag_base.asp">HTML base Tag&#x3C;/a>
&#x3C;/body>
</code></pre>

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_head_base" %}

## Xulosa

* `<head>` elementi meta ma'lumotlar uchun konteyner hisoblanadi
* `<head>` elementi `<html>` va `<body>` teglarining orasiga joylashtiriladi
* `<title>` elementini yozish talab qilinadi va u sahifaning nomini ifodalaydi
* `<style>` elementidan joriy sahifaning o'ziga xos CSS xususiyatlarini berish uchun foydalaniladi&#x20;
* `<link>`  tashqi CSS fayllarni ulash uchun eng ko'p foydalaniladigan teg
* `<meta>` elementi odatda belgilar to'plami, sahifa ta'rifi, kalit so'zlar, hujjat muallifi va viewport sozlamalari uchun foydalaniladi
* `<scriot>` elementi client-side Javascript kodlar uchun foydalaniladi
* `<base>` elementi sahifaga bo'g'liq URLlar uchun asosiy sayt URLini yoki tashqi sayt URLini ifodalaydi.

### HTML head Elements

| Teg                                                         | Ta'rif                                                                                    |
| ----------------------------------------------------------- | ----------------------------------------------------------------------------------------- |
| [\<head>](https://www.w3schools.com/tags/tag\_head.asp)     | Hujjat haqidagi ma'lumotni ifodalaydi                                                     |
| [\<title>](https://www.w3schools.com/tags/tag\_title.asp)   | Hujjatning nomini ifodalaydi                                                              |
| [\<base>](https://www.w3schools.com/tags/tag\_base.asp)     | Sahifadagi barcha havolalar uchun standart manzil yoki standart tashqi saytni belgilaydi. |
| [\<link>](https://www.w3schools.com/tags/tag\_link.asp)     | HTML hujjat va tashqi manba o'rtasini bir biriga ulaydi                                   |
| [\<meta>](https://www.w3schools.com/tags/tag\_meta.asp)     | HTML hujjat uchun meta ma'lumotlarni ifdalaydi                                            |
| [\<script>](https://www.w3schools.com/tags/tag\_script.asp) | Client-side scriptni ifodalaydi                                                           |
| [\<style>](https://www.w3schools.com/tags/tag\_style.asp)   | Hujjat uchun CSS xususiyatlarini belgilaydi                                               |

{% hint style="warning" %}
HTMLda mavjuda barcha teglar ro'yhatini ko'rish uchun, bizning [HTML Tag Ma'lumotnomasi](../html-reference/) sahifamizga o'ting.
{% endhint %}
