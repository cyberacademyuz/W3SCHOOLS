# JS Promiselar

{% hint style="success" %}
_"Men natijaga va'da beraman!"_

"Kod ishlab chiqarish" - bu biroz vaqt talab qilishi mumkin bo'lgan kod

"Kodni iste'mol qilish" - natijani kutish kerak bo'lgan kod

Promise - bu kod ishlab chiqarish va iste'mol qilish bilan bog'laydigan JavaScript obyektidir
{% endhint %}

### Promise obyekti

Promise obyekti ishlab chiqaruvchi kodni ham, iste'molchi kodga callbacklarni ham o'z ichiga oladi:

{% code title="Promise sintaksisi" %}
```
let myPromise = new Promise(function(myResolve, myReject) {
// "Producing Code" (May take some time)

  myResolve(); // when successful
  myReject();  // when error
});

// "Consuming Code" (Must wait for a fulfilled Promise)
myPromise.then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
```
{% endcode %}

Ishlab chiqaruvchi kod natijani olganida, u ikkita callbackdan birini chaqirishi kerak:

| Natija         | Chaqirish                 |
| -------------- | ------------------------- |
| Muvaffaqiyatli | myResolve(natija qiymati) |
| Xatolik        | myReject(xato obyekti)    |

### Promise obyekt xususiyatlari

Promise obyektida quyidagilar bo'lishi mumkin:

* Pending
* Fullfilled
* Rejected

Promise obyekti ikkita xususiyatni qo'llab-quvvatlaydi: state va result.

Promise obyekti "pending" bo'lsa-da, natija undefined bo'ladi.

Promise obyekti "fulfilled" bo'lsa, natija qiymat bo'ladi.

Promise obyekti "rejected" bo'lsa, natija xato obyekti bo'ladi.

| myPromise.state | myPromise.result |
| --------------- | ---------------- |
| "pending"       | undefined        |
| "fulfilled"     | natija qiymati   |
| "rejected"      | xato obyekti     |

{% hint style="warning" %}
Promisening state va result xususiyatlariga murojaat qila olmaysiz.

Promiselarni bajarish uchun Promise metodidan foydalanishingiz kerak.
{% endhint %}

### Promisedan qanday foydalaniladi

Promisedan qanday foydalanish kerak:

```
myPromise.then(
  function(value) { /* code if successful */ },
  function(error) { /* code if some error */ }
);
```

{% hint style="warning" %}
Promise.then() ikkita argumentni oladi, birinchisi muvaffaqqiyatli bajarilgan kod uchun, ikkinchisi esa muvaffaqiyatsiz bajarilgan kod uchun callbackni.

Ikkalasi ham ixtiyoriy, shuning uchun hohlasangi faqat muvaffaqiyatli bajarilgan kod uchun yoki muvaffaqiyatsiz bajarilgan kod uchun callbackni qo'shishingiz mumkin.
{% endhint %}

```
function myDisplayer(some) {
  document.getElementById("demo").innerHTML = some;
}

let myPromise = new Promise(function(myResolve, myReject) {
  let x = 0;

// The producing code (this may take some time)

  if (x == 0) {
    myResolve("OK");
  } else {
    myReject("Error");
  }
});

myPromise.then(
  function(value) {myDisplayer(value);},
  function(error) {myDisplayer(error);}
);
```

### Promisega misollar

Promiselardan foydalanishni ko'rsatish uchun biz oldingi bo'limdagi callback misollaridan foydalanamiz:

* Promise tugashi kutilmoqda
* Fayl kutilmoqda

### Vaqt tugashini kutish

#### Callbackdan foydalanishga misol

```
setTimeout(function() { myFunction("I love You !!!"); }, 3000);

function myFunction(value) {
  document.getElementById("demo").innerHTML = value;
}
```

#### Promisedan foydalanishga misol

```
let myPromise = new Promise(function(myResolve, myReject) {
  setTimeout(function() { myResolve("I love You !!"); }, 3000);
});

myPromise.then(function(value) {
  document.getElementById("demo").innerHTML = value;
});
```

### Fayl kutilmoqda

#### Callbackdan foydalanishga misol

```
function getFile(myCallback) {
  let req = new XMLHttpRequest();
  req.open('GET', "mycar.html");
  req.onload = function() {
    if (req.status == 200) {
      myCallback(req.responseText);
    } else {
      myCallback("Error: " + req.status);
    }
  }
  req.send();
}

getFile(myDisplayer);
```

#### Promise-dan foydalanishga misol

```
let myPromise = new Promise(function(myResolve, myReject) {
  let req = new XMLHttpRequest();
  req.open('GET', "mycar.htm");
  req.onload = function() {
    if (req.status == 200) {
      myResolve(req.response);
    } else {
      myReject("File not Found");
    }
  };
  req.send();
});

myPromise.then(
  function(value) {myDisplayer(value);},
  function(error) {myDisplayer(error);}
);
```

### Brauzerni qo'llab-quvvatlashi

ES6 Promise obyektini taqdim qildi.

Quyidagi jadvalda Promise obyektlarini to'liq qo'llab-quvvatlaydigan brauzerning boshlang'ich versiyasi ko'rsatilgan:

| Chrom     | Edge      | Firefox    | Safari     | Opera     |
| --------- | --------- | ---------- | ---------- | --------- |
| Chrome 33 | Edge 12   | Firefox 29 | Safari 7.1 | Opera 20  |
| Feb, 2014 | Jul, 2015 | Apr, 2014  | Sep, 2014  | Mar, 2014 |
