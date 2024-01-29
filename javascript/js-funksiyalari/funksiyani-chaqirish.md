# Funksiyani chaqirish

JavaScript ichidagi `function` kodi "biror narsa" uni chaqirganda bajariladi.

### JavaScript funksiyasini chaqirish

**Funktsiya yaratilgan** funksiya ichidagi kod bajarilmaydi.

Funksiya ichidagi kod funksiya chaqirilgandagina **bajariladi**.

Funksiyani chaqirishni "funksiyani ishga tushirish" yoki "funksiyani bajarish" deb aytish odatiy holga aylangan.

Ushbu qo'llanmada biz **invoke** dan foydalanamiz, chunki, funksiyalarga murojaat qilinmasdan ham ularni ishga tushirish mumkin.

### Funksiyani funksiya sifatida chaqirish

```
function myFunction(a, b) {
  return a * b;
}
myFunction(10, 2);           // Will return 20
```

Yuqoridagi funktsiya hech qanday obyektga tegishli emas. Lekin JavaScript-da har doim standart global obyekt mavjud.

HTMLda standart global obyekt HTML sahifaning o'zi, shuning uchun yuqoridagi funktsiya HTML sahifasiga "tegishli".

Brauzerda sahifa obyekti brauzer oynasi hisoblanadi. Yuqoridagi funksiya avtomatik tarzda window funksiyasiga aylanadi.

{% hint style="warning" %}
### Eslatma

Bu funksiyani chaqirishning keng tarqalgan usuli, lekin unchalik yaxshi amaliyot emas.\
Global o'zgaruvchilar, metodlar yoki funktsiyalar global obyektda nomlardagi ziddiyatlarni va xatolarni osongina keltirib chiqarishi mumkin.
{% endhint %}

myFunction() va window.myFunction() bir xil funksiya:

```
function myFunction(a, b) {
  return a * b;
}
window.myFunction(10, 2);    // Will also return 20
```

### This nima ?

JavaScript-da `this` kalit so'zi obyektga yo'naladi qiladi.

`this` qaysi obyekt qanday chaqirilayotganiga (ishlatilganiga yoki chaqirilganiga) bog'liq.

`this` kalit so'zi qanday ishlatilishiga qarab turli xil obyektlarga yo'naladi qiladi:

| `this` obyekt metodida obyektning o'ziga yo'naladi.                                             |
| ----------------------------------------------------------------------------------------------- |
| `this`  yakka holda,  global obyektga yo'naladi.                                                |
| `this` funktsiyada global obyektga yo'naladi.                                                   |
| `this` qat'iy rejimda funktsiyada `undefined` bo'ladi                                           |
| `this` eventda, hodisani qabul qilgan elementga yo'naladi.                                      |
| `call()`, `apply()`va `bind()` kabi metodlar `this`ni har qanday obyektga yo'naltirishi mumkin. |

{% hint style="warning" %}
### Eslatma

`this` o'zgaruvchi emas. Bu kalit so'z. `this`ning qiymatini o'zgartira olmaysiz.

### Shuningdek qarang:

[JavaScriptda **this** qo'llanmasi](https://www.w3schools.com/js/js\_this.asp)
{% endhint %}

### Global obyekt

Funksiya egasi obyektisiz chaqirilganda, `this`ning qiymati global obyektga aylanadi.

Veb-brauzerda global obyekt brauzer oynasi hisoblanadi.

Bu misol windows obyektini `this` ning qiymati sifatida qaytaradi:

```
let x = myFunction();            // x will be the window object

function myFunction() {
  return this;
}
```

{% hint style="warning" %}
Funktsiyani global funktsiya sifatida chaqirish, `this`ning qiymati global obyekt bo'lishiga olib keladi.\
window obyektini o'zgaruvchi sifatida ishlatish dasturni osongina buzishi mumkin.
{% endhint %}

### Funksiyani metod sifatida chaqirish

JavaScript-da funksiyalarni obyekt metodlar sifatida belgilashingiz mumkin.

Quyidagi misol obyektni (**myObject**), ikkita xususiyat (**firstName** va **LastName**) va metod ( **fullName**) bilan yaratadi:

```
const myObject = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  }
}
myObject.fullName();         // Will return "John Doe"
```

**fullName** metodi funksiyadir. Funksiya obyektga tegishli. **myObject** funksiyaning egasidir.

`this` deb nomlangan narsa JavaScript kodiga "egalik qiluvchi" obyektdir. Bu holatda `this`ning qiymati **myObject** hisoblanadi.

Sinab ko'ring! `this` qiymatini qaytarish uchun **fullName** metodini o'zgartiring:

```
const myObject = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this;
  }
}

// This will return [object Object] (the owner object)
myObject.fullName();

```

{% hint style="warning" %}
Funksiyani obyekt metodi sifatida chaqirish, `this` qiymatini obyektning o'zi bo'lishiga olib keladi.
{% endhint %}

### Funksiya konstruktori yordamida funksiyani chaqirish

Agar funktsiya chaqiruvi `new` kalit so'zidan oldin bo'lsa, u konstruktor chaqiruvidir.

Siz yangi funktsiya yaratganga o'xshaysiz, lekin JavaScript funktsiyalari obyekt bo'lgani uchun aslida yangi obyekt yaratasiz:

```
// This is a function constructor:
function myFunction(arg1, arg2) {
  this.firstName = arg1;
  this.lastName  = arg2;
}

// This creates a new object
const myObj = new myFunction("John", "Doe");

// This will return "John"
myObj.firstName;
```

Konstruktorni chaqirish yangi obyekt yaratadi. Yangi obyekt o'z konstruktoridan xususiyatlar va metodlarni meros qilib oladi.

{% hint style="warning" %}
`this`Konstruktordagi kalit so'z qiymatga ega emas .\
ning qiymati `this`funksiya chaqirilganda yaratilgan yangi ob'ekt bo'ladi.
{% endhint %}
