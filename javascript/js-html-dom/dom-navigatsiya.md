# DOM Navigatsiya

HTML DOM yordamida node shajarasu bo'ylab node munosabatlari yordamida harakat qilishingiz mumkin.

### DOM Nodelar

W3C HTML DOM standartiga ko'ra, HTML hujjatidagi barcha narsa node hisoblanadi:

* Butun hujjat hujjat node-i
* Har bir HTML elementi element node-i
* HTML elementlari ichidagi matn matn node-i
* Har bir HTML atributi atribut node-i (eskirgan)
* Barcha izohlat izoh node-i hisoblanadi

<figure><img src="https://www.w3schools.com/js/pic_htmltree.gif" alt=""><figcaption></figcaption></figure>

HTML DOM yordamida Node shajarasidagi barcha nodelarga JavaScript orqali murojaat qilish mumkin.

Yangi nodelarni yaratish va barcha nodelarni o'zgartirish yoki o'chirish mumkin.

### Node munosabatlari

Node shajarasidagi Nodelar bir-biriga ierarxik munosabatga ega.

Ota-ona, bola va aka-uka atamalari munosabatlarni tasvirlash uchun ishlatiladi.

* Node shajarasida yuqori node **root** (yoki ildiz node) deb ataladi.
* Har bir nodening faqat bitta ota-onasi bor, ildizdan tashqari (uning ota-onasi yo'q)
* Node bir nechta bolalarga ega bo'lishi mumkin
* Siblinglar (aka-ukalar yoki opa-singillar) bir ota-onaga ega bo'lgan nodelardir

```
<html>

  <head>
    <title>DOM Tutorial</title>
  </head>

  <body>
    <h1>DOM Lesson one</h1>
    <p>Hello world!</p>
  </body>

</html>
```

![Tugun daraxti](https://www.w3schools.com/js/pic\_navigate.gif)

Yuqoridagi HTML dan quyidagilarni o'qishingiz mumkin:

* `<html>` ildiz node
* `<html>` ning ota-onasi yo'q
* `<html>` `<head>` va `<body>`ning ota-onasi hisoblanadi
* `<head>` `<html>`ning birinchi farzandi hisoblanadi
* `<body>` `<html>`ing oxirgi farzandi hisoblanadi

va:

* `<head>`ning bitta farzandi bor: `<title>`
* `<title>`ning bitta farzandi bor (matnli node): "DOM Tutorial"
* `<body>`ning ikkita farzandi bor: `<h1>` va `<p>`
* `<h1>`ning bitta bolasi bor: "DOM birinchi dars"
* `<p>`ning bitta farzandi bor: "Salom dunyo!"
* `<h1>` va `<p>` aka-uka

### Nodelar orasida harakatlanish

JavaScript bilan nodelar orasida harakatlanish uchun quyidagi node xususiyatlaridan foydalanishingiz mumkin:

* `parentNode`
* `childNodes[`_`nodenumber`_`]`
* `firstChild`
* `lastChild`
* `nextSibling`
* `previousSibling`

### Child nodelar va node qiymatlari

{% hint style="warning" %}
DOMni qayta ishlashda keng tarqalgan xato - bu element node-ida matn bo'lishini kutish.
{% endhint %}

```
<title id="demo">DOM Tutorial</title>
```

`<title>` element node-ida (yuqoridagi misolda) matn mavjud emas.

U "DOM Tutorial" qiymatiga ega matn node-ini o'z ichiga oladi.

Matn node-ining qiymatiga nodening `innerHTML` xususiyati orqali murojaat qilish mumkin:

```
myTitle = document.getElementById("demo").innerHTML;
```

innerHTML xususiyatiga kirish birinchi bola elementning `nodeValue` siga murojaaq qilish bilan bir xil:

```
myTitle = document.getElementById("demo").firstChild.nodeValue;
```

Birinchi bola elementiga murojaat qilish quyidagi tarzda amalga oshirilishi mumkin:

```
myTitle = document.getElementById("demo").childNodes[0].nodeValue;
```

Quyidagi barcha (3) misollar `<h1>` elementining matnini oladi va uni `<p>` elementiga ko'chiradi:

```
<html>
<body>

<h1 id="id01">My First Page</h1>
<p id="id02"></p>

<script>
document.getElementById("id02").innerHTML = document.getElementById("id01").innerHTML;
</script>

</body>
</html>
```

```
<html>
<body>

<h1 id="id01">My First Page</h1>
<p id="id02"></p>

<script>
document.getElementById("id02").innerHTML = document.getElementById("id01").firstChild.nodeValue;
</script>

</body>
</html>
```

```
<html>
<body>

<h1 id="id01">My First Page</h1>
<p id="id02">Hello!</p>

<script>
document.getElementById("id02").innerHTML = document.getElementById("id01").childNodes[0].nodeValue;
</script>

</body>
</html>
```

### InnerHTML

Ushbu qo'llanmada HTML elementining tarkibini olish uchun `innerHTML` xususiyatidan foydalanamiz.

Biroq, yuqoridagi boshqa usullarni o'rganish shajaraning tuzilishini va DOM navigatsiyasini tushunish uchun foydali hisoblanadi.

### DOM root nodelari

Butun hujjatga murojaat qilish imkonini beruvchi ikkita maxsus xususiyat mavjud:

* `document.body`- Hujjatning asosiy qismi
* `document.documentElement`- Butun hujjat

```
<html>
<body>

<h2>JavaScript HTMLDOM</h2>
<p>Displaying document.body</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = document.body.innerHTML;
</script>

</body>
</html>
```

```
<html>
<body>

<h2>JavaScript HTMLDOM</h2>
<p>Displaying document.documentElement</p>

<p id="demo"></p>

<script>
document.getElementById("demo").innerHTML = document.documentElement.innerHTML;
</script>

</body>
</html>
```

### nodeName xususiyati

`nodeName` xususiyati node nomini belgilaydi.

* nodeName faqat o'qiladi
* element node-ining nodeName-i teg nomi bilan bir xil
* atribut node-ining nodeName-i atribut nomi hisoblanadi
* Matn node-ining nodeName-i har doim #text
* Hujjat node-ining nodeName-i har doim #document hisoblanadi

```
<h1 id="id01">My First Page</h1>
<p id="id02"></p>

<script>
document.getElementById("id02").innerHTML = document.getElementById("id01").nodeName;
</script>
```

{% hint style="warning" %}
**Eslatma:** `nodeName` har doim HTML elementining teg nomini katta harfda o'z ichiga oladi.
{% endhint %}

### nodeValue xususiyati

`nodeValue` xususiyati nodening qiymatini belgilaydi.

* element nodelari uchun nodeValue `null`
* Matn nodelari uchun nodeValue matnning o'zi
* atribut nodelari uchun nodeValue atributning qiymati hisoblanadi

### NodeType xususiyati

`nodeType` xususiyati faqat o'qish uchun. U node turini qaytaradi.

```
<h1 id="id01">My First Page</h1>
<p id="id02"></p>

<script>
document.getElementById("id02").innerHTML = document.getElementById("id01").nodeType;
</script>
```

Eng muhim nodeType xususiyatlari:

| Node                 | Turi | Misol                                            |
| -------------------- | ---- | ------------------------------------------------ |
| ELEMENT\_NODE        | 1    | \<h1 class="heading">W3Schools\</h1>             |
| ATTRIBUTE\_NODE      | 2    |  class = "heading" (deprecated)                  |
| TEXT\_NODE           | 3    | W3Schools                                        |
| COMMENT\_NODE        | 8    | \<!-- This is a comment -->                      |
| DOCUMENT\_NODE       | 9    | The HTML document itself (the parent of \<html>) |
| DOCUMENT\_TYPE\_NODE | 10   | \<!Doctype html>                                 |

{% hint style="warning" %}
2-tur HTML DOM da eskirgan (lekin ishlaydi). XML DOM da u eskirmagan.
{% endhint %}
