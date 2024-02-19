---
description: Semantik elementlar = ma'noga ega elementlar.
---

# Semantikalar

## <mark style="color:green;">Semantik elementlar nima ?</mark>

Semantik element brauzer va dasturchi uchun element mazmunini aniq tasvirlab beradi.

**Semantik bo'lmagan** elementlarga misollar : <mark style="color:red;">`<div>`</mark> va <mark style="color:red;">`<span>`</mark>- Bular nimalarni o'z ichiga olishi haqida avvaldan hech narsa deb bo'lmaydi.

**Semantik** elementlarga misollar : <mark style="color:red;">`<form>`</mark>, <mark style="color:red;">`<table>`</mark>, va <mark style="color:red;">`<article>`</mark>- Bular nimalarni o'z ichiga olishi, element nomidan bilinib turadi.

## <mark style="color:green;">HTMLdagi semantik elementlar</mark>

Ko'pgina saytlarda navigatsiya, sarlavha va footerni ifodalash uchun quyidagi kabi HTML kodlar mavjud: <mark style="color:red;">\<div id="nav"></mark> <mark style="color:red;">\<div class="header"></mark> <mark style="color:red;">\<div id="footer"></mark>.

HTMLda veb-sahifaning turli qismlarini ifodalash uchun ishlatilishi mumkin bo'lgan ba'zi semantik elementlar mavjud:

* \<article>
* \<aside>
* \<details>
* \<figcaption>&#x20;
* \<figure>
* \<footer>
* \<header>
* \<main>
* \<mark>
* \<nav>
* \<section>
* \<summary>
* \<time>

![](<../../.gitbook/assets/image (22).png>)

## <mark style="color:green;">\<section> elementi</mark>

\<section> elementi html fayldagi ma'lum bir bo'limni ifodalaydi.

W3C ning HTML qo'llanmasiga  ko'ra: "Section odatda sarlavhali kontentning tematik guruhlanishidir."

<mark style="color:red;">\<srction></mark> elementini qayerlarda ishlatish mumkinligiga misollar:

* Bo'limlar
* Tanishtiruv qismlar
* Yangiliklarda
* Kontakt ma'lumotlarda

Veb-sahifa odatda tanishtiruv, kontent va kontakt ma'lumotlari uchun bo'limlarga bo'linishi mumkin.

{% code title="HTMLdagi 2ta bo'lim" %}
```html
<section>
<h1>WWF</h1>
<p>The World Wide Fund for Nature (WWF) is an international organization working on issues regarding the conservation, research and restoration of the environment, formerly named the World Wildlife Fund. WWF was founded in 1961.</p>
</section>

<section>
<h1>WWF's Panda symbol</h1>
<p>The Panda has become the symbol of WWF. The well-known panda logo of WWF originated from a panda named Chi Chi that was transferred from the Beijing Zoo to the London Zoo in the same year of the establishment of WWF.</p>
</section> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_section" %}

## <mark style="color:green;">\<article> elementi</mark>

<mark style="color:red;">`<article>`</mark> elementi mustaqil kontentni ifodalaydi.

Article o'zining ma'zmuniga ega bo'lishi kerak va uni veb-saytning qolgan qismidan mustaqil ravishda ajratish imkoniyati bo'lishi kerak.

<mark style="color:red;">`<article>`</mark> elementini qayerda ishlatish mumkinligiga misollar:

* Forum xabarlarida
* Blog postlarda
* Foydalanuvchining izholarida
* Mahsulot uchun kartochkalarda
* Gazeta maqolalarida

{% code title="Mustaqil kontentga ega uchta maqola:" %}
```html
<article>
<h2>Google Chrome</h2>
<p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
</article>

<article>
<h2>Mozilla Firefox</h2>
<p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.</p>
</article>

<article>
<h2>Microsoft Edge</h2>
<p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.</p>
</article> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_article" %}

### Ikkinchi misol

