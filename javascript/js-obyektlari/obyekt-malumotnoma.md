# Obyekt ma'lumotnoma

{% hint style="success" %}
ECMAScript 5 (2009) JavaScript-ga juda ko'p yangi obyekt metodlarini qo'shdi.
{% endhint %}

#### Obyektlarni boshqarish

```
// Prototip sifatida mavjud obyekt bilan boshqa bir obyekt yaratish
Object.create()

// Obyekt prototipini qo'shish va o'chirish
Object.defineProperty(object, property, descriptor)

// Obyekt xususiyatini qo'shish va o'chirish
Object.defineProperties(object, descriptors)

// Xususiyatlarga murojaat qilish
Object.getOwnPropertyDescriptor(object, property)

// Barcha xususiyatlarni array sifatida qaytarish
Object.getOwnPropertyNames(object)

// Prototipga murojaat qilish
Object.getPrototypeOf(object)

// Sanaluvchi xususiyatlarni massiv sifatida qaytaradi
Object.keys(object)


```

#### Obyektlarni himoya qilish

```
// Obyektga xususiyatlar qo'shishni oldini oladi
Object.preventExtensions(object)

// Agar xususiyatlar obyektga qo'shilishi mumkin bo'lsa, true qiymatini qaytaradi
Object.isExtensible(object)

// Obyekt xususiyatlarining o'zgarishini oldini oladi (qiymatlarni emas)
Object.seal(object)

// Obyekt muhrlangan bo'lsa, true qiymatini qaytaradi
Object.isSealed(object)

// Obyektdagi har qanday o'zgarishlarni oldini oladi
Object.freeze(object)

// Obyekt muzlatilgan bo'lsa, true qiymatini qaytaradi
Object.isFrozen(object)
```

### Xususiyat qiymatini o'zgartirish

```
Object.defineProperty(object, property, {value : value})
```

Ushbu misoldagi kod xususiyat qiymatini o'zgartiradi:

```
const person = {
  firstName: "John",
  lastName : "Doe",
  language : "EN"
};

// Change a property
Object.defineProperty(person, "language", {value : "NO"});
```

### Meta ma'lumotlarini o'zgartirish

ES5 dagi quyidagi xususiyat meta-ma'lumotlarini o'zgartirishga imkon beradi:

```
writable : true      // Xususiyat qiymatini o'zgartirish mumkin
enumerable : true    // Xususiyatni sanab o'tish mumkin
configurable : true  // Xususiyat qayta sozlanishi mumkin

writable : false     // Xususiyat qiymatini o'zgartirish mumkin emas
enumerable : false   // Xususiyatni sanab bo'lmaydi
configurable : false // Xususiyat qayta sozlanishi mumkin emas
```

ES5 getterlarni va setterlarni o'zgartirishga imkon beradi:

```
// Defining a getter
get: function() { return language }
// Defining a setter
set: function(value) { language = value }
```

Ushbu kod language-ni  faqat o'qish uchun qiladi:

```
Object.defineProperty(person, "language", {writable:false});
```

Ushbu kod language-ni sanab bo'lmaydigan qiladi:

```
Object.defineProperty(person, "language", {enumerable:false});
```

### Barcha xususiyatlarni ro'yxatga olish

Ushbu kod obyektning barcha xususiyatlarini ko'rsatadi:

```
const person = {
  firstName: "John",
  lastName : "Doe",
  language : "EN"
};

Object.defineProperty(person, "language", {enumerable:false});
Object.getOwnPropertyNames(person);  // Returns an array of properties
```

### Ro'yxatga olish mumkin bo'lgan xususiyatlar

Ushbu misolda faqat obyektning sanab bo'ladigan xususiyatlari keltirilgan:

```
const person = {
  firstName: "John",
  lastName : "Doe",
  language : "EN"
};

Object.defineProperty(person, "language", {enumerable:false});
Object.keys(person);  // Returns an array of enumerable properties
```

### Xususiyat qo'shish

Ushbu kod obyektga yangi xususiyat qo'shadi:

```
// Create an object:
const person = {
  firstName: "John",
  lastName : "Doe",
  language : "EN"
};

// Add a property
Object.defineProperty(person, "year", {value:"2008"});
```

### Getterlar va setterlar qo'shish

`Object.defineProperty()`metodi getterlar va Setterlarni qo'shish uchun ham ishlatilishi mumkin:

```
//Create an object
const person = {firstName:"John", lastName:"Doe"};

// Define a getter
Object.defineProperty(person, "fullName", {
  get: function () {return this.firstName + " " + this.lastName;}
});
```

### Qarshi misol

```
// Define object
const obj = {counter:0};

// Define setters
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
  set : function (i) {this.counter -= i;}
});

// Play with the counter:
obj.reset;
obj.add = 5;
obj.subtract = 1;
obj.increment;
obj.decrement;
```
