# Funksiya Closure

JavaScript o'zgaruvchilari **lokal** yoki **global** miqyosga tegishli bo'la oladi.

Global o'zgaruvchilarni **closure** bilan lokal qilish mumkin.

### Global o'zgaruvchilar

`function` funktsiya **ichida** yaratilgan barcha o'zgaruvchilarga murojaat qilishi mumkin, masalan:

```
function myFunction() {
  let a = 4;
  return a * a;
}
```

Bundan tashqari `function` funksiyadan **tashqarida** e'lon qilingan o'zgaruvchilarga ham murojaat qila oladi, masalan:

```
let a = 4;
function myFunction() {
  return a * a;
}
```

Oxirgi misoldagi **a global** o'zgaruvchidir.

Veb-sahifada global o'zgaruvchilar sahifaga tegishli.

Global o'zgaruvchilar sahifadagi barcha boshqa skriptlar tomonidan ishlatilishi (va o'zgartirilishi) mumkin.

Birinchi misolda **a lokal** o'zgaruvchidir.

Lokal o'zgaruvchidan faqat u e'lon qilingan funktsiya ichida foydalanish mumkin. U boshqa funksiyalardan va boshqa skript kodlaridan yashiringan.

Xuddi shu nomdagi global va lokal o'zgaruvchilar turli xil o'zgaruvchilar hisoblanadi. Birini o'zgartirish ikkinchisini o'zgartirmaydi.

{% hint style="warning" %}
### Eslatma

Deklaratsiya kalit so'zisiz yaratilgan o'zgaruvchilar (var, let yoki const) har doim global o'zgaruvchi bo'ladi, hatto ular funksiya ichida yaratilgan bo'lsa ham.
{% endhint %}

```
function myFunction() {
  a = 4;
}
```

### O'zgaruvchining ishlash vaqti

Global o'zgaruvchilar sahifa o'chirilmaguncha, masalan, boshqa sahifaga o'tayotganingizda yoki oynani yopguningizgacha ishlaydi.

Lokal o'zgaruvchilarning umri esa qisqa. Ular funktsiya chaqirilganda yaratiladi va funksiya tugagach o'chiriladi.

### Sanoq

Faraz qilaylik, siz biror narsani hisoblash uchun o'zgaruvchidan foydalanmoqchisiz va bu hisoblagich barcha funksiyalar uchun mavjud bo'lishini xohlaysiz.

Hisoblagichni oshirish uchun global o'zgaruvchidan va `function` dan foydalanishingiz mumkin :

```
// Initiate counter
let counter = 0;

// Function to increment counter
function add() {
  counter += 1;
}

// Call add() 3 times
add();
add();
add();

// The counter should now be 3
```

Yuqoridagi yechim bilan bog'liq muammo bor: sahifadagi har qanday kod `add()` ni chaqirmasdan turib hisoblagichni o'zgartirishi mumkin.

Hisoblagich boshqa kodni o'zgartirishiga yo'l qo'ymaslik uchun add() funktsiyasi uchun lokal bo'lishi kerak:

```
// Initiate counter
let counter = 0;

// Function to increment counter
function add() {
  let counter = 0;
  counter += 1;
}

// Call add() 3 times
add();
add();
add();

//The counter should now be 3. But it is 0
```

Bu ishlamadi, chunki biz lokal hisoblagich o'rniga global hisoblagichni ko'rsatdik.

Biz global hisoblagichni olib tashlashimiz va funksiyani qaytarishiga ruxsat berish orqali lokal hisoblagichga murojaat qilishimiz mumkin:

```
// Function to increment counter
function add() {
  let counter = 0;
  counter += 1;
  return counter;
}

// Call add() 3 times
add();
add();
add();

//The counter should now be 3. But it is 1.
```

Bu ishlamadi, chunki biz har safar funktsiyani chaqirganimizda lokal hisoblagichni qayta tiklaymiz.

&#x20;**JavaScriptning ichki funksiyasi buni bartaraf qilishi mumkin.**

### JavaScript-ning ichki built-in funksiyalari

Barcha funktsiyalar global miqyosda murojaat qilish huquqiga ega. &#x20;

Aslida, JavaScript-da barcha funktsiyalar o'zining "yuqori" doirasiga murojaat qilish huquqiga ega.

JavaScript ichki built-in funktsiyalarni qo'llab-quvvatlaydi. Ichki funksiyalar o'zining "yuqorisida joylashgan" scopeag murojaat qilish huquqiga ega.

Ushbu misolda, ichki `plus()` funksiyasi tashqi funktsiyadagi `counter` o'zgaruvchisiga murojaat qilish huquqiga ega:

```
function add() {
  let counter = 0;
  function plus() {counter += 1;}
  plus();   
  return counter;
}
```

Agar funksiyaga tashqaridan murojaat olsak, bu counter muammosini hal qilishi mumkin.

Bundan tashqari, `counter = 0` ni faqat bir marta bajarish yo'lini topishimiz kerak .

**Bizga closure kerak.**

### JavaScript closure-lari

O'z-o'zidan chaqiriladigan funktsiyalarni eslaysizmi ? Bu funksiya nima qiladi ?

```
const add = (function () {
  let counter = 0;
  return function () {counter += 1; return counter}
})();

add();
add();
add();

// the counter is now 3
```

### Misolni tushuntirish

`add` o'zgaruvchisi o'z-o'zidan chaqiriladigan funktsiyaning return qiymatiga tayinlanadi.

O'z-o'zini chaqirish funktsiyasi faqat bir marta ishlaydi. Counterni nolga (0) o'rnatadi va function expression qaytaradi.

Shu tarzda add funksiyaga aylanadi. "Ajoyib" tomoni shundaki, u ota-ona doirasidagi counterga  murojaat qilad oladi.

Bu JavaScript-ni **clouser** qilish deb ataladi**.** Bu funktsiyaga  "**maxsus**" o'zgaruvchilarga ega bo'lish imkonini beradi.

Counter anonim funksiya doirasi bilan himoyalangan va uni faqat add funksiyasi yordamida o‘zgartirish mumkin.

{% hint style="warning" %}
Closure - bu ota-ona funksiyasi yopilgandan keyin ham ota-ona doirasiga murojaat qilish huquqiga ega bo'lgan funksiya.
{% endhint %}
