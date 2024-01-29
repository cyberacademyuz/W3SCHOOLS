# Hoisting

Hoisting - bu deklaratsiyalarni yuqoriga ko'taruvchi JavaScript-ning standart xatti-harakati.

### JavaScript deklaratsiyalari ko'tariluvchandir

JavaScript-da o'zgaruvchini ishlatilganidan keyin ham e'lon qilish mumkin.

Boshqacha qilib aytganda; oʻzgaruvchini eʼlon qilishdan oldin ham foydalanish mumkin

**1-misol 2-misol** bilan bir xil natija beradi:

{% code title="1-misol:" %}
```
x = 5; // Assign 5 to x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x;                     // Display x in the element

var x; // Declare x
```
{% endcode %}

{% code title="2-misol" %}
```
var x; // Declare x
x = 5; // Assign 5 to x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x;                     // Display x in the element
```
{% endcode %}

Buni tushunish uchun hosiying atamasini tushunishingiz kerak

Hoisting JavaScript-ning standart xatti-harakati bo'lib, barcha deklaratsiyalarni joriy scopening yuqori qismiga ko'chiradi.

### let va const kalit so'zlari

let va const bilan eʼlon qilingan o'zgaruvchilar blokning yuqori qismiga ko'tariladi, lekin ishga tushirilmaydi.

Yaʼni: Kod bloki o'zgaruvchini biladi, lekin uni e'lon qilinmaguncha ishlatib bo'lmaydi.

Let o'zgaruvchisini e'lon qilishdan avval ishlatish ReferenceErrorga xatoligiga olib keladi.

O'zgaruvchi blokning boshidan e'lon qilinmaguncha "vaqtinchalik o'lik zonada" bo'ladi:

{% code title="Bu quyidagi ReferenceError xatoligiga olib keladi:" %}
```
carName = "Volvo";
let carName;
```
{% endcode %}

`const` o'zgaruvchini e'lon qilishdan avval ishlatish sintaksis xato hisoblanadi, shu sababli kod shunchaki ishlamaydi.

{% code title="Bu kod ishga tushmaydi." %}
```
carName = "Volvo";
const carName;
```
{% endcode %}

`Let` va `const` haqida [JS Let/Const ](https://www.w3schools.com/js/js\_let.asp)bo'limida batafsil o'qing.

### JavaScript-ni ishga tushirish hoisting bo'lmaydi

JavaScript faqat deklaratsiyalarni hoisting qiladi, ishga tushishni emas emas.

**1-misol 2-misol bilan bir xil** natija bermaydi:

{% code title="1-misol:" %}
```
var x = 5; // Initialize x
var y = 7; // Initialize y

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y;           // Display x and y
```
{% endcode %}

{% code title="2-misol" %}
```
var x = 5; // Initialize x

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y;           // Display x and y

var y = 7; // Initialize y
```
{% endcode %}

Oxirgi misolda y ning aniqlanmaganligi biror ma'no bildiradimi ?

Buning sababi shundaki, ishga tushirish (=7) emas, balki faqatgina deklaratsiya (var y) hoisting bo'ladi.

Hoisting sababli, y uni ishlatishdan avval e'lon qilingan, lekin ishga tushirishlar ko'tarilmagani uchun y qiymati aniqlanmagan.

2-misol quyidagi bilan bir xil:

```
var x = 5; // Initialize x
var y;     // Declare y

elem = document.getElementById("demo"); // Find an element
elem.innerHTML = x + " " + y;           // Display x and y

y = 7;    // Assign 7 to y
```

### O'zgaruvchilaringizni tepada e'lon qiling!

Hoisting (ko'plab dasturchilar uchun) JavaScript-ning noma'lum yoki e'tibordan chetda qolgan harakati hisoblanadi.

Agar dasturchi hoistigni tushunmasa, dasturlarda xatolar bo'lishi mumkin.

Xatolarni oldini olish uchun har doim barcha o'zgaruvchilarni har bir scope boshida e'lon qiling.

JavaScript kodni shunday ifodalagani sababli, bu har doim yaxshi qoida hisoblanadi.

{% hint style="warning" %}
Strict modeda o'zgaruvchilar e'lon qilinmasa, ulardan foydalanishga ruxsat bermaydi. Keyingi bo'limda **"qat'iy rejim"** haqida batafsil o'rganing.
{% endhint %}
