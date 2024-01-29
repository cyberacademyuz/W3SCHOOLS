---
description: >-
  Har bir HTML elementi o'zining element turiga qarab standart display qiymatiga
  ega bo'ladi. HTMLda 2 turdagi display element bor: block va inline
---

# Block & Inline

## Block elementlar

Block elementlar har doim yangi qatardan boshlanadi va brauzerlar avtomatik tarzda  elementning boshi va ohirini bo'sh joy bilan to'ldiradi.

Block elementlar har doim mavjud bo'lgan to'liq joyni egallab oladi. (iloji boricha chapga va o'ngga cho'ziladi)

Keng tarqalgan 2-ta blok elementlari: `<p>` va `<div>`

`<p>` elementi HTML sahifada paragrafni ifodalaydi.

`<div>` elementi esa HTML fayldagi bo'limni ifodalaydi.

<figure><img src="../../.gitbook/assets/image (58).png" alt=""><figcaption></figcaption></figure>

```
<p>Hello World</p>
<div>Hello World</div> 
```

Quyidagilar HTMLdagi block elementlar hisoblanadi:

```
<address>    <article>    <aside>      <blockquote>    <canvas>    <dd>        <div>
<dl>         <dt>         <fieldset>   <figcaption>    <figure>    <footer>    <form>
<h1>-<h6>    <header>     <hr>         <li>            <main>      <nav>       <noscript>
<ol>         <p>          <pre>        <section>       <table>     <tfoot>     <ul>
<video>
```

## Inline elementar

Inline elementlar yangi qatordan boshlanmaydi.

Inline element faqat kerakli miqdordagi joyni egallaydi.

![](<../../.gitbook/assets/image (9).png>)

```
<span>Hello World</span> 
```

Quyidagilar HTMLdagi inline elementlar hisoblanadi:

```
<a>        <abbr>        <acronym>    <b>        <bdo>    <big>    <br>       <button>
<cite>     <code>        <dfn>        <em>       <i>      <img>    <input>    <kbd>
<label>    <map>         <object>     <output>   <q>      <samp>   <script>   <select>
<small>    <span>        <strong>     <sub>      <sup>    <time>   <tt>       <var>
<textarea>
```

{% hint style="warning" %}
**Eslatma**: Inline element blok elementni o'z ichiga olmaydi!
{% endhint %}

## \<div> elementi

`<div>` elementi ko'pincha boshqa HTML elementlar uchun konteyner sifatida ishlatiladi.

`<div>` elementida kiritilishi talab qilinadigan attributlar yo'q ammo `style`, `class` va `id` attributlari umumiy atributlar hisoblanadi.

CSS bilan ishlatilganda, `<div>` elementidan kontent bloklariga stil berish uchun foydalanish mumkin:

```
<div style="background-color:black;color:white;padding:20px;">
  <h2>London</h2>
  <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
</div> 
```

## \<span> elementi

`<span>` elementi matnning yoki kodlarning bir qismini o'rab olish uchun ishlatiladigan ichki konteynerdir.

`<span>` elementi talab qiladian ma'lum bir atributlar yo'q ammo `style`, `class` va `id` umumiy atribut hisoblanadi.

CSS bilan ishlatilganda, `<span>` elementi matnning bir qismiga stil berish uchun ishlatilishi mumkin:

```
<p>My mother has <span style="color:blue;font-weight:bold;">blue</span> eyes and my
father has <span style="color:darkolivegreen;font-weight:bold;">dark green</span> eyes.
</p>
```

## Bo'lim xulosasi

* HTMLda 2 turdagi display element bor: **block** va **inline**
* Block elementlar har doim yangi qatordan boshlanadi va mavjud bo'lgan to'liq joyni egallab oladi
* Inline elementlar yangi qatordan boshlanmaydi va faqatgina o'ziga kerakli joyni egallaydi
* `<div>` elementi block element hisoblanadi va boshqa HTML elementlar uchun kontener sifatida ishlatiladi
* `<span>` elementi inline element hisoblanadi va matn yoki ma'lumotlarning bir qismini o'rab olish uchun ishlatiladi

## HTML teglar

| Teg     | Ta'rif                                                |
| ------- | ----------------------------------------------------- |
| \<div>  | Kodlarning bir bo'lagini o'rab oladi (blok element)   |
| \<span> | Kodlarning bir bo'lagini o'rab oladi (inline element) |
