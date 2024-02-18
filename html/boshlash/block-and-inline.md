---
description: >-
  Har bir HTML elementi o'zining element turiga qarab standart display qiymatiga
  ega bo'ladi. HTMLda 2 turdagi display element bor: block va inline
---

# Block & Inline

## <mark style="color:green;">Block elementlar</mark>

Block elementlar har doim yangi qatardan boshlanadi va brauzerlar avtomatik tarzda  elementning boshi va ohirini bo'sh joy bilan to'ldiradi.

Block elementlar har doim mavjud bo'lgan to'liq joyni egallab oladi. (iloji boricha chapga va o'ngga cho'ziladi)

Keng tarqalgan 2-ta blok elementlari: <mark style="color:red;">`<p>`</mark> va <mark style="color:red;">`<div>`</mark>

<mark style="color:red;">`<p>`</mark> elementi HTML sahifada paragrafni ifodalaydi.

<mark style="color:red;">`<div>`</mark> elementi HTMLdagi bo'lim yoki qismni ifdalaydi.

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

```html
<p>Hello World</p>
<div>Hello World</div> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_block_div" %}

Quyidagilar HTMLdagi block elementlar hisoblanadi:

```html
<address>    <article>    <aside>      <blockquote>    <canvas>    <dd>        <div>
<dl>         <dt>         <fieldset>   <figcaption>    <figure>    <footer>    <form>
<h1>-<h6>    <header>     <hr>         <li>            <main>      <nav>       <noscript>
<ol>         <p>          <pre>        <section>       <table>     <tfoot>     <ul>
<video>
```

## <mark style="color:green;">Inline elementar</mark>

Inline elementlar yangi qatordan boshlanmaydi.

Inline element faqat kerakli miqdordagi joyni egallaydi.

![](<../../.gitbook/assets/image (9) (1).png>)

```html
<span>Hello World</span> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_inline_span" %}

Quyidagilar HTMLdagi inline elementlar hisoblanadi:

```html
<a>        <abbr>        <acronym>    <b>        <bdo>    <big>    <br>       <button>
<cite>     <code>        <dfn>        <em>       <i>      <img>    <input>    <kbd>
<label>    <map>         <object>     <output>   <q>      <samp>   <script>   <select>
<small>    <span>        <strong>     <sub>      <sup>    <time>   <tt>       <var>
<textarea>
```

{% hint style="warning" %}
**Eslatma**: Inline element blok elementni o'z ichiga olmaydi!
{% endhint %}

## <mark style="color:green;">`<div>`</mark> <mark style="color:green;"></mark><mark style="color:green;">elementi</mark>

<mark style="color:red;">`<div>`</mark> elementi ko'pincha boshqa HTML elementlar uchun konteyner sifatida ishlatiladi.

<mark style="color:red;">`<div>`</mark> elementida kiritilishi talab qilinadigan attributlar yo'q ammo <mark style="color:red;">`style`</mark>, <mark style="color:red;">`class`</mark> va <mark style="color:red;">`id`</mark> attributlari umumiy atributlar hisoblanadi.

CSS bilan ishlatilganda, <mark style="color:red;">`<div>`</mark> elementidan kontent bloklariga stil berish uchun foydalanish mumkin:

```html
<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
</div> 
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_div" %}

## <mark style="color:green;">\<span> elementi</mark>

<mark style="color:red;">`<span>`</mark> elementi matnning yoki kodlarning bir qismini o'rab olish uchun ishlatiladigan ichki konteynerdir.

<mark style="color:red;">`<span>`</mark> elementi talab qiladian ma'lum bir atributlar yo'q ammo <mark style="color:red;">`style`</mark>, <mark style="color:red;">`class`</mark> va <mark style="color:red;">`id`</mark> umumiy atribut hisoblanadi.

CSS bilan ishlatilganda, <mark style="color:red;">`<span>`</mark> elementi matnning bir qismiga stil berish uchun ishlatilishi mumkin:

```html
<p>My mother has <span style="color:blue;font-weight:bold;">blue</span> eyes and my
father has <span style="color:darkolivegreen;font-weight:bold;">dark green</span> eyes.
</p>
```

{% embed url="https://www.w3schools.com/html/tryit.asp?filename=tryhtml_span" %}

## <mark style="color:green;">Bo'lim xulosasi</mark>

* HTMLda 2 turdagi display element bor: **block** va **inline**
* Block elementlar har doim yangi qatordan boshlanadi va mavjud bo'lgan to'liq joyni egallab oladi
* Inline elementlar yangi qatordan boshlanmaydi va faqatgina o'ziga kerakli joyni egallaydi
* <mark style="color:red;">`<div>`</mark> elementi block element hisoblanadi va boshqa HTML elementlar uchun kontener sifatida ishlatiladi
* <mark style="color:red;">`<span>`</mark> elementi inline element hisoblanadi va matn yoki ma'lumotlarning bir qismini o'rab olish uchun ishlatiladi

## <mark style="color:green;">HTML teglar</mark>

| Teg     | Ta'rif                                                |
| ------- | ----------------------------------------------------- |
| \<div>  | Kodlarning bir bo'lagini o'rab oladi (blok element)   |
| \<span> | Kodlarning bir bo'lagini o'rab oladi (inline element) |
