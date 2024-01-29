# Funksiya Call

### Metodni qayta ishlatish

`call()` metodi yordamida turli obyektlarda foydalanish mumkin bo'lgan metod yozishingiz mumkin.

### Barcha funktsiyalar metodlardir

JavaScript-da barcha funktsiyalar obyekt metodlari hisoblanadi.

Agar funktsiya obyektning metodi bo'lmasa, u global obyektning funktsiyasidir.

Quyidagi misol 3 ta xususiyatga ega obyekt yaratadi: **firstName**, **LastName**, **fullName**.

```
const person = {
  firstName:"John",
  lastName: "Doe",
  fullName: function () {
    return this.firstName + " " + this.lastName;
  }
}

// This will return "John Doe":
person.fullName();  
```

Yuqoridagi misolda `this` person obyektini bildiradi.

**this.firstName** `this`ning **firstName** xususiyatini bildiradi.

Xuddi shunday:

**this.firstName** personning **firstName** xususiyatini bildiradi.

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

### call() metodi

`call()` metodi JavaScriptning built-in metodi hisoblanadi.

U obyekt egasi bilan metodni chaqirish  uchun  argument (parametr) sifatida ishlatilishi mumkin.

{% hint style="warning" %}
`call()` bilan, obyekt boshqa obyektga tegishli metoddan foydalanishi mumkin.
{% endhint %}

Bu misol **person1** dan foydalanib, personning **fullName** metodini chaqiradi:

```
const person = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}
const person1 = {
  firstName:"John",
  lastName: "Doe"
}
const person2 = {
  firstName:"Mary",
  lastName: "Doe"
}

// This will return "John Doe":
person.fullName.call(person1);
```

Bu misol **person2** dan foydalanib, personning **fullName** metodini chaqiradi:

```
const person = {
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
}
const person1 = {
  firstName:"John",
  lastName: "Doe"
}
const person2 = {
  firstName:"Mary",
  lastName: "Doe"
}

// This will return "Mary Doe"
person.fullName.call(person2);
```

### call() metodi argumentlar bilan birga

`call()` metodi argumentlarni qabul qilishi mumkin:

```
const person = {
  fullName: function(city, country) {
    return this.firstName + " " + this.lastName + "," + city + "," + country;
  }
}

const person1 = {
  firstName:"John",
  lastName: "Doe"
}

person.fullName.call(person1, "Oslo", "Norway");
```
