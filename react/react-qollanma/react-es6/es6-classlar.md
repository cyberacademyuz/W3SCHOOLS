# ES6 Classlar

### Classlar

ES6 classlarni taqdim qildi.

Class - bu funksiya turi, lekin uni ishlatish uchun `function` kalit so'zidan foydalanish o'rniga `class` kalit so'zidan foydalanamiz va xususiyatlar `constructor()` metodi ichida tayinlanadi.

{% code title="Oddiy class konstruktori:" %}
```jsx
class Car {
  constructor(name) {
    this.brand = name;
  }
}
```
{% endcode %}

{% hint style="warning" %}
Class nomining katta harf bilan boshlanishiga e'tibor bering. Biz "Car" nomini bosh harf bilan boshladik. Bu classlarni nomlash uchun standart konventsiya hisoblanadi.
{% endhint %}

Endi Car classidan foydalanib obyektlar yaratishingiz mumkin:

{% code title="Car classi asosida "mycar" deb nomlangan obyekt yarating:" %}
```jsx
class Car {
  constructor(name) {
    this.brand = name;
  }
}

const mycar = new Car("Ford");
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Obyekt ishga tushirilganda konstruktor funksiya avtomatik tarzda chaqiriladi.
{% endhint %}

## Classlarda metoddan foydalanish

O'z metodlaringizni classga qo'shishingiz mumkin:

"present" nomli metod yarating:

```jsx
class Car {
  constructor(name) {
    this.brand = name;
  }
  
  present() {
    return 'I have a ' + this.brand;
  }
}

const mycar = new Car("Ford");
mycar.present();
```

Yuqoridagi misolda ko'rib turganingizdek, obyektning metod nomidan keyin qavslar (parametrlar qavs ichiga kiradi) orqali metodni chaqirasiz.

### Classni meroslash

Class meroslash uchun `extends` kalit so'zidan foydalaning.

Classni meroslash orqali yaratilgan class boshqa classdan barcha metdolarni meros qilib oladi:

{% code title=""Car" classidan metodlarni meros qilib oladigan "Model" nomli class yarating:" %}
```jsx
class Car {
  constructor(name) {
    this.brand = name;
  }

  present() {
    return 'I have a ' + this.brand;
  }
}

class Model extends Car {
  constructor(name, mod) {
    super(name);
    this.model = mod;
  }  
  show() {
      return this.present() + ', it is a ' + this.model
  }
}
const mycar = new Model("Ford", "Mustang");
mycar.show();
```
{% endcode %}

`super()` metodi parent classni bildiradi.

Konstruktor metodda `super()` metodini chaqirish orqali parent classning konstruktor metodini chaqiramiz va parent classining xususiyatlari va metodlariga murojaat qilish huquqiga ega bo'lamiz.

Classlar haqida ko'proq ma'lumot olish uchun JavaScript classlari bo'limimizni ko'rib chiqing.
