# Arraylarni saralash

### Massivni saralash

`sort()` metodi massivni alifbo ketma ketligida tartiblaydi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort" %}

### Massivni teskari aylantirish

`reverse()` metodi massivdagi elementlarni teskari aylantiradi.

Siz undan arrayni teskari tartibda saralash uchun foydalanishingiz mumkin:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.sort();
fruits.reverse();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_reverse" %}

### Raqamli saralash

Defult tarzda, `sort()` funksiyasi qiymatlarni **string** sifatida tartiblaydi.

Bu stringlar bilan yaxshi kelishadi. ("Olma" "Banan" dan oldin keladi).

Biroq, agar raqamlar string sifatida tartiblangan bo'lsa, "25" "100" dan katta, chunki "2" "1" dan katta.

Shu sababli, raqamlarni tartiblashda `sort()`  metodi  noto'g'ri ishlaydi.

Buni **taqqoslash funksiyasi** yordamida tuzatishingiz mumkin:

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a - b});
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort2" %}

Massivni teskari tartibda  saralash uchun xuddi shu usuldan foydalaning:

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b - a});
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort3" %}

### Taqqoslash funksiyasi

Taqqoslash funksiyasining vazifasi muqobil saralash tartibini aniqlashdir.

Taqqoslash funksiyasi argumentlarga qarab manfiy, nol yoki musbat qiymat qaytarishi kerak:

```javascript
function(a, b){return a - b}
```

`sort()` funksiyasi 2-ta qiymatni taqqoslaganda, qiymatlarni taqqoslash funksiyasiga yuboradi va qiymatlarni qaytarilgan qiymatga ko'ra tartiblaydi.

Agar natija manfiy bo'lsa, `a` `b` dan oldin tartiblanadi.

Agar natija musbat bo'lsa, `b` `a`dan oldin tartiblanadi.

Agar natija 0 bo'lsa, ikkita qiymatning tartiblash tartibi bilan hech qanday o'zgarish amalga oshirilmaydi.

**Misol:**

Taqqoslash funktsiyasi massivdagi barcha qiymatlarni, bir vaqtning o'zida ikkita qiymatga solishtiradi `(a, b)`.

40 va 100 ni solishtirganda, `sort()` metodi  function(40, 100) solishtirish funksiyasini chaqiradi.

Funksiya 40 - 100 ni hisoblaydi `(a - b)` va natija manfiy bo'lgani uchun (-60), tartiblash funksiyasi 40 ni 100 dan kichik qiymat sifatida saralaydi.

Raqamli va alifbo tartibida tartiblashni sinab ko'rish uchun ushbu kod snippetidan foydalanishingiz mumkin:

```html
<button onclick="myFunction1()">Sort Alphabetically</button>
<button onclick="myFunction2()">Sort Numerically</button>

<p id="demo"></p>

<script>
const points = [40, 100, 1, 5, 25, 10];
document.getElementById("demo").innerHTML = points;

function myFunction1() {
  points.sort();
  document.getElementById("demo").innerHTML = points;
}

function myFunction2() {
  points.sort(function(a, b){return a - b});
  document.getElementById("demo").innerHTML = points;
}
</script>
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_alpha" %}

### Arrayni tasodifiy tartibda saralash

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(){return 0.5 - Math.random()});
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_random" %}

### Fisher Yates usuli

Yuqoridagi misolda, array.sort() aniqlik bilan ishlamaydi. U ba'zi raqamlarni boshqalaridan afzal ko'radi.

Arraylarni tasodifiy tartiblashning eng mashhur usuli **Fisher Yates shuffle** deb ataladi va 1938 yilda data sciencega kiritilgan!

JavaScript-da bu usulni mana bunday yozish mumkin:

```javascript
const points = [40, 100, 1, 5, 25, 10];

