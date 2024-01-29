# Obyektlar

## Obyektlarga, ularning xususiyatlari va metodlariga haqiqiy hayotdan misol

Haqiqiy hayotda mashina bir obyekt.

Mashina esa og'irlik va rang kabi xususiyatlarga ega, ishga tushishi va to'xtashi esa uning metodlari hisoblanadi.

| Obyekt                                                | Xususiyatlari                                                                                        | Metodlari                                                                      |
| ----------------------------------------------------- | ---------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------ |
| ![](https://www.w3schools.com/js/objectExplained.gif) | <p><br>car.name = Fiat<br><br>car.model = 500<br><br>car.weight = 850kg<br><br>car.color = white</p> | <p><br>car.start()<br><br>car.drive()<br><br>car.brake()<br><br>car.stop()</p> |

Barcha avtomobillar bir xil **xususiyatlarga** ega, ammo **metod qiymatlari** mashinaga qarab farq qiladi.

Barcha mashinalar bir xil **metodlarga** ega, ammo metodlar har xil paytda amalga oshiriladi.

### JavaScript obyektlari

O'zgaruvchilar ma'lumot qiymatlarini saqlash uchun konteyner vazifasini bajarishini bilasiz.

Ushbu kod `car` nomli o'zgaruvchiga oddiygina **Fiat** qiymatini beradi:

```javascript
let car = "Fiat";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_objects_variable" %}

Obyektlar ham o'zgaruvchilardir. Lekin obyektlar juda ko'p qiymatlarni o'z ichiga olishi mumkin.

Ushbu kod car nomli o'zgaruvchiga ko'plab qiymatlar (Fiat, 500, white) beradi:

```javascript
const car = {type:"Fiat", model:"500", color:"white"};
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_objects_object" %}

Qiymatlar **nom:qiymat** juftligi (nom va qiymat ikki nuqta bilan ajratilgan) sifatida yoziladi.

{% hint style="warning" %}
Obyektlarni `const` kalit so'zi bilan e'lon qilish odatiy hol hisoblanadi.

Obyektlar bilan `const` dan foydalanish haqida ko'proq ma'lumotga ega bo'ling: [JS Const](const.md).
{% endhint %}

### Obyekt yaratish

JavaScriptda obyektlarni obyekt literali bilan yaratasiz:

```javascript
const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_objects_object" %}

Bo'sh joylar va qatorlarni ajratish shart emas. Obyekt bir nechta qatorlardan tashkil topishi mumkin:

```javascript
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_objects_create_2" %}

### Obyekt xususiyatlari

JavaScript obyektlaridagi **nom:qiymat** ​​juftliklari **xususiyatlar** deyiladi:

| Xususiyat | Xususiyat qiymati |
| --------- | ----------------- |
| firstName | John              |
| lastName  | Doe               |
| age       | 50                |
| eyeColor  | blue              |

### Obyekt xususiyatlarini boshqarish

Obyekt xususiyatlarini ikki yo'l bilan boshqarishingiz mumkin:

```javascript
obyektNomi.xususiyatNomi
```

yoki

```
obyektNomi["xususiyatNomi"]
```

{% code title="1-misol" %}
```javascript
person.lastName;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_objects_properties_1" %}

{% code title="2-misol" %}
```javascript
person["lastName"];
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_objects_properties_2" %}

{% hint style="warning" %}
JavaScriptda obyektlar **xususiyatlar** deb ataladigan nomga ega qiymatlar uchun konteyner hisoblanadi.
{% endhint %}

### Obyekt metodlari

Obyektlar matodlarga ega bo'lishi ham mumkin.

Metodlar - bu obyektlar ustida bajarilishi mumkin bo'lgan **harakatlar.**

Metodlar obyekt xususiyatida funksiya sifatida saqlanadi.

| Xususiyat | Xususiyat qiymati                                         |
| --------- | --------------------------------------------------------- |
| firstName | John                                                      |
| lastName  | Doe                                                       |
| age       | 50                                                        |
| eyeColor  | blue                                                      |
| fullName  | function() {return this.firstName + " " + this.lastName;} |

Metod bu xususiyat sifatida saqlanadigan funksiya.

```javascript
const person = {
  firstName: "John",
  lastName : "Doe",
  id       : 5566,
  fullName : function() {
    return this.firstName + " " + this.lastName;
  }
};
```

Yuqoridagi misolda `this` **person** obyektiga murojaat qiladi.

**this.firstName this**ning **firstName** xususiyatini bildiradi.

**this.firstName person**-ning **firstName** xususiyatini bildiradi.

## &#x20;This nima ?

JavaScript-da `this` kalit so'zi obyektga murojaat qiladi.

Obyekt `this` qanday chaqirilayotganiga bog'liq.

`this` kalit so'zi qanday ishlatilishiga qarab turli obyektlarga murojaat qiladi:

| Obyekt metodida `this` obyektga murojaat qiladi.                                                       |
| ------------------------------------------------------------------------------------------------------ |
| Yakka holatdaa `this` global obyektga murojaat qiladi.                                                 |
| Funksiyada `this` global obyektga murojaat qiladi.                                                     |
| Funksiyaning strict rejimida `this` `undefined` bo'ladi.                                               |
| Hodisa sodir bo'lganda, `this` hodisani qabul qilgan elementga murojaat qiladi.                        |
| `call()`, `apply()`va `bind()` kabi metodlar har qanday obyekt uchun `this`ga murojaat qilishi mumkin. |

{% hint style="warning" %}
### Eslatma

`this` o'zgaruvchi emas. Bu kalit so'z. `this`ning qiymatini o'zgartira olmaysiz.

### Shuningdek:

[Javascriptda **this** qo'llanmasi](https://www.w3schools.com/js/js\_this.asp)
{% endhint %}

### This kalit **so'zi**

Funksiyada`this` funksiyaning "egasi" ga murojaat qiladi.

Yuqoridagi misolda `this` `fullName` funksiyasiga "egalik qiluvchi" person obyektidir.

Boshqacha qilib aytganda, `this.firstName` ushbu obyektning `firstName` xususiyatini bildiradi.

[Ushbu qo'llanmada](https://www.w3schools.com/js/js\_this.asp) `this` haqida batafsil bilib oling.

### Obyekt metodlariga murojaat qilish

Siz quyidagi sintaksis orqali obyekt metodlarini boshqara olasiz:

```
obyektNomi.metodNomi()
```

{% code title="Misol:" %}
```javascript
name = person.fullName();
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_objects_method" %}

Agar metodga () qavssiz  murojaat qilsangiz, u funksiyani qaytaradi:

```javascript
name = person.fullName;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_objects_function" %}

### Stringlarni, raqamlarni va Booleanlarni obyekt sifatida e'lon qilmang!

O'zgaruvchi "`new`" kalit so'zi bilan e'lon qilinganda, u obyekt sifatida yaratiladi:

```javascript
x = new String();        // Declares x as a String object
y = new Number();        // Declares y as a Number object
z = new Boolean();       // Declares z as a Boolean object
```

`String`, `Number` va `Boolean` obyektlaridan foydalanmang. Ular sizning kodingizni murakkablashtiradi va bajarish tezligini sekinlashtiradi.

{% hint style="warning" %}
Obyektlar haqida keyinroq batafsil bilib olasiz.
{% endhint %}