{% code title="<article> elementiga stil berish uchun CSSdan foydalaning" %}
```html
<html>
<head>
<style>
.all-browsers {
  margin: 0;
  padding: 5px;
  background-color: lightgray;
}

.all-browsers > h1, .browser {
  margin: 10px;
  padding: 5px;
}

.browser {
  background: white;
}

.browser > h2, p {
  margin: 4px;
  font-size: 90%;
}
</style>
</head>
<body>

<article class="all-browsers">
  <h1>Most Popular Browsers</h1>
  <article class="browser">
    <h2>Google Chrome</h2>
    <p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
  </article>
  <article class="browser">
    <h2>Mozilla Firefox</h2>
    <p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January, 2018.</p>
  </article>
  <article class="browser">
    <h2>Microsoft Edge</h2>
    <p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. Microsoft Edge replaced Internet Explorer.</p>
  </article>
</article>

</body>
</html> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_article2" %}

<mark style="color:red;">`<article>`</mark> elementini <mark style="color:red;">`<section>`</mark> ichiga joylashtirasizmi yoki aksimi ?

Ushbu elementlarni qanday joylashtirish kerakligiga qaror qabul qilish uchun biror bir ta'rifdan foydalana olamizmi ? Albatta yo'q.

Shunday ekan, siz <mark style="color:red;">`<section>`</mark> elementlarni o'z ichiga olgan <mark style="color:red;">`<article>`</mark> elementlarini va <mark style="color:red;">`<article>`</mark> elementlarni o'z ichiga olgan <mark style="color:red;">`<section>`</mark> elementlariga ega HTML sahifalarni topishingiz mumkin.

## <mark style="color:green;">\<header> elementi</mark>

<mark style="color:red;">`<header>`</mark> elementi tanishtiruv ma'lumotlari yoki navigatsiya havolalari uchun konteyner hisoblanadi.

<mark style="color:red;">`<header>`</mark> elementi odatda quyidagilarni o'z ichiga oladi:

* bir yoki bir nechta sarlavha elementlari (\<h1> - \<h6>)
* logotip yoki ikonka
* mualliflik ma'lumotlari

Eslatma: Bitta HTMLda bir nechta `<header>` elementlari bo'lishi mumkin. Lekin  <mark style="color:red;">\<header></mark> elementi <mark style="color:red;">`<footer>`</mark>, <mark style="color:red;">`<address>`</mark> yoki boshqa <mark style="color:red;">`<header>`</mark> elementi ichiga joylashtirilmaydi.

{% code title="<article> uchun header" %}
```html
<article>
  <header>
    <h1>What Does WWF Do?</h1>
    <p>WWF's mission:</p>
  </header>
  <p>WWF's mission is to stop the degradation of our planet's natural environment,
  and build a future in which humans live in harmony with nature.</p>
</article> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_header" %}

## <mark style="color:green;">\<footer> elementi</mark>

<mark style="color:red;">`<footer>`</mark> elementi sahifa yoki bo'lim uchun uning pastki qismini ifodalaydi.

<mark style="color:red;">`<footer>`</mark> elementi odatda quyidagilarni o'z ichiga oladi:

* mualliflik ma'lumotlari
* mualliflik huquqi haqida ma'lumot
* kontakt ma'lumotlari
* sayt xaritasi
* yuqoriga qaytish havolasi
* tegishli ma'lumotlar

Bir sahifada bir nechta <mark style="color:red;">`<footer>`</mark> elementlaridan foydalanishingiz mumkin.

{% code title="Sahifaning footer bo'limi" %}
```html
<footer>
  <p>Author: Hege Refsnes</p>
  <p><a href="mailto:hege@example.com">hege@example.com</a></p>
</footer> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_footer" %}

## <mark style="color:green;">\<nav> elementi</mark>

<mark style="color:red;">\<nav></mark> elementi navigatsiya havolalarini ifodalaydi.

{% hint style="warning" %}
Eslab qoling, sahifadagi barcha havolalar<mark style="color:red;">`<nav>`</mark>elementining ichida bo'lishi kerak emas. <mark style="color:red;">`<nav>`</mark> elementi faqat navigatsiya havolalarining asosiy bloklari uchun mo'ljallangan.

Brauzerlar nogiron foydalanuvchilar uchun ekranni o'qish vositasi sifatida ushbu bo'limni o'tkazib yubormaslik kerakligini aniqlash uchun ushbu tegdan foydalanishi mumkin.
{% endhint %}

{% code title="Navigatsiya havolalari" %}
```html
<nav>
  <a href="/html/">HTML</a> |
  <a href="/css/">CSS</a> |
  <a href="/js/">JavaScript</a> |
  <a href="/jquery/">jQuery</a>
</nav> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_nav" %}

## <mark style="color:green;">\<aside> elementi</mark>

<mark style="color:red;">`<aside>`</mark> elementi o'zi joylashtirilgan kontentdan tashqari ba'zi tarkibiy qismni ifodalaydi (masalan, yon panelni).

