# Classdan meros olish (inheritance)

### Class meros olish

Class merosini yaratish uchun `extends` kalit so'zidan foydalaning.

Class merosi bilan yaratilgan class boshqa classdan barcha metodlarni meros qilib oladi:

{% code title=""Car" classidan metodlarni meros qilib oladigan "Model" nomli class yarating:" %}
```javascript
class Car {
  constructor(brand) {
    this.carname = brand;
  }
  present() {
    return 'I have a ' + this.carname;
  }
}

class Model extends Car {
  constructor(brand, mod) {
    super(brand);
    this.model = mod;
  }
  show() {
    return this.present() + ', it is a ' + this.model;
  }
}

let myCar = new Model("Ford", "Mustang");
document.getElementById("demo").innerHTML = myCar.show();
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_classes_inherit" %}

`super()` metodi ota-klassga tegishli.

Konstruktor metodida `super()` metodini chaqirish orqali biz ota-onaning konstruktor metodini chaqiramiz va ota-onaning xossalari va metodlariga murojaat qilish huquqiga ega bo'lamiz.

{% hint style="warning" %}
Meroslash kodni qayta ishlatish uchun foydalidir: yangi sinf yaratishda mavjud sinfning xususiyatlari va usullarini qayta ishlating.
{% endhint %}

### Getterlar va setterlar

Classlar, getterlar va setterlardan foydalanishga imkon beradi.

Xususiyatlaringiz uchun getter va setterlardan foydalanish oqilona ish bo'lishi mumkin, ayniqsa ayniqsa uni return qilishdan yoki sozlashdan oldin qiymat bilan biror narsa qilishni xohlasangiz.

Classga getter va setterlarni qo'shish uchun `get` va `set` kalit so'zlaridan foydalaning.

```javascript
"Carname" xususiyati uchun oluvchi va sozlagich yarating:

class Car {
  constructor(brand) {
    this.carname = brand;
  }
  get cnam() {
    return this.carname;
  }
  set cnam(x) {
    this.carname = x;
  }
}

const myCar = new Car("Ford");

document.getElementById("demo").innerHTML = myCar.cnam;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_classes_getters" %}

{% hint style="warning" %}
**Eslatma:** agar getter metod bo'lsa ham, xususiyat qiymatini olishni xohlaganingizda qavslardan foydalanmaysiz.
{% endhint %}

Getter/setter metodining nomi xususiyat nomi bilan bir xil bo'lishi kerak emas, bu holatda `carname`.

Ko'pgina dasturchilar getter/setterni haqiqiy xususiyatdan ajratish uchun xususiyat nomidan oldin pastki chiziq `_` belgisidan foydalanadilar:

{% code title=" Getter/setterni haqiqiy xususiyatdan ajratish uchun pastki chiziq belgisidan foydalanishingiz mumkin:" %}
```javascript
class Car {
  constructor(brand) {
    this._carname = brand;
  }
  get carname() {
    return this._carname;
  }
  set carname(x) {
    this._carname = x;
  }
}

const myCar = new Car("Ford");

document.getElementById("demo").innerHTML = myCar.carname;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_classes_getters2" %}

_Setterdan_ foydalanish uchun, qavslarsiz xususiyat qiymatini o'rnatganingizdek bir xil sintaksisdan foydalaning:

{% code title="Car nomini "Volvo" ga o'zgartirish uchun setterdan foydalaning:" %}
```javascript
class Car {
    constructor(brand) {
    this._carname = brand;
  }
  get carname() {
    return this._carname;
  }
  set carname(x) {
    this._carname = x;
  }
}

const myCar = new Car("Ford");
myCar.carname = "Volvo";
document.getElementById("demo").innerHTML = myCar.carname;
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_classes_setter" %}

### Hoisting

Funktsiyalar va boshqa deklaratsiyalardan farqli o'laroq, class deklaratsiyasi hoisting.

Ya'ni, classdan foydalanishdan avval uni e'lon qilishingiz kerak:

```javascript
//You cannot use the class yet.
//myCar = new Car("Ford") will raise an error.

class Car {
  constructor(brand) {
    this.carname = brand;
  }
}

//Now you can use the class:
const myCar = new Car("Ford")
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_classes_hoisting" %}

{% hint style="warning" %}
**Eslatma:** Funktsiyalar kabi boshqa deklaratsiyalarda uni e'lon qilinishidan oldin ishlatmoqchi bo'lganingizda xatolik olmaysiz, chunki deklaratsiyalarning standart xatti-harakati hoisting bo'ladi.
{% endhint %}
