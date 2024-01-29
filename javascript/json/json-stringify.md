# JSON Stringify

Veb-server bilan ma'lumot almashish JSON-dan foydalanishning keng tarqalgan usuli hisoblanadi.

Veb-serverga ma'lumotlarni yuborishda ma'lumotlar doimo string bo'lishi kerak.

Obyektni `JSON.stringify()` yordamida stringga aylantiring.

### JavaScript obyektini stringga o'tkazish

Tasavvur qiling-a, JavaScriptimiz-da ushbu obyekt bor:

```
const obj = {name: "John", age: 30, city: "New York"};
```

Uni stringga aylantirish uchun `JSON.stringify()` funksiyasidan foydalaning.

```
const myJSON = JSON.stringify(obj);
```

{% hint style="warning" %}
Natijada JSON notatsiyasidan keyingi string bo'ladi.
{% endhint %}

`myJSON` endi string va serverga yuborilishga tayyor:

```
const obj = {name: "John", age: 30, city: "New York"};
const myJSON = JSON.stringify(obj);
```

JSONni serverga qanday yuborishni keyingi bo'limlarda bilib olasiz.

### JavaScript massivini stringga o'tkazish

JavaScript massivlarini stringifikatsiya qilish ham mumkin:

Tasavvur qiling, JavaScriptimizda ushbu massiv bor:

```
const arr = ["John", "Peter", "Sally", "Jane"];
```

Uni stringga aylantirish uchun `JSON.stringify()` funksiyasidan foydalaning.

```
const myJSON = JSON.stringify(arr);
```

{% hint style="warning" %}
Natija JSON notatsiyasidan keyingi string bo'ladi.
{% endhint %}

`myJSON` endi string va serverga yuborilishga tayyor:

```
const arr = ["John", "Peter", "Sally", "Jane"];
const myJSON = JSON.stringify(arr);
```

JSON stringini serverga qanday yuborishni keyingi bo'limlarda bilib olasiz.

### Ma'lumotlarni saqlash

Ma'lumotlarni saqlashda ma'lumotlar ma'lum bir formatda bo'lishi kerak va uni qayerda saqlashni tanlashingizdan qat'iy nazar, _matn_ har doim to'g'ri formatlardan biri bo'ladi.

JSON obyektlarni matn sifatida saqlash imkonini beradi.

{% code title="Mahalliy xotirada ma'lumotlarni saqlash" %}
```
// Storing data:
const myObj = {name: "John", age: 31, city: "New York"};
const myJSON = JSON.stringify(myObj);
localStorage.setItem("testJSON", myJSON);

// Retrieving data:
let text = localStorage.getItem("testJSON");
let obj = JSON.parse(text);
document.getElementById("demo").innerHTML = obj.name;
```
{% endcode %}

### Istisnolar

#### Sanalarni stringga o'tkazish

JSONda date obyektlariga ruxsat berilmaydi. `JSON.stringify()` funktsiyasi har qanday sanani stringga aylantiradi.

```
const obj = {name: "John", today: new Date(), city : "New York"};
const myJSON = JSON.stringify(obj);
```

Siz stringni qabul qiluvchida sanani obyektga aylantirishingiz mumkin.

#### Funktsiyalarni stringga aylantirish

JSON-da funksiyalarga oobekt qiymatlari sifatida ruxsat berilmaydi.

`JSON.stringify()` funksiyasi obyektdan barcha funksiyalarni, kalitni ham, qiymatni ham olib tashlaydi:

```
const obj = {name: "John", age: function () {return 30;}, city: "New York"};
const myJSON = JSON.stringify(obj);
```

`JSON.stringify()` funksiyasini ishga tushirishdan oldin funksiyalaringizni stringga aylantirsangiz, buni oldini olishingiz mumkin.

```
const obj = {name: "John", age: function () {return 30;}, city: "New York"};
obj.age = obj.age.toString();
const myJSON = JSON.stringify(obj);
```

{% hint style="danger" %}
Agar JSON yordamida funksiyalar yuborsangiz, funksiyalar o‘z qamrovini yo‘qotadi va qabul qiluvchi ularni yana funksiyalarga aylantirish uchun `eval()`dan foydalanishi kerak bo‘ladi.
{% endhint %}
