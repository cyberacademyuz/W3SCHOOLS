# ES6 Destructuring

## Destructuring

Destructuringni tasvirlab berish uchun sendvich qilamiz. Sendvichni tayyorlash uchun muzlatgichdan hamma narsani olasizmi ? Yo'q, siz faqat sendvichingizda ishlatmoqchi bo'lgan mahsulotlarnigina olasiz holos.

Destructuring ham huddi shu. Ya'ni kodimizda ishlayotgan array yoki obyekt bo'lishi mumkin, lekin bizga faqat ulardagi ba'zi elementlargina kerak.

Destructuring faqat kerakli narsani olishni osonlashtiradi.

### Arraylarda destructuring&#x20;

O'zgaruvchiga array elementlarini tayinlashning eski usuli:

{% code title="Oldin:" %}
```jsx
const vehicles = ['mustang', 'f-150', 'expedition'];

// old way
const car = vehicles[0];
const truck = vehicles[1];
const suv = vehicles[2];
```
{% endcode %}

O'zgaruvchiga array elementlarini tayinlashning yangi usuli:

{% code title="Desttructing orqali:" %}
```jsx
const vehicles = ['mustang', 'f-150', 'expedition'];

const [car, truck, suv] = vehicles;
```
{% endcode %}

{% hint style="warning" %}
Arraylarni destruksiyalashda o‘zgaruvchilarni e’lon qilish tartibi muhim ahamiyatga ega.
{% endhint %}

Agar bizga faqat car va suv o'zgaruvchisi kerak bo'lsa, shunchaki truck o'zgaruvchisni yozmay, vergul qo'yib ketishimiz mumkin:

```jsx
const vehicles = ['mustang', 'f-150', 'expedition'];

const [car,, suv] = vehicles;
```

Funksiya array qaytarganida destructuring foydali bo'ladi:

```jsx
function calculate(a, b) {
  const add = a + b;
  const subtract = a - b;
  const multiply = a * b;
  const divide = a / b;

  return [add, subtract, multiply, divide];
}

const [add, subtract, multiply, divide] = calculate(4, 7);
```

### Obektlarda destructuring

Funksiya ichidagi obyektdan foydalanishning eski usuli:

{% code title="Oldin:" %}
```jsx
const vehicleOne = {
  brand: 'Ford',
  model: 'Mustang',
  type: 'car',
  year: 2021, 
  color: 'red'
}

myVehicle(vehicleOne);

// old way
function myVehicle(vehicle) {
  const message = 'My ' + vehicle.type + ' is a ' + vehicle.color + ' ' + vehicle.brand + ' ' + vehicle.model + '.';
}
```
{% endcode %}

Funksiya ichidagi obyektdan foydalanishning yangi usuli:

{% code title="Destructuring orqali:" %}
```jsx
const vehicleOne = {
  brand: 'Ford',
  model: 'Mustang',
  type: 'car',
  year: 2021, 
  color: 'red'
}

myVehicle(vehicleOne);

function myVehicle({type, color, brand, model}) {
  const message = 'My ' + type + ' is a ' + color + ' ' + brand + ' ' + model + '.';
}
```
{% endcode %}

E'tibor bering, obyekt xususiyatlari ma'lum bir tartibda e'lon qilinishi shart emas.

Biz hatto ichki obyektga murojaat qilib, undan kerakli elementlarni qayta desturct qilish uchun ikki nuqta va qavslar yordamida ichki joylashtirilgan obyektlarni destruct qilishimiz mumkin:

```jsx
const vehicleOne = {
  brand: 'Ford',
  model: 'Mustang',
  type: 'car',
  year: 2021, 
  color: 'red',
  registration: {
    city: 'Houston',
    state: 'Texas',
    country: 'USA'
  }
}

myVehicle(vehicleOne)

function myVehicle({ model, registration: { state } }) {
  const message = 'My ' + model + ' is registered in ' + state + '.';
}
```
