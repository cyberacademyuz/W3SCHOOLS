---
description: >-
  Tog'ri, tushunarli va tartibli kod, boshqalarga kodingizni o'qish va
  tushunishni osonlashtiradi. Bu yerda to'g'ri kod yozish bo'yicha ba'zi
  ko'rsatmalar va maslahatlar mavjud.
---

# Stil berish qo'llanmasi

## Har doim hujjat turini e'lon qiling

Har doim HTML faylingizning birinchi qatoridayoq hujjat turini kiriting.

HTML uchun to'g'ri hujjat turi bu:

```
<!DOCTYPE html>
```

## Element nomlarida kichik harflardan foydalaning

HTML element nomlarida katta va kichik harflarni aralashtirib yozilishiga ruhsat beradi.

Ammo biz kichik harflardan foydalanishni maslahat beramiz, chunki:

* Katta va kichik harflar bilan aralashtirib yozilgan element nomlari hunuk ko'rinadi
* Dasturchilar odatda kichik harflardan foydalanishadi
* Kichik harflar yanada tushunarli ko'rinadi
* Kichik harflarda yozish osonroq

{% code title="Yaxshi" %}
```
<body>
<p>This is a paragraph.</p>
</body> 
```
{% endcode %}

{% code title="Yomon" %}
```
<BODY>
<P>This is a paragraph.</P>
</BODY> 
```
{% endcode %}

## Barcha HTML elementlarini yoping

HTMLda barcha elementni ham yopishingiz shart emas (masalan \<p> elementini)

Ammo biz HTML elementlarini quyidagi ko'rinishda yopishingizni qattiq masalahat beramiz:

{% code title="Yaxshi" %}
```
<section>
  <p>This is a paragraph.</p>
  <p>This is a paragraph.</p>
</section>
```
{% endcode %}

{% code title="Yomon" %}
```
<section>
  <p>This is a paragraph.
  <p>This is a paragraph.
</section> 
```
{% endcode %}

## Atribut nomlarida kichik harflardan foydalaning

HTML, attribut nomlarida ham katta va kichik harflarni aralashtirib yozishga ruhsat beradi:

Ammo biz kichik harflardan foydalanishni maslahat beramiz, chunki:

* Katta va kichik harflar bilan aralashtirib yozilgan element nomlari hunuk ko'rinadi
* Dasturchilar odatda kichik harflardan foydalanishadi
* Kichik harflar yanada tushunarli ko'rinadi
* Kichik harflarda yozish osonroq

{% code title="Yaxshi" %}
```
<a href="https://www.w3schools.com/html/">Visit our HTML tutorial</a> 
```
{% endcode %}

{% code title="Yomon" %}
```
<a HREF="https://www.w3schools.com/html/">Visit our HTML tutorial</a> 
```
{% endcode %}

## Har doim atribut qiymatlarini qo'shtirnoqga oling

HTML qo'shtirnoqsiz atribut qiymatlarini ham qabul qiladi.

Ammo biz ularni qo'shtirnoq ichiga olishingizni maslahat beramiz, chunki:

* Dasturchilar odatda atribut qiymatlarini qo'shtirnoqqa olishadi
* Qo'shtirnoqqa olingan qiymatlarni o'qish oson
* Agar qiymatda bo'sh joy bo'lsa qo'shtirnoqdan foydalanishingiz shart

{% code title="Yaxshi" %}
```
<table class="striped"> 
```
{% endcode %}

{% code title="Yomon" %}
```
<table class=striped> 
```
{% endcode %}

{% code title="Juda yomon: bu ishlamaydi chunki qiymatda bo'sh joylar bor" %}
```
<table class=table striped> 
```
{% endcode %}

## Har doim rasmlar uchun alt, width va heightni kiriting

Rasmlar uchun har doim `alt` atributini bering. Agar biron sababga ko'ra rasmni ko'rsatib bo'lmasa, bu atribut muhim ahamiyatga ega hisoblanadi.

Shuningdek, har doim rasmlarning  `width` va `height` o'lchamlarini ham bering. Bu sakrashni oldini oladi, chunki brauzer rasmni yuklashdan oldin u uchun joy ajratadi.

{% code title="Yaxshi" %}
```
<img src="html5.gif" alt="HTML5" style="width:128px;height:128px"> 
```
{% endcode %}

{% code title="Yomon" %}
```
<img src="html5.gif"> 
```
{% endcode %}

## Bo'sh joy va barobar belgisi

HTML barobar belgisi atrofida bo'sh joy tashlashga ruhsat beradi. Ammo bo'sh joylar bilan kodni o'qish biroz noqulay

{% code title="Yaxshi" %}
```
<link rel="stylesheet" href="styles.css"> 
```
{% endcode %}

{% code title="Yomon" %}
```
<link rel = "stylesheet" href = "styles.css"> 
```
{% endcode %}

## Uzun kodli qatorlardan chetlaning

HTML editorlardan foydalangandan, codeni o'qish uchun uni o'ng va chapga surish kodni o'qishga noqulaylik tug'diradi.

