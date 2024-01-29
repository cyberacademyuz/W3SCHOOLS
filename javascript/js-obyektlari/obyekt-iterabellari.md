# Obyekt iterabellari

{% hint style="success" %}
Iteratsiyali obyektlar - `for..of`  bilan takrorlanishi mumkin bo'lgan obyektlardir.

Texnik jihatdan, iterablelar `Symbol.iterator` metodini bajarishi kerak.
{% endhint %}

### String ustida iteratsiya

String elementlarini takrorlash uchun `for..of` tsiklidan foydalanishingiz mumkin:

```
for (const x of "W3Schools") {
  // code block to be executed
}
```

### Massiv ustida iteratsiya

Massiv elementlarini takrorlash uchun `for..of` siklidan foydalanishingiz mumkin:

```
for (const x of [1,2,3,4,5]) {
  // code block to be executed
}
```

### JavaScript iteratorlari

Iterator protokoli obyektdan qiymatlar ketma-ketligini qanday yaratishni belgilaydi.

Obyekt `next()` metodini amalga oshirganda iteratorga aylanadi.

`next()` metodi ikkita xususiyatga ega obyekt qaytarishi kerak:

* qiymat (keyingi qiymat)
* bajarilgan (to'g'ri yoki noto'g'ri)

| qiymat    | <p>Iterator tomonidan qaytarilgan qiymat<br>(agar true bo'lsa, o'tkazib yuborilishi mumkin)</p>                     |
| --------- | ------------------------------------------------------------------------------------------------------------------- |
| bajarildi | <p>agar iterator tugallangan bo'lsa true </p><p>agar itertrueator yangi qiymat yaratgan bo'lsa<em>, false</em> </p> |

### Qo'lda iteratsiya qilish

Bu takrorlanuvchi iteratsiya  hech qachon tugamaydi: Har safar `next()` chaqirilganida 10,20,30,40,.... kabi davom etaveradi.

```
// Home Made Iterable
function myNumbers() {
  let n = 0;
  return {
    next: function() {
      n += 10;
      return {value:n, done:false};
    }
  };
}

// Create Iterable
const n = myNumbers();
n.next(); // Returns 10
n.next(); // Returns 20
n.next(); // Returns 30
```

{% hint style="warning" %}
Home made iteratsiyasi bilan bo'gliq muammo:

U `for..of` steytmentini qo'llab-quvvatlamaydi.
{% endhint %}

Iterable - bu **Symbol.iterator**ga ega bo'lgan obyektdir.

`Symbol.iterator` `next()` funktsiyani qaytaradigan funktsiyadir.

Kod bilan iteratsiyani takrorlash mumkin: `for (const x of iterable) { }`

```
// Create an Object
myNumbers = {};

// Make it Iterable
myNumbers[Symbol.iterator] = function() {
  let n = 0;
  done = false;
  return {
    next() {
      n += 10;
      if (n == 100) {done = true}
      return {value:n, done:done};
    }
  };
}

```

Endi `for..of` dan foydalanishingiz mumkin:

```
for (const num of myNumbers) {
  // Any Code Here
}
```

Symbol.iterator metodi avtomatik ravishda `for..of` tomonidan chaqiriladi.

Ammo biz buni "qo'lda" ham qilishimiz mumkin:

```
let iterator = myNumbers[Symbol.iterator]();

while (true) {
  const result = iterator.next();
  if (result.done) break;
  // Any Code Here
}
```
