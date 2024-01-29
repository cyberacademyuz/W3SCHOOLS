# Obyekt yaratish

{% hint style="warning" %}
JavaScript-da obyektlar qirol hisoblanadi. Agar obyektlarni tushunsangiz, JavaScript-ni tushunasiz.
{% endhint %}

JavaScript-da deyarli "barcha narsa" obyekt.

* Boolean qiymatlar obyekt bo'lishi mumkin (agar `new` kalit so'zi bilan ifodalangan bo'lsa)
* Raqamlar obyekt bo'lishi mumkin (agar `new` kalit so'zi bilan ifodalangan bo'lsa)
* Stringlar obyekt bo'lishi mumkin (agar `new` kalit so'zi bilan ifodalangan bo'lsa)
* Sanalar har doim obyekt bo'ladi
* Arifmetikalar har doim obyekt bo'ladi
* RegExp har doim obyekt bo'ladi
* Massivlar har doim obyekt bo'ladi
* Funktsiyalar har doim obyekt bo'ladi
* Obyektlar har doim obyekt bo'ladi

Primitivlar qiymatlardan tashqari barcha qiymatlar obyektlardir.

### Primitivlar

Primitiv qiymat - bu hech qanday xususiyat yoki metodga ega bo'lmagan qiymatdir.

3.14 - primitiv qiymat

Primitiv ma'lumot turi - primitiv qiymatga ega bo'lgan ma'lumotlar hisoblanadi.

JavaScript 7 turdagi primitv ma'lumot turlarini o'z ichiga oladi:

### Misollar

* `string`
* `number`
* `boolean`
* `null`
* `undefined`
* `symbol`
* `bigint`

{% hint style="warning" %}
### O'zgarmas

Primitiv qiymatlar o'zgarmas hisoblanadi (ular kuchli kodlashtirilgan va o'zgartirilmaydi).

agar x = 3.14 bo'lsa, siz x qiymatini o'zgartirishingiz mumkin, lekin siz 3.14 qiymatini o'zgartira olmaysiz.
{% endhint %}

| Qiymat    | Turi          | Izoh                         |
| --------- | ------------- | ---------------------------- |
| "Salom"   | String        | "Salom" har doim "Salom"     |
| 3.14      | Number        | 3.14 har doim 3.14           |
| true      | Boolean       | true har doim true           |
| false     | Boolean       | false har doim false         |
| null      | null (obyekt) | null har doim null           |
| undefined | undefined     | undefined har doim undefined |

### Obyektlar o'zgaruvchilardir

JavaScript o'zgaruvchilari bitta qiymatni o'z ichiga olishi mumkin:

```
let person = "John Doe";
```

JavaScript o'zgaruvchilari ko'p qiymatlarni ham o'z ichiga olishi mumkin.

Obyektlar ham o'zgaruvchilar hisoblanadi. Lekin obyektlar juda ko'p qiymatlarni o'z ichiga olishi mumkin.

Obyekt qiymatlari nom :qiymat juftligi sifatida yoiladi (nom va qiymat ikki nuqta bilan ajratilgan).

```
let person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

{% hint style="warning" %}
**JavaScript obyekti -** bu nomga ega qiymatlar to'plamidir
{% endhint %}

Obyektlarni `const` kalit so'zi bilan e'lon qilish odatiy holga aylangan.

```
const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

### Obyekt xususiyatlari

JavaScript obyektlarida nomga ega qiymatlar **xususiyatlar** deyiladi.

| Xususiyat | Qiymat |
| --------- | ------ |
| firstName | Jon    |
| lastName  | Doe    |
| age       | 50     |
| eyeColor  | ko'k   |

Obyektlardagi nom qiymat jufligi mana bularga o'xshab yoiladi:

* PHP dagi assotsiativ massivlarga
* Python tilidagi lug'atlarga
* C tilidagi xesh jadvallariga
* Java-da xash xaritalarga
* Ruby va Perl tillarida xeshlarga