Uzun kodli qatorlardan chetlanishga harakat qiling.

## Bo'sh qatorlar va indentatsiya

Bo'sh qatorlar va bo'sh joylarni yoki indentatsiyalarni besabab qo'shmang.

O'qishni osonlashtirish maqsadida katta yoki logikaviy kod bloklarini ajratish uchun bo'sh qatorlar qo'shing.

O'qishni osonlashtirish uchun ikkita bo'sh joy qo'shing. Tab tugmasidan foydalanmang.

{% code title="Yaxshi" %}
```
<body>

<h1>Famous Cities</h1>

<h2>Tokyo</h2>
<p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area, and the most populous metropolitan area in the world.</p>

<h2>London</h2>
<p>London is the capital city of England. It is the most populous city in the United Kingdom.</p>

<h2>Paris</h2>
<p>Paris is the capital of France. The Paris area is one of the largest population centers in Europe.</p>

</body> 
```
{% endcode %}

{% code title="Yomon" %}
```
<body>
<h1>Famous Cities</h1>
<h2>Tokyo</h2><p>Tokyo is the capital of Japan, the center of the Greater Tokyo Area, and the most populous metropolitan area in the world.</p>
<h2>London</h2><p>London is the capital city of England. It is the most populous city in the United Kingdom.</p>
<h2>Paris</h2><p>Paris is the capital of France. The Paris area is one of the largest population centers in Europe.</p>
</body>

```
{% endcode %}

{% code title="Yaxshi jadval kodiga misol" %}
```
 <table>
  <tr>
    <th>Name</th>
    <th>Description</th>
  </tr>
  <tr>
    <td>A</td>
    <td>Description of A</td>
  </tr>
  <tr>
    <td>B</td>
    <td>Description of B</td>
  </tr>
</table> 
```
{% endcode %}

{% code title="Yaxshi ro'yhatga misol:" %}
```
<ul>
  <li>London</li>
  <li>Paris</li>
  <li>Tokyo</li>
</ul> 
```
{% endcode %}

## Hech qachon \<title> elementini unitib qoldirmang

HTML da \<title> elementi talab qilinadi.

Sahifa sarlavhasi qidiruv tizimini optimallashtirish (SEO) uchun juda muhim hisoblanadi! Sahifa sarlavhasi qidiruv tizimlarining algoritmlari tomonidan qidiruv natijalarida sahifalarni ro'yxatga olish tartibini aniqlash uchun ishlatiladi.

\<title> elementi:

* brauzerning toolbaridagi sarlavhani ko'rsatadi
* sahifa brauzerdagi sevimlilar bo'limiga qo'shilganda sahifa uchun nom beradi
* qidiruv tizimlarining natijalarida sahifa sarlavhasini ko'rsatadi

Shunday ekan, sarlavhani iloji boricha aniq va tushunarli qilishga harakat qiling!

```
<title>HTML Style Guide and Coding Conventions</title>
```

## \<html> va \<body> ni yozmasa ham bo'ladimi ?

HTML sahifasi \<html> va \<body> elementlarisiz ham ko'rinadi.

```
<!DOCTYPE html>
<head>
  <title>Page Title</title>
</head>

<h1>This is a heading</h1>
<p>This is a paragraph.</p> 
```

Ammo biz \<html> va \<body> elementlaridan har doim foydalanishni qattiq maslahat beramiz.

\<body> elementini tashlab ketishlik eski brauzerlarda xatoliklarga olib kelishi mumkin.

Qoldirib ketilgan \<html> va \<body> elementlari DOM va XML dasturlarini ishdan chiqarishi mumkin.

## \<head> ni yozmasa bo'ladimi ?

\<head> elementini ham qoldirib ketish mumkin.

Brauzerlar \<body> elementidan oldin standart \<head> elementini qo'shishadi.

```
<!DOCTYPE html>
<html>
<title>Page Title</title>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html> 
```

Ammo biz \<head> elementidan foydalanishni masalahat beramiz.

## To'q elementlar yopiladimi ?

{% code title="Mumkin:" %}
```
<meta charset="utf-8"> 
```
{% endcode %}

{% code title="Bu ham mumkin:" %}
```
<meta charset="utf-8" /> 
```
{% endcode %}

Agar XML va XHTML sahifangizga kiritiladigan bo'lsa, XML va XHTMLda talab qilinganligi sababli, yopilish chizig'i / dan foydalaning.

## Lang atributini qo'shish

Veb-sahifa tilini bildirish uchun har doim `lang` atributini \<html> tegining ichiga kiritishingiz kerak. Bu qidiruv tizimlari va brauzerlarga yordam berish uchun mo'ljallangan.

```
<!DOCTYPE html>
<html lang="en-us">
<head>
  <title>Page Title</title>
</head>
<body>

<h1>This is a heading</h1>
<p>This is a paragraph.</p>

</body>
</html> 
```

## Meta ma'lumotlar

