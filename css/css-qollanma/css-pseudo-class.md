# CSS Pseudo-class

### Pseudo-classlar nima ? <a href="#css-psevdo-klasslar-nima" id="css-psevdo-klasslar-nima"></a>

Pseudo-class elementning maxsus holatini bildirish uchun ishlatiladi

Masalan, u quyidagilar uchun ishlatilishi mumkin:

* Foydalanuvchi kursorni element ustiga olib kelganida elementga stil berish
* Kirilgan va kirilmagan havolalarga stil berish
* Element focus bo'lganida stil berish

<figure><img src="../../.gitbook/assets/image (844).png" alt=""><figcaption></figcaption></figure>

### Sintaksis <a href="#sintaksis" id="sintaksis"></a>

Pseudo-classlar sintaksisi:

```
selector:pseudo-class {
  property: value;
}
```

### Havola uchun Pseudo-classlar <a href="#link-uchun-psevdo-klasslar" id="link-uchun-psevdo-klasslar"></a>

Havolalarni turli holatlardagi ko'rinishini o'zgartirish:

```
 /* unvisited link */
a:link {
  color: #FF0000;
}

/* visited link */
a:visited {
  color: #00FF00;
}

/* mouse over link */
a:hover {
  color: #FF00FF;
}

/* selected link */
a:active {
  color: #0000FF;
} 
```

{% hint style="warning" %}
**Note:** `a:hover`  to'g'ri ishlashi uchun  `a:link` va `a:visited` dan keyin kelishi SHART. `a:active` esa `a:hover` dan keyin kelishi SHART. Pseudo-classlarni xohlagancha katta va kichk harflarda yozish mumkin.
{% endhint %}

### Pseudo-classlar va HTML classlari <a href="#psevdo-klasslar-va-html-klasslari" id="psevdo-klasslar-va-html-klasslari"></a>

Pseudo classlar HTML classlar bilan birlashtirilishi mumkin.

Misoldagi havola ustiga kursorni olib borganingizda, u rangni o'zgartiradi:

```
a.highlight:hover {
  color: #ff0000;
}
```

### `<div>` ga hover berish <a href="#div-ga-hover-berish" id="div-ga-hover-berish"></a>

`<div>` elementda `:hover` pseudo classidan foydalanishga misol:

```
div:hover {
  background-color: blue;
}
```

### Oddiy hoverli tooltip <a href="#sodda-hover-orqali-tooltip" id="sodda-hover-orqali-tooltip"></a>

`<div>` elementining ustiga kursorni olib borsangiz `<p>` elementi tooltip ko'rinishida paydo bo'ladi:

<mark style="color:red;">\<p> elementini ko'rish uchun meni hover qil</mark>

<figure><img src="../../.gitbook/assets/image (831).png" alt=""><figcaption></figcaption></figure>

```
p {
  display: none;
  background-color: yellow;
  padding: 20px;
}

div:hover p {
  display: block;
}
```

### CSS - :first-child xususiyati <a href="#css-first-child-xususiyati" id="css-first-child-xususiyati"></a>

`:first-child` pseudo-classi boshqa elementning birinchi bola elementi bo'lgan elementni topadi.

### Birinchi kelgan `<p>` elementni topish <a href="#birinchi-joylashgan-p-elementni-aniqlash" id="birinchi-joylashgan-p-elementni-aniqlash"></a>

Quyidagi misolda, selektor har qanday birinchi bola element bo'lgan `<p>` elementini topadi:

```
p:first-child {
  color: blue;
}
```

### `<p>` elementlar orasida joylashgan barcha `<i>` elementlarni topish <a href="#p-elementlar-orasida-joylashgan-barcha-i-elementlarni-belgilash" id="p-elementlar-orasida-joylashgan-barcha-i-elementlarni-belgilash"></a>

Quyidagi misolda, selektor `<p>` elementlar orasida joylashgan barcha `<i>` elementlarni topadi:

```
p i:first-child {
  color: blue;
}
```

### Barcha `<p>` elementlar ichidagi birinchi childi bo'lgan `<i>` elementlarni topish <a href="#barcha-p-elementlar-ichidagi-birinchi-i-child-larni-aniqlash" id="barcha-p-elementlar-ichidagi-birinchi-i-child-larni-aniqlash"></a>

Quyidagi misoldagi selektor `<p>` elementlarining ichidagi birinchi chil bo'lgan barcha `<i>` elementlarni aniqlaydi

```
p:first-child i {
  color: blue;
}
```

