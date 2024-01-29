# Class Static

{% hint style="success" %}
Statik class metodlari classning o'zida yaratiladi.

Obyektda `static` metodni chaqira olmaysiz , uni faqat obyekt classida chaqirishingi mumkin.
{% endhint %}

```javascript
class Car {
  constructor(name) {
    this.name = name;
  }
  static hello() {
    return "Hello!!";
  }
}

const myCar = new Car("Ford");

// You can call 'hello()' on the Car Class:
document.getElementById("demo").innerHTML = Car.hello();

// But NOT on a Car Object:
// document.getElementById("demo").innerHTML = myCar.hello();
// this will raise an error.
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_class_static" %}

Agar siz `myCar` obyektini `static` metod ichida ishlatmoqchi bo'lsangiz, uni parametr sifatida yuborishingiz mumkin:

```javascript
class Car {
  constructor(name) {
    this.name = name;
  }
  static hello(x) {
    return "Hello " + x.name;
  }
}
const myCar = new Car("Ford");
document.getElementById("demo").innerHTML = Car.hello(myCar);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_class_static2" %}
