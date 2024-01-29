# Obyekt metodlari

```
const person = {
  firstName: "John",
  lastName: "Doe",
  id: 5566,
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};
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

`this`o'zgaruvchi emas. Bu kalit so'z. `this`ning qiymatini o'zgartira olmaysiz.

### Shuningdek qarang:

[JavaScriptda **this** qo'llanmasi](https://www.w3schools.com/js/js\_this.asp)
{% endhint %}

### JavaScript metodlari

JavaScript metodlari - bu obyektlarda bajarilishi mumkin bo'lgan harakatlardir.

Metod **funksiya** vazifasini o'z ichiga olgan xususiyatdir.

| Xususiyat | Qiymat                                                    |
| --------- | --------------------------------------------------------- |
| firstName | Jon                                                       |
| lastName  | Doe                                                       |
| age       | 50                                                        |
| eyeColor  | ko'k                                                      |
| fullName  | function() {return this.firstName + " " + this.lastName;} |

{% hint style="warning" %}
Metodlar obyekt xususiyatlari sifatida saqlanadigan funktsiyalardir.
{% endhint %}

### Oyektga murojaat qilish usullari

Siz quyidagi sintaksis bilan obyekt murojaat qilasiz:

```
objectName.methodName()
```

Siz odatda fullName() ni person obyektining metodi sifatida va fullNameni xususiyat sifatida tasvirlaysiz.

FullName xususiyati () bilan chaqirilganda (funksiya sifatida) bajariladi.

Ushbu misol person obyektining **fullName()** metodiga murojaat**:**

```
name = person.fullName();
```

Agar **fullName** xususiyatiga ()siz murojaat qilsangiz**,** u funksiya ta'rifini qaytaradi:

```
name = person.fullName;
```

### Obyektga metod qo'shish

Obyektga yangi metod qo'shish oson:

```
person.name = function () {
  return this.firstName + " " + this.lastName;
};
```

### Avvaldan mavjud metodlardan foydalanish

Ushbu kod matnni bosh harfga aylantirish uchun String obyektining `toUpperCase()` metodidan foydalanadi:

```
let message = "Hello world!";
let x = message.toUpperCase();
```

Yuqoridagi kod bajarilgandan so'ng x-ning qiymati quyidagek bo'ladi:

```
HELLO WORLD!
```

```
person.name = function () {
  return (this.firstName + " " + this.lastName).toUpperCase();
};
```
