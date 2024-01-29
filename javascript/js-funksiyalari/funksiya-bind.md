# Funksiya Bind

### Funktsiyani qarzga olish

`bind()` metodi yordamida obyekt boshqa obyektdan metod olishi mumkin.

Quyidagi misol 2 ta obyekt (person va member) yaratadi.

Member obyekti person obyektidan fullName metodini oladi:

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

### this-ni saqlang

`this`ni yo'qotmaslik uchun ba'zan `bind()` metodidan foydalanish kerak bo'ladi.

Quyidagi misolda person obyekti display metodiga ega. Display metodida `this` person obyektiga ishora qiladi:

```
const person = {
  firstName:"John",
  lastName: "Doe",
  display: function () {
    let x = document.getElementById("demo");
    x.innerHTML = this.firstName + " " + this.lastName;
  }
}

person.display();
```

Agar funktsiya callback sifatida ishlatilsa, u yo'qoladi.

Ushbu misol 3 soniyadan keyin person ismini ekranda ko'rsatishga harakat qiladi, lekin uning o'rniga `undefined` ko'rsatiladi:

```
const person = {
  firstName:"John",
  lastName: "Doe",
  display: function () {
    let x = document.getElementById("demo");
    x.innerHTML = this.firstName + " " + this.lastName;
  }
}

setTimeout(person.display, 3000);
```

`bind()` metodi bu muammoni hal qiladi.

Quyidagi misolda person.displayni personga bog'lash uchun `bind()` metodi qo'llaniladi.

Ushbu misol 3 soniyadan so'ng person ismini ekranda ko'rsatadi:

```
const person = {
  firstName:"John",
  lastName: "Doe",
  display: function () {
    let x = document.getElementById("demo");
    x.innerHTML = this.firstName + " " + this.lastName;
  }
}

let display = person.display.bind(person);
setTimeout(display, 3000);
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
