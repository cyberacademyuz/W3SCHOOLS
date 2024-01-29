# Obyekt prototiplari

Barcha obyektlar prototipdan xususiyat va metodlarni meros qilib oladi.

Oldingi byo'limda biz **obekt konstruktoridan** qanday foydalanishni bilib oldik:

```
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
}

const myFather = new Person("John", "Doe", 50, "blue");
const myMother = new Person("Sally", "Rally", 48, "green");
```

Mavjud obyekt konstruktoriga yangi xususiyat qo'sha olmasligingizni ham bilib oldik:

```
Person.nationality = "English";
```

Konstruktorga yangi xususiyat qo'shish uchun uni konstruktor funksiyasiga qo'shishingiz kerak:

```
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
  this.nationality = "English";
}
```

### Prototip inheritance (meros)

Barcha JavaScript obyektlari prototipdan xossa va metodlarni meros qilib oladi:

* `Date` oybektlar meros qilib olinadi`Date.prototype`
* `Array`obyektlar meros qilib olinadi`Array.prototype`
* `Person`obeyktlar meros qilib olinadi`Person.prototype`

`Object.prototype` prototip meros zanjirining tepasida joylashgan:

`Date` ob'ektlar, `Array` ob'ektlar va `Person` obyektlar `Object.prototype`dan meros qilib olinadi.

### Obyektlarga xossalar va metodlarni qo'shish

Ba'zan siz ma'lum turdagi barcha mavjud obyektlarga yangi xususiyatlar (yoki metodlar) qo'shishni xohlaysiz.

Ba'zan obyekt konstruktoriga yangi xususiyatlar (yoki metodlar) qo'shishni xohlaysiz.

### **prototype** xususiyatidan foydalanish

`prototype` xususiyati obyekt konstruktorlariga yangi xususiyat qo'shish imkonini beradi:

```
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
}

Person.prototype.nationality = "English";
```

`prototype` xususiyati, obyekt konstruktorlariga yangi metod qo'shish imkonini beradi:

```
function Person(first, last, age, eyecolor) {
  this.firstName = first;
  this.lastName = last;
  this.age = age;
  this.eyeColor = eyecolor;
}

Person.prototype.name = function() {
  return this.firstName + " " + this.lastName;
};
```

Faqat o'zingizning **prototype-ingizni** o'zgartiring. Hech qachon standart obyektlarning prototiplarini o'zgartirmang.
