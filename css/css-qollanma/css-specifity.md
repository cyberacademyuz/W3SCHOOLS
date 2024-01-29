# CSS Specifity

### O'ziga xoslik nima ? <a href="#oziga-xoslik-nima" id="oziga-xoslik-nima"></a>

Agar bir xil elementga still beruvchi ikki yoki undan ortiq CSS qoidalari mavjud bo'lsa, o'ziga xoslik qiymati katta bo'lgan selektor "ustunlik" qiladi va uning still deklaratsiyasi ushbu HTML elementiga qo'llaniladi.

O'ziga xoslikni, qaysi stillar to'plami elementga qo'llanilishini aniqlaydigan darajali ko'rsatkich sifatida tasavvur qiling.

Quyidagi misollarni ko'rib chiqing:

#### 1-Misol <a href="#id-1-misol" id="id-1-misol"></a>

```
<html>
<head>
  <style>
    p {color: red;}
  </style>
</head>
<body>

<p>Hello World!</p>

</body>
</html>
```

#### 2-Misol <a href="#id-2-misol" id="id-2-misol"></a>

```
<html>
<head>
  <style>
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p class="test">Hello World!</p>

</body>
</html>
```

Ana endi 3-misolga qarang

#### 3-misol <a href="#id-3-misol" id="id-3-misol"></a>

```
<html>
<head>
  <style>
    #demo {color: blue;}
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p id="demo" class="test">Hello World!</p>

</body>
</html>
```

Ana endi 4-misolga qarang:

```
<html>
<head>
  <style>
    #demo {color: blue;}
    .test {color: green;}
    p {color: red;}
  </style>
</head>
<body>

<p id="demo" class="test" style="color: pink;">Hello World!</p>

</body>
</html>
```

### O'ziga xoslik ierarxiyasi <a href="#oziga-xoslik-ierarxiyasi" id="oziga-xoslik-ierarxiyasi"></a>

Har bir CSS selektorining o'ziga xoslik ierarxiyasi mavjud.

Selektorning o'ziga xoslik darajasini belgilaydigan to'rtta toifa mavjud:

1. **Inline style** (HTML element ichida stil berish) - Masalan: `<h1 style="color: pink;">`
2. **ID lar** - Masalan: #navbar
3. **Classelar, pseudo-classelar, attribute selektorlari** -Masalan: .test, :hover, \[href]
4. **Elementlar va psevdo-elementlar** - Masalan :h1 va ::before

### O'ziga xoslikni qanday xisoblash mumkin ? <a href="#qanday-qilib-oziga-xoslikni-xisoblash-mumkin" id="qanday-qilib-oziga-xoslikni-xisoblash-mumkin"></a>

O'ziga xoslikni qanday xisoblash keraklifini yaxshilab eslab qoling!

0 dan boshlab, har bir identifikator qiymati uchun 100 qo'shiladi, har bir class qiymati uchun 10 qo'shiladi (yoki pseudo-class yoki atribut selektori), har bir element selektori yoki pseudo-element uchun 1 qo'shiladi. Qisqasi, har bir ID qiymati 100, klass va psevdo-klasslar 10, element va psevdo elementlar 1 qiymatiga ega.

{% hint style="warning" %}
**1 - eslatma:** Inline style lar to'g'ridan to'gri 1000 ball oladi va har doim yuqori ierarxiyaga ega!

**2 - esalatma:** Lekin bitta istisno holati bor, agar CSS fayldagi stilda `!important` ishlatilgan bo'lsa u inline style lardan ustun turadi.
{% endhint %}

Quyidagi jadvalda o'ziga xoslikni qanday hisoblash kerakligini keltiramiz:

| Selector                  | O'ziga xoslik qiymati | Hisoblash                                     |
| ------------------------- | --------------------- | --------------------------------------------- |
| p                         | 1                     | 1                                             |
| p.test                    | 11                    | 1 + 10                                        |
| p#demo                    | 101                   | 1 + 100                                       |
| \<p style="color: pink;"> | 1000                  | 1000                                          |
| #demo                     | 100                   | 100                                           |
| .test                     | 10                    | 10                                            |
| p.test1.test2             | 21                    | 1 + 10 + 10                                   |
| #navbar p#demo            | 201                   | 100 + 1 + 100                                 |
| \*                        | 0                     | 0 (universal selektor e'tiborsiz qoldiriladi) |

Katta qiymatga ega selektor boshqasidan ustun bo'ladi va elementga o'z ta'sirini o'tkazadi!

Quyidagi 3 ta kod fragmentiga e'tibor qaratsangiz

```
A: h1
B: h1#content
C: <h1 id="content" style="color: pink;">Heading</h1>
```

A o'ziga xosligi 1 ga teng (chunki u elementni belgilayapti)\
B ning o'ziga xosligi 101 ga teng (chunki u ham element ham ID ni belgilayapti)\
C ning o'ziga xosligi 1000 ga teng (chunki u inline style)

Uchinchi o'ziga xoslikning stili elementga ta'sir o'tkazadi, chunki uning qiymati katta.

### O'ziga xoslik bo'yicha ko'proq misollar <a href="#oziga-xoslik-boyicha-koproq-misollar" id="oziga-xoslik-boyicha-koproq-misollar"></a>

**Teng qiymatli o'ziga xoslik**: oxirgi yozilgan qoida g'alaba qozonadi - Agar CSS faylda bir xil css qoidlari ikki marta yozilsa, oxirgisi qabul qilinadi:

```
h1 {background-color: yellow;}
h1 {background-color: red;}
```

ID selektorlarining o'ziga xosliligi attribut selektorlardan ustunroq - quyidagi kodga qarang:

```
div#a {background-color: green;}
#a {background-color: yellow;}
div[id=a] {background-color: blue;}
```

birinchi qoida qolgan ikki qoidaga nisbatan ko'proq o'ziga xoslikka ega sababi u element nomi va ID bilan birga yozilgan

Kontekstli selektorlar bitta elementli selektorga qaraganda ustunroq - berilgan css kod still beriladigan elementga yaqinroq. Shunday qilib, quyidagi vaziyatda

```
From external CSS file:
#content h1 {background-color: red;}

In HTML file:
<style>
#content h1 {background-color: yellow;}
</style>
```

oxirgi qoida qo'llaniladi.

Class selektorlari har qanday element selektoridan ustunroq: `.intro` kabi class selektori **h1**, **p**, **div** va hokazolardan ustun:

```
.intro {background-color: yellow;}
h1 {background-color: red;}
```

Universal selektor (\*_) va uning meros qilib olingan qiymatlari 0 ga teng - universal selektor (\*_) va meros qilib olingan qiymatlari e'tiborga olinmaydi!