<mark style="color:red;">`<aside>`</mark> kontenti, boshqa bo'lim kontentlari bilan bilvosita bog'liq bo'lishi kerak.

{% code title="Ba'zi ma'lumotlarni u joylashgan ma'lumotlardan tashqarida ko'rsatish:" %}
```html
<p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>

<aside>
<h4>Epcot Center</h4>
<p>Epcot is a theme park at Walt Disney World Resort featuring exciting attractions, international pavilions, award-winning fireworks and seasonal special events.</p>
</aside> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_aside" %}

{% code title="<aside> elementiga stil berish uchun CSSdan foydalaning" %}
```html
<html>
<head>
<style>
aside {
  width: 30%;
  padding-left: 15px;
  margin-left: 15px;
  float: right;
  font-style: italic;
  background-color: lightgray;
}
</style>
</head>
<body>

<p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>

<aside>
<p>The Epcot center is a theme park at Walt Disney World Resort featuring exciting attractions, international pavilions, award-winning fireworks and seasonal special events.</p>
</aside>

<p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>
<p>My family and I visited The Epcot center this summer. The weather was nice, and Epcot was amazing! I had a great summer together with my family!</p>

</body>
</html> 
```
{% endcode %}

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml5_aside2" %}

## <mark style="color:green;">\<figure> va \<figcaption> elementlari</mark>

<mark style="color:red;">`<figure>`</mark> tegi rasmlar, diagrammalar, fotosuratlar, kodlar ro'yxati va shu kabi boshqa mustaqil kontentlarni ifodalaydi.

<mark style="color:red;">`<figcaption>`</mark> tegi <mark style="color:red;">`<figure>`</mark> elementi uchun sarlavha nomini bildiradi. <mark style="color:red;">`<figcaption>`</mark> elementi <mark style="color:red;">`<figure>`</mark> elementining birinchi yoki oxirgi bolasi sifatida joylashtirilishi mumkin.

<mark style="color:red;">`<img>`</mark> elementi haqiqiy rasm/illyustratsiyani ifodalaydi.

```html
<figure>
  <img src="pic_trulli.jpg" alt="Trulli">
  <figcaption>Fig1. - Trulli, Puglia, Italy.</figcaption>
</figure> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_figcaption" %}

## <mark style="color:green;">Nega aynan Semantik elementlar ?</mark>

W3C ga ko'ra: "Semantika Internetdagi ma'lumotlarni, dasturlar, korxonalar va kommunitylar aro almashish va qayta foydalanish imkonini beradi."

## <mark style="color:green;">HTMLdagi semantik elementlar</mark>

Quyidagi ro'yhatda HTMLning ba'zi semantik elementlari keltirilgan:

| Tag                                                                 | Description                                                                                 |
| ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------- |
| [\<article>](https://www.w3schools.com/tags/tag\_article.asp)       | Defines independent, self-contained content                                                 |
| [\<aside>](https://www.w3schools.com/tags/tag\_aside.asp)           | Defines content aside from the page content                                                 |
| [\<details>](https://www.w3schools.com/tags/tag\_details.asp)       | Defines additional details that the user can view or hide                                   |
| [\<figcaption>](https://www.w3schools.com/tags/tag\_figcaption.asp) | Defines a caption for a \<figure> element                                                   |
| [\<figure>](https://www.w3schools.com/tags/tag\_figure.asp)         | Specifies self-contained content, like illustrations, diagrams, photos, code listings, etc. |
| [\<footer>](https://www.w3schools.com/tags/tag\_footer.asp)         | Defines a footer for a document or section                                                  |
| [\<header>](https://www.w3schools.com/tags/tag\_header.asp)         | Specifies a header for a document or section                                                |
| [\<main>](https://www.w3schools.com/tags/tag\_main.asp)             | Specifies the main content of a document                                                    |
| [\<mark>](https://www.w3schools.com/tags/tag\_mark.asp)             | Defines marked/highlighted text                                                             |
| [\<nav>](https://www.w3schools.com/tags/tag\_nav.asp)               | Defines navigation links                                                                    |
| [\<section>](https://www.w3schools.com/tags/tag\_section.asp)       | Defines a section in a document                                                             |
| [\<summary>](https://www.w3schools.com/tags/tag\_summary.asp)       | Defines a visible heading for a \<details> element                                          |
| [\<time>](https://www.w3schools.com/tags/tag\_time.asp)             | Defines a date/time                                                                         |