for (let i = points.length -1; i > 0; i--) {
  let j = Math.floor(Math.random() * (i+1));
  let k = points[i];
  points[i] = points[j];
  points[j] = k;
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_random2" %}

### Arrayning eng katta (yoki eng kichik) qiymatini toping

Arrayda eng katta yoki eng kichik qiymatni topish uchun o‘rnatilgan funksiyalar mavjud emas.

Biroq, arrayni tartiblaganingizdan so'ng, eng katta va eng kichik qiymatlarni olish uchun indexdan foydalanishingiz mumkin.

Kichikdan katta qiymatga qarab saralash:

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return a - b});
// Endi points[0] eng kichik qiymatni o'z ichiga oladi
// va points[points.length-1] eng katta qiymatni o'z ichiga oladi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_low" %}

Eng kattadan kichik qiymatga qarab saralash:

```javascript
const points = [40, 100, 1, 5, 25, 10];
points.sort(function(a, b){return b - a});
// Endi points[0] eng katta qiymatni o'z ichiga oladi
// va points[points.length-1] eng kichik qiymatni o'z ichiga oladi
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_high" %}

{% hint style="warning" %}
Agar faqat eng katta (yoki eng kichik) qiymatni topmoqchi bo'lsangiz, butun arrayni saralash samarasiz usuldir.
{% endhint %}

### Arrayda Math.max() dan foydalanish

Arraydagi eng katta raqamni topish uchun `Math.max.apply`dan foydalanishingiz mumkin :

```javascript
function myArrayMax(arr) {
  return Math.max.apply(null, arr);
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_math_max" %}

`Math.max.apply(null, [1, 2, 3])` `Math.max(1, 2, 3)` ga teng.

### Arrayda Math.min() dan foydalanish

Arraydagi eng kichik raqamni topish uchun `Math.min.apply` foydalanishingiz mumkin:

```javascript
function myArrayMin(arr) {
  return Math.min.apply(null, arr);
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_math_min" %}

`Math.min.apply(null, [1, 2, 3])` `Math.min(1, 2, 3)` ga teng.

### Mening Min / Max metodlarim

Eng tezkor yechim "home mede" usulidan foydalanishdir.

Ushbu funksiya har bir qiymatni topilgan eng yuqori qiymat bilan taqqoslaydigan array elementlari bo'ylab aylanadi:

{% code title="Eng katta qiymatni topish:" %}
```javascript
function myArrayMax(arr) {
  let len = arr.length;
  let max = -Infinity;
  while (len--) {
    if (arr[len] > max) {
      max = arr[len];
    }
  }
  return max;
}
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_max" %}

Ushbu funksiya har bir qiymatni topilgan eng kichik qiymat bilan taqqoslaydigan array elementlari bo'ylab aylanadi:

{% code title="Eng kichik sonni topish:" %}
```javascript
function myArrayMin(arr) {
  let len = arr.length;
  let min = Infinity;
  while (len--) {
    if (arr[len] < min) {
      min = arr[len];
    }
  }
  return min;
}
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_min" %}

### Obyekt arraylarini saralash

Arraylar ko'pincha obyektlarni o'z ichiga oladi:

```javascript
const cars = [
  {type:"Volvo", year:2016},
  {type:"Saab", year:2001},
  {type:"BMW", year:2010}
];
```

Obyektlar har xil turdagi ma'lumotlarning xususiyatlariga ega bo'lsa ham,  `sort()` metodi arrayni saralash uchun ishlatilishi mumkin.

Buning yechimi xususiyatlarning qiymatlarini solishtirish uchun taqqoslash funksiyasini yozishdir:

```javascript
cars.sort(function(a, b){return a.year - b.year});
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_object1" %}

String xususiyatlarini solishtirish biroz murakkabroq:

```javascript
cars.sort(function(a, b){
  let x = a.type.toLowerCase();
  let y = b.type.toLowerCase();
  if (x < y) {return -1;}
  if (x > y) {return 1;}
  return 0;
});
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_sort_object2" %}

{% hint style="warning" %}
### Massiv haqida to'liq ma'lumotnoma

Massiv haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda massiv haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_array.asp)

Ma'lumotnomada massivning barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