### CSS - `:lang` pseudo-classi <a href="#css-lang-psevdo-klassi" id="css-lang-psevdo-klassi"></a>

`:lang` pseudo-classi turli tillar uchun maxsus qoidalar berish imkonini beradi.

Quyidagi misolda `:lang` pseudo-classi `lang="no"` orqali `<q>` elementlari uchun iqtibos belgilarini qo'yadi:

```
<html>
<head>
<style>
q:lang(no) {
  quotes: "~" "~";
}
</style>
</head>
<body>

<p>Some text <q lang="no">A quote in a paragraph</q> Some text.</p>

</body>
</html> 
```

[<mark style="color:green;">Havolalarga turli stillar qo'shish</mark>](https://www.w3schools.com/css/tryit.asp?filename=trycss\_pc\_links2)\
Ushbu misolda giperhavolalarga boshqacha stillarni qanday qo'shis/hi ko'rsatilgan.&#x20;

[<mark style="color:green;">`:focus`</mark><mark style="color:green;">dan foydalanish</mark>](https://www.w3schools.com/css/tryit.asp?filename=trycss\_link\_focus)\
Ushbu misolda `:focus` pseudo-classidan qanday foydalanish ko'rsatilgan.

### CSSning barcha Pseudo classlari <a href="#barcha-css-psevdo-elementlar" id="barcha-css-psevdo-elementlar"></a>

| Selektor                                                                           | Misol                 | Misol tarifi                                                                                              |
| ---------------------------------------------------------------------------------- | --------------------- | --------------------------------------------------------------------------------------------------------- |
| [:active](https://www.w3schools.com/cssref/sel\_active.asp)                        | a:active              | Aktiv linkni belgilaydi                                                                                   |
| [:checked](https://www.w3schools.com/cssref/sel\_checked.asp)                      | input:checked         | Har bir tekshirilgan inputni belgilaydi                                                                   |
| [:disabled](https://www.w3schools.com/cssref/sel\_disabled.asp)                    | input:disabled        | Barcha o'chirilgan inputlarni belgilaydi                                                                  |
| [:empty](https://www.w3schools.com/cssref/sel\_empty.asp)                          | p:empty               | Barcha childi yo'q \<p> elementlarini belgilaydi                                                          |
| [:enabled](https://www.w3schools.com/cssref/sel\_enabled.asp)                      | input:enabled         | Barcha yoqilgan inputlarni belgilaydi                                                                     |
| [:first-child](https://www.w3schools.com/cssref/sel\_firstchild.asp)               | p:first-child         | \<p> elementning ichidagi birinchi childni belgilaydi                                                     |
| [:first-of-type](https://www.w3schools.com/cssref/sel\_first-of-type.asp)          | p:first-of-type       | Barcha birinchi elementi \<p> bo'lgan elementlarni belgilaydi                                             |
| [:focus](https://www.w3schools.com/cssref/sel\_focus.asp)                          | input:focus           | Focusga ega \<input> ni belgilaydi                                                                        |
| [:hover](https://www.w3schools.com/cssref/sel\_hover.asp)                          | a:hover               | Link ustida kursor paydo bo'lganini belgilaydi                                                            |
| [:in-range](https://www.w3schools.com/cssref/sel\_in-range.asp)                    | input:in-range        | Barcha maxsus range qiymatiga ega \<input> elementlarini belgilaydi                                       |
| [:invalid](https://www.w3schools.com/cssref/sel\_invalid.asp)                      | input:invalid         | Barcha invalid qiymatga ega \<input> elementlarini belgilaydi                                             |
| [:lang(_language_)](https://www.w3schools.com/cssref/sel\_lang.asp)                | p:lang(it)            | Har bir “it” qiymatiga ega lang atributi bor \<p> elemenni belgilaydi                                     |
| [:last-child](https://www.w3schools.com/cssref/sel\_last-child.asp)                | p:last-child          | Har bir \<p> elementining oxirgi childini belgilaydi                                                      |
| [:last-of-type](https://www.w3schools.com/cssref/sel\_last-of-type.asp)            | p:last-of-type        | Har bir oxiri \<p> elementga ega parent \<p> elementlarni belgilaydi                                      |
| [:link](https://www.w3schools.com/cssref/sel\_link.asp)                            | a:link                | Barcha kirilmagan linklarni belgilaydi                                                                    |
| [:not(selector)](https://www.w3schools.com/cssref/sel\_not.asp)                    | :not(p)               | Har bir \<p> element bo’lmagan elementlarni belgilaydi                                                    |
| [:nth-child(n)](https://www.w3schools.com/cssref/sel\_nth-child.asp)               | p:nth-child(2)        | \<p> elementning ikkinchi childini belgilaydi                                                             |
| [:nth-last-child(n)](https://www.w3schools.com/cssref/sel\_nth-last-child.asp)     | p:nth-last-child(2)   | Har bir \<p> elementning ikkinchi childini oxirgi childdan boshlangan hisobda belgilaydi                  |
| [:nth-last-of-type(n)](https://www.w3schools.com/cssref/sel\_nth-last-of-type.asp) | p:nth-last-of-type(2) | Har bir parent \<p> elementning oxirgi childdan hisoblangandagi ikkinchi childi \<p> bo’lganni belgilaydi |
| [:nth-of-type(n)](https://www.w3schools.com/cssref/sel\_nth-of-type.asp)           | p:nth-of-type(2)      | Har bir \<p> elementning ikkinchi childi \<p> bo’lganni tanlaydi                                          |
| [:only-of-type](https://www.w3schools.com/cssref/sel\_only-of-type.asp)            | p:only-of-type        | Har bir \<p> elementni faqatgina \<p> bo’lgan parentini belgilaydi                                        |
| [:only-child](https://www.w3schools.com/cssref/sel\_only-child.asp)                | p:only-child          | Har bir parenti uchun bitta child bo’lgan \<p> elementni belgilaydi                                       |
| [:optional](https://www.w3schools.com/cssref/sel\_optional.asp)                    | input:optional        | Barcha no-required qiymatiga ega \<input> elementlarni belgilaydi                                         |
| [:out-of-range](https://www.w3schools.com/cssref/sel\_out-of-range.asp)            | input:out-of-range    | Barcha qiymati ma’lum chegaradan oshib ketgan \<input> elementlarni belgilaydi                            |
| [:read-only](https://www.w3schools.com/cssref/sel\_read-only.asp)                  | input:read-only       | Barcha readonly atributiga ega \<input> elementlarni belgilaydi                                           |
| [:read-write](https://www.w3schools.com/cssref/sel\_read-write.asp)                | input:read-write      | Barcha readonly atributiga ega emas \<input> elementlarni belgilaydi                                      |
| [:required](https://www.w3schools.com/cssref/sel\_required.asp)                    | input:required        | Barcha required atributiga ega \<input> elementlarni belgilaydi                                           |
| [:root](https://www.w3schools.com/cssref/sel\_root.asp)                            | root                  | Butun HTML belgilaydi                                                                                     |
| [:target](https://www.w3schools.com/cssref/sel\_target.asp)                        | #news:target          | Hozirda aktiv bo’lib turgan #news elementni belgilaydi (Bosib turilgan a elementni)                       |
| [:valid](https://www.w3schools.com/cssref/sel\_valid.asp)                          | input:valid           | Barcha to’g’ri keladigan qiymatga ega \<input> elementlarni belgilaydi                                    |
| [:visited](https://www.w3schools.com/cssref/sel\_visited.asp)                      | a:visited             | Barcha kirilgan linklarni belgilaydi                                                                      |

### CSSning barcha Pseudo Elementlar <a href="#barcha-css-psevdo-elementlar" id="barcha-css-psevdo-elementlar"></a>

| Selektor                                                                | Misol           | Misol ta'rifi                                                    |
| ----------------------------------------------------------------------- | --------------- | ---------------------------------------------------------------- |
| [::after](https://www.w3schools.com/cssref/sel\_after.asp)              | p::after        | Har bir \<p> elementning kontentiga keyin narsa qo’shadi         |
| [::before](https://www.w3schools.com/cssref/sel\_before.asp)            | p::before       | Har bir \<p> elementning kontentiga oldin narsa qo’shadi         |
| [::first-letter](https://www.w3schools.com/cssref/sel\_firstletter.asp) | p::first-letter | Har bir \<p> elementning birinchi harfini belgilaydi             |
| [::first-line](https://www.w3schools.com/cssref/sel\_firstline.asp)     | p::first-line   | Har bir \<p> elementning birinchi qatorini belgilaydi            |
| [::marker](https://www.w3schools.com/cssref/sel\_marker.asp)            | ::marker        | List dagi markerlarni belgilaydi                                 |
| [::selection](https://www.w3schools.com/cssref/sel\_selection.asp)      | p::selection    | Elementning foydalanuvchi tomonidan tanlangan qismini belgilaydi |