Brauzerlar saytni to'g'ri tushunishi va qidiruv tizimlari sayni to'g'ri indekslashini ta'minlash uchun HTML da saytning tili va belgilarni kodlash `<meta charset="`_`charset`_`">` imkon qadar erta aniqlanishi kerak.

```
<!DOCTYPE html>
<html lang="en-us">
<head>
  <meta charset="UTF-8">
  <title>Page Title</title>
</head>
```

## Viewportni sozlash

Viewport veb-sahifaning foydalanuvchiga ko'rinadigan qismidir. Bu qurilmaga qarab farq qiladi - u mobil telefonda kompyuter ekraniga qaraganda kichikroq bo'ladi.

Barcha veb-sahifalaringizga quyidagi \<meta> elementini kiritishingiz kerak:

```
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

## Komentariyalar

Qisqa izohlar quyidagi kabi bir qatorda yoziladi:

```
<!-- This is a comment -->
```

Bir necha qatoli izohlar quyidagicha yozilishi kerak:

```
<!--
  This is a long comment example. This is a long comment example.
  This is a long comment example. This is a long comment example.
-->
```

## Stillardan foydalanish

Stillarni ulash uchun quyidagidek oddiy sintaksisdan foydalaning ( `type` atributi shart emas):

```
<link rel="stylesheet" href="styles.css">
```

Qisqa CSS kodalarni zichlashtirib yozish mumkin.

```
p.intro {font-family:Verdana;font-size:16em;}
```

Uzun CSS kodlar quyidakidek bir nechta qatorlarda yoziladi:

```
body {
  background-color: lightgrey;
  font-family: "Arial Black", Helvetica, sans-serif;
  font-size: 16em;
  color: black;
}
```

* Ochiluvchi jingalak qavsni selektor nomi bilan bir qatorda yozing
* Ochiluvchi qavsdan oldin bitta bo'sh joy tashlang
* Indentatsiya uchun 2-ta bo'sh joydan foydalaning
* Har bir "xususiyat: qiymat" dan keyin nuqta-vergul ( ; ) qo'ying
* Beiladigan qiymatda bo'sh joylar bo'lsa qo'shtirnoqdan foydalaning
* Yopiluvchi jingalak qavsdan oldin bo'sh joy tashlamasdan yangi qatorda yozing.

## HTMLda Javascriptni yuklash

Tashqi resurslarni ulash uchun oddiy sintaksis (type atributi shart emas):

```
<script src="myscript.js">
```

## Javascript orqali HTML elementlarini olish

HTML kodidan tartibsiz foydalanish JavaScript xatolariga olib kelishi mumkin.

Quyidagi ikkita JavaScript bayonoti turlicha natijalar ko'rsatadi:

```
getElementById("Demo").innerHTML = "Hello";

getElementById("demo").innerHTML = "Hello"; 
```

## Fayl nomlarida kichik harflardan foydalaning

Ba'zi veb-serverlar (Apache, Unix) fayl nomlaridagi harflarning katta-kichikligi e'tibor beradi: "london.jpg" nomli faylni "London.jpg" deb yozib bo'lmaydi.

Boshqa veb-serverlar (Microsoft, IIS) fayl nomlaridagi harflarning katta-kichikligiga e'tibor bermaydi: "london.jpg" nomli faylni "London.jpg" deb yozish mumkin.

Agar fayl nomlarini berishda katta va kichik harflarni aralashtirib foydalansangiz, buni bilishingiz kerak.

Agar fayl nomlaridagi harflarning katta-kichikligiga e'tibor qilmaydigan serverdan harflarning katta-kichikligiga e'tibot beradigan serverga o'tsangiz, kichik kamchiliklar ham saytingizni buzadi!

Bunday muammolarni oldini olish uchun har doim fayl nomlarida kichik harflardan foydalaning!

## Fayl kengaytmalari

HTML fayllari **.html** kengaytmasiga ega bo'lishi kerak ( **.htm** ham bo'lishi mumkin).

CSS fayllari **.css** kengaytmasiga ega bo'lishi kerak.

JavaScript fayllari **.js** kengaytmasiga ega boʻlishi kerak.

## HTM va HTML o'rtasida qanday farq bor ?

.html va .html fayl kengaytmalarining o'rtasida hech qanday farq yo'q.

Ikkalasi ham istalgan veb-brauzer va veb-server tomonidan HTML sifatida qabul qilinadi.

## Standart fayl nomlar

Agar URL oxirida fayl nomini ko'rsatilmasa (masalan, "https://www.w3schools.com/"), server shunchaki "index.html", "index.htm", "default.html", yoki "default.htm" kabi standart fayl nomini qo'shadi.

Agar serveringiz standart fayl nomi sifatida faqat "index.html" bilan tuzilgan bo'lsa, faylingiz nomi "default.html" emas, balki "index.html" deb nomlanishi kerak.

Ammo, serverlar bir nechta standart fayl nomlari bilan sozlanishi mumkin; odatda siz xohlagancha bir nechta standart fayl nomlarini o'rnatishingiz mumkin.

