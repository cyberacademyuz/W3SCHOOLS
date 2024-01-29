# This kalit so'zi

```
const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```

## Bu nima ?

JavaScript-da `this` kalit so'zi obyektga ishora qiladi.

`this` qaysi obyekt qanday chaqirilayotganiga (ishlatilgan yoki chaqirilganiga) bog'liq.

`this` kalit so'zi qanday ishlatilishiga qarab turli xil obyektlarga ishora qiladi:

| Obekt metodida, `this` obyektga ishora qiladi.                                                    |
| ------------------------------------------------------------------------------------------------- |
| Yakka tartibda, `this` global obyektga ishora qiladi.                                             |
| Funktsiyada `this` global obyektga ishora qiladi.                                                 |
| Funktsiyada, qat'iy rejimda `this` `undefined` bo'ladi.                                           |
| Eventda, `this` hodisani qabul qilgan elementga ishora qiladi.                                    |
| `call()`, `apply()`va `bind()` kabi metodlar `this` ni har qanday obyektga havola qilishi mumkin. |

{% hint style="info" %}
### Eslatma

`this` o'zgaruvchi emas. Bu kalit so'z. `this`ning qiymatini o'zgartira olmaysiz.
{% endhint %}

### Metodda this

Obyekt metodida `this`dan foydalanilganda, obyektga ishora qiladi.

Ushbu sahifaning yuqori qismidagi misolda `this` person obyektiga ishora qiladi.

Chunki fullName metodi person obyektining metodi hisoblanadi.

```
fullName : function() {
  return this.firstName + " " + this.lastName;
}
```

### Yakka tartibdagi thisz

`This`ni bir o'zinigina ishlatish global obyektga ishora qiladi.

Chunki `this` global miqyosda ishlaydi.

Brauzer oynasida global obyekt `[object Window]`:

```
let x = this;
```

**Qat'iy rejimda** `this` dab yolg'iz foydalanilganda u global obyektga ham tegishli:

```
"use strict";
let x = this;
```

### bu funktsiyada (standart)

Funksiyada global ob'ekt standart bog'lovchi hisoblanadi `this`.

Brauzer oynasida global ob'ekt `[object Window]`:

```
function myFunction() {
  return this;
}
```

### Funksiyada this (qat'iy)

Funktsiyada global ob'ekt `this` uchun standart bog'lovchi hisoblanadi.

Brauzer oynasida global obyekt \[object Window]:

```
"use strict";
function myFunction() {
  return this;
}
```

### Eventni boshqarish vositalarida this

HTML hodisaga ishlov beruvchilarida `this` hodisani qabul qilgan HTML elementiga ishora qiladi:

```
<button onclick="this.style.display='none'">
  Click to Remove Me!
</button>
```

### Obyekt metodini bog'lash

Ushbu misollarda `this` **person** obekti hisoblanadi:

```
const person = {
  firstName  : "John",
  lastName   : "Doe",
  id         : 5566,
  myFunction : function() {
    return this;
  }
};
```

```
const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```

Ya'ni: **this.firstName** `this`ning **firstName** xususiyati hisoblanadi (person obyekti).

### Aniq funktsiyani bog'lash

`call()` va `apply()` metodlari oldindan o'rnatilgan JavaScript metodlari hisoblanadi.

Ularning ikkalasi ham obyekt meodini boshqa obekt bilan argument sifatida chaqirish uchun ishlatilishi mumkin.

{% hint style="warning" %}
### Bularnin ham ko'ring:

[Function call() metodi](https://www.w3schools.com/js/js\_function\_call.asp)

[Function apply() metodi](https://www.w3schools.com/js/js\_function\_apply.asp)

[Function bind() metodi](https://www.w3schools.com/js/js\_function\_bind.asp)
{% endhint %}

Quyidagi misolda person1.fullName argument sifatida person2 bilan chaqiriladi, **fullName** **person1**ning metodi bo'lsada, `this` **person2**ga tegishli:

```
const person1 = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}

const person2 = {
  firstName:"John",
  lastName: "Doe",
}

// Return "John Doe":
person1.fullName.call(person2);
```

### Funktsiyada nusxa olish

`bind()` metodi yordamida obekt boshqa obektdan metodni olishi mumkin.

Bu misol 2 ta obyekt (person va member) yaratadi.

**member** obyekti **person** obyektidan fullname metodini oladi:

```
const person = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  }
}

const member = {
  firstName:"Hege",
  lastName: "Nilsen",
}

let fullName = person.fullName.bind(member);
```

### This ustunligi

this qaysi obyektga tegishli ekanligini aniqlash uchun; quyidagi tartib ustuvorligidan foydalaning.

| Ustunlik | Obyekt                  |
| -------- | ----------------------- |
| 1        | bind()                  |
| 2        | application() va call() |
| 3        | Obyekt metodi           |
| 4        | Global scope            |

`this` funksiyada bind() yordamida chaqiriladimi ?

`this` funksiyada application() yordamida chaqiriladimi ?

`this` funksiyada call() yordamida chaqiriladimi ?

`this` obyekt funktsiyasida (metodda) bormi ?

`this` global scopedagi funksiyadami.