### Obyekt metodlari

Metodlar - bu obyektlar ustida amalga oshiriladigan **harakat**lardir**.**

Obyekt xususiyatlari primitiv qiymat ham, boshqa obyekt ham va funktsiya ham bo'la oladi.

Obyekt metodi **- bu funksiya vazifasini** o'z ichiga olgan obyekt xususiyati hisoblanadi.

| Xususiyat | Qiymat                                                    |
| --------- | --------------------------------------------------------- |
| firstName | Jon                                                       |
| lastName  | Doe                                                       |
| age       | 50                                                        |
| eyeColor  | ko'k                                                      |
| fullName  | function() {return this.firstName + " " + this.lastName;} |

{% hint style="warning" %}
JavaScript obyektlari xususiyatlar va metodlar deb ataladigan nomli qiymatlar uchun konteyner hisoblanadi.
{% endhint %}

Keyingi bo'limlarda metodlar haqida batafsil bilib olasiz.

### JavaScript obyektini yaratish

JavaScript yordamida siz o'zingizning obyektlaringizni ifodalashingiz va yaratishingiz mumkin.

Yangi obyekt yaratishning turli usullari mavjud:

* Obyekt literalidan foydalanib, birgina obyekt yaratish.
* `new` kalit so'zi bilan bir obyekt yaratish.
* Obyekt constructorini berish va keyin constructor turidagi obyektlarni yaratish.
* `Object.create()`dan foydalanib obyekt yaratish.

### Obyekt literalidan foydalanish

Bu obyekt yaratishning eng oson usuli.

Obyekt literalidan foydalanib, bitta steytmentda obyektni ifodalaysiz va yaratasiz.

Obyekt literali jingalak qavslar `{}` ichidagi nom:qiymat juftlik (masalan, yosh:50) ro'yxatidir.

Quyidagi misol to'rtta xususiyatga ega yangi obyekt yaratadi:

```
const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

Bo'sh joylarni va qatorlarni ajratish muhim emas. Obyekt bir nechta qatorlarni qamrab olishi mumkin:

```
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

Ushbu misoldagi kod bo'sh obyekt yaratadi va keyin 4 ta xususiyat qo'shadi:

```
const person = {};
person.firstName = "John";
person.lastName = "Doe";
person.age = 50;
person.eyeColor = "blue";
```

### new kalit so'zidan foydalanish

Quyidagi misolda `new Object()` yordamida yangi obyekt yaratiladi va keyin 4 ta xususiyat qo'shiladi:

```
const person = new Object();
person.firstName = "John";
person.lastName = "Doe";
person.age = 50;
person.eyeColor = "blue";Yuqoridagi misollar xuddi shunday qiladi.
```

{% hint style="warning" %}
Yuqoridagi misollar ham xuddi shunday qiladi.

Lekin `new Object()`dan foydalanishga hojat yo'q.

O'qishga oson, sodda va bajarilish tezligi yaxshi bo'lishi uchun obyektning literal usulidan foydalaning.
{% endhint %}

### JavaScript obyektlari o'zgaruvchandir

Obyektlar o'zgaruvchandir: ular qiymat bo'yicha emas, balki mos havola bo'yicha murojaat qilinadi.

Agar person obyekt bo'lsa, quyidagi steytment personning nusxasini yaratmaydi:

```
const x = person;  // Will not create a copy of person.
```

X obyekti personning **nusxasi** emas**.** Bu personning o'zi. X ham, person ham bir xil obyektdir.

X ga har qanday kiritilgan o'zgarishlar personni ham o'zgartiradi, chunki x va person bir xil obyekt hisoblanadi.

```
const person = {
  firstName:"John",
  lastName:"Doe",
  age:50, eyeColor:"blue"
}

const x = person;
x.age = 10;      // Will change both x.age and person.age
```
