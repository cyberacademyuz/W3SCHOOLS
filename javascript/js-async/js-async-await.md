# JS Async/Await

{% hint style="success" %}
_"Async va await promiselarni yozishni osonlashtiradi"_

async funksiyani promise qaytarishiga majbur qiladi

await funksiyani promise kutishiga majbur qiladi
{% endhint %}

### Async sintaksisi

Funksiya oldidagi `async` kalit so'zi funksiyani promise qaytarishga majbur qiladi:

```
async function myFunction() {
  return "Hello";
}
```

Xuddi bunday:

```
function myFunction() {
  return Promise.resolve("Hello");
}
```

Promisedan qanday foydalanish kerak:

```
myFunction().then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
```

```
async function myFunction() {
  return "Hello";
}
myFunction().then(
  function(value) {myDisplayer(value);},
  function(error) {myDisplayer(error);}
);
```

Yoki soddaroq, chunki normal qiymat kutyapsiz (xatolik emas):

```
async function myFunction() {
  return "Hello";
}
myFunction().then(
  function(value) {myDisplayer(value);}
);
```

### Await sintaksisi

`await` kalit so'zi faqat `async` funksiyasining ichida ishlatilishi mumkin.

`await` kalit so'zi funksiyani bajarishni to'xtatib turishga va davom etishdan oldin bajarilgan promiseni kutishga majbur qiladi:

```
let value = await promise;
```

## Misol

Keling, asta-sekin boramiz va undan qanday foydalanishni o'rganamiz.

#### Boshlang'ich sintaksis

```
async function myDisplay() {
  let myPromise = new Promise(function(resolve, reject) {
    resolve("I love You !!");
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

myDisplay();
```

{% hint style="warning" %}
Ikki argument (resolve va reject) JavaScript tomonidan built-in sifatida belgilangan.

Biz ularni yaratmaymiz, lekin bajaruvchi funksiya tayyor bo'lganda ulardan birini chaqiramiz.

Ko'pincha bizga reject funktsiyasi kerak bo'lmaydi.
{% endhint %}

#### Rejectsiz misol

```
async function myDisplay() {
  let myPromise = new Promise(function(resolve) {
    resolve("I love You !!");
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

myDisplay();
```

#### Vaqt tugashini kutish

```
async function myDisplay() {
  let myPromise = new Promise(function(resolve) {
    setTimeout(function() {resolve("I love You !!");}, 3000);
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

myDisplay();
```

#### Fayl kutilmoqda

```
async function getFile() {
  let myPromise = new Promise(function(resolve) {
    let req = new XMLHttpRequest();
    req.open('GET', "mycar.html");
    req.onload = function() {
      if (req.status == 200) {
        resolve(req.response);
      } else {
        resolve("File not Found");
      }
    };
    req.send();
  });
  document.getElementById("demo").innerHTML = await myPromise;
}

getFile();
```

### Brauzerni qo'llab-quvvatlashi

ECMAScript 2017 `async` va `await` kalit so'zlarini taqdim qildi.

Quyidagi jadvalda ikkalasini ham to'liq qo'llab-quvvatlaydigan birinchi brauzer versiyasi ko'rsatilgan:

| Chrome    | Edge      | Firefox    | Safari    | Opera     |
| --------- | --------- | ---------- | --------- | --------- |
| Chrome 55 | Edge 15   | Firefox 52 | Safari 11 | Opera 42  |
| Dec, 2016 | Apr, 2017 | Mar, 2017  | Sep, 2017 | Dec, 2016 |
