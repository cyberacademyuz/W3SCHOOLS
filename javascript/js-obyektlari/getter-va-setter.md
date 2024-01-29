# Getter va setter

### JavaScriptda getterlar va setterlar

ECMAScript 5 (ES5 2009) Getter va Setterlarni taqdim qildi.

Getterlar va setterlar obyektga murojaat qilish vositalarini (hisoblash xususiyatlari) ifodalashga imkon beradi.

### JavaScript Getter (get kalit so'zi)

Bu misolda `language` xususiyatining qiymatini olish (`get`) uchun `lang` xususiyatidan foydalanilgan.

```
// Create an object:
const person = {
  firstName: "John",
  lastName: "Doe",
  language: "en",
  get lang() {
    return this.language;
  }
};

// Display data from the object using a getter:
document.getElementById("demo").innerHTML = person.lang;
```

### JavaScript setter (set kalit soʻz)

Ushbu misolda language xususiyatining qiymatini belgilash (`set`) uchun `lang` xususiyatidan foydalanilgan.

```
const person = {
  firstName: "John",
  lastName: "Doe",
  language: "",
  set lang(lang) {
    this.language = lang;
  }
};

// Set an object property using a setter:
person.lang = "en";

// Display data from the object:
document.getElementById("demo").innerHTML = person.language;
```

### Funktsiyami yoki Getter ?

Ushbu ikki misol o'rtasidagi farq qanday ?

#### 1-misol

```
const person = {
  firstName: "John",
  lastName: "Doe",
  fullName: function() {
    return this.firstName + " " + this.lastName;
  }
};

// Display data from the object using a method:
document.getElementById("demo").innerHTML = person.fullName();
```

#### 2-misol

```
const person = {
  firstName: "John",
  lastName: "Doe",
  get fullName() {
    return this.firstName + " " + this.lastName;
  }
};

// Display data from the object using a getter:
document.getElementById("demo").innerHTML = person.fullName;
```

1-misolda fullName-ga funksiya sifatida murojaat qilish ko'rsatilgan: person.fullName().

2-misolda fullName-ga xususiyat sifatida murojaat qilish ko'rsatilgan: person.fullName.

Ikkinchi misol soddaroq sintaksis taqdim qiladi.

### Ma'lumot sifati

Getter va setterlardan foydalanganda ma'lumotlar sifatini yaxshilash mumkin.

Ushbu misol `lang` xususiyatidan foydalanib, `language` xususiyatining qiymatini katta harfda  qaytaradi:

```
// Create an object:
const person = {
  firstName: "John",
  lastName: "Doe",
  language: "en",
  get lang() {
    return this.language.toUpperCase();
  }
};

// Display data from the object using a getter:
document.getElementById("demo").innerHTML = person.lang;
```

Ushbu misol `lang` xususiyatidan foydalanib, `language` xususiyatining qiymatini katta harfda  saqlaydi:

```
const person = {
  firstName: "John",
  lastName: "Doe",
  language: "",
  set lang(lang) {
    this.language = lang.toUpperCase();
  }
};

// Set an object property using a setter:
person.lang = "en";

// Display data from the object:
document.getElementById("demo").innerHTML = person.language;
```

### Nima uchun Getter va Setterlardan dan foydalanish kerak ?

* Bu soddaroq sintaksisda yozish imkonini beradi
* U xususiyatlar va metodlar uchun bir xil sintaksisga imkon beradi
* Bu ma'lumotlar sifatini xavfsiz ta'minlashi mumkin
* Bu narsalarni "sahna ortida" qilishda foyda beradi

### Object.defineProperty()

`Object.defineProperty()` metodi getter va setterlarni qo'shish uchun ham ishlatilishi mumkin:

```
// Define object
const obj = {counter : 0};

// Define setters and getters
Object.defineProperty(obj, "reset", {
  get : function () {this.counter = 0;}
});
Object.defineProperty(obj, "increment", {
  get : function () {this.counter++;}
});
Object.defineProperty(obj, "decrement", {
  get : function () {this.counter--;}
});
Object.defineProperty(obj, "add", {
  set : function (value) {this.counter += value;}
});
Object.defineProperty(obj, "subtract", {
  set : function (value) {this.counter -= value;}
});

// Play with the counter:
obj.reset;
obj.add = 5;
obj.subtract = 1;
obj.increment;
obj.decrement;
```
