# Array metodlari

{% hint style="success" %}
Array length                                                  Array join()

Array toString()                                             Array delete()

Array pop()                                                    Array concat()

push()                                                            Array flat()

Array shift()                                                   Array splice()

Array unshift()                                               Array slice()

Metodlar ushbu sahifada ko'rsatilgan tartibda keltirilgan.
{% endhint %}

### Array length

`length` xususiyati arrayning uzunligini qaytaradi.

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let size = fruits.length;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_length" %}

### Arraylar toString()

JavaScriptning `toString()` metodi array elementlarini arraydan stringga o'tkazadi.

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
```

Natija:

```
Banana,Orange,Apple,Mango
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_tostring" %}

`join()`  metodi esa barcha massiv elementlarini stringga birlashtiradi.

U `toString()` kabi ishlaydi, lekin qo'shimcha ravishda ajratuvchi belgi kiritishingiz mumkin:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.join(" * ");
```

Natija:

```
Banana * Orange * Apple * Mango
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_join" %}

### Olib tashlash va qo'shish

Arraylar bilan ishlaganda elementlarni olib tashlash va yangi elementlar qo'shish oson.

Popping va pushing nima:

Popping bu elementlarni arraydan olib tashlash, pushing esa array ichiga elementlar qo'shish.

### Arrayda pop()

`pop()` metodi arraydan oxirgi elementni olib tashlaydi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.pop();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_pop" %}

`pop()` metodi "olib tashlangan" qiymatni qaytaradi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits.pop();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_pop_out" %}

### Massivda push()

`push()` metodi arrayning oxiriga yangi element qo'shadi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.push("Kiwi");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_push" %}

`push()` metodi yangi massiv uzunligini qaytaradi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let length = fruits.push("Kiwi");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_push_length" %}

### Shifting elementlar

Shifting popping bilan bir xil, lekin u oxirgi element bilan emas birinchi element bilan ishlaydi.

### Arrayda shift()

`shift()` metodi arrayning birinchi elementini olib tashlaydi va qolgan barcha elementlarni kichik indexga o'tkazadi.

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.shift();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_shift" %}

`shift()` metodi "o'chirilgan" qiymatni qaytaradi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
let fruit = fruits.shift();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_shift_return" %}

### Array unshift()

`unshift()` metodi massivning boshiga yangi element qo'shadi va eski elementlarni kattaroq indexga o'tkazadi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_unshift" %}

`unshift()` metodi yangi array uzunligini qaytaradi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.unshift("Lemon");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_unshift" %}

### Elementlarni o'zgartirish

Array elementlariga ularning index raqami orqali murojaat qilsih mumkin:

{% hint style="warning" %}
Array indekslari **0** dan boshlanadi:

\[0] arrayning birinchi elementi\
\[1] ikkinchi\
\[2] uchinchi ...
{% endhint %}

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[0] = "Kiwi";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_change" %}

### Array uzunligi

`length` xususiyati arrayga yangi element qo'shishning oson yo'lini taqdim qiladi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits[fruits.length] = "Kiwi";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_change_add" %}

### Array delete()

{% hint style="danger" %}
#### Ogohlantirish!

Array elementlari JavaScriptning `delete` operatori yordamida ham o'chirilishi mumkin.

`delete`dan foydalanish Arrayda `undefined` elementlar qoldiradi

Uning o'rniga pop() yoki shift() dan foydalaning.
{% endhint %}

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
delete fruits[0];
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_delete" %}

### Arraylarni birlashtirish.

`concat()` metodi mavjud arraylarni birlashtirish orqali yangi massiv yaratadi:

{% code title="Ikki arrayni birlashtirishga misol" %}
```javascript
const myGirls = ["Cecilie", "Lone"];
const myBoys = ["Emil", "Tobias", "Linus"];

const myChildren = myGirls.concat(myBoys);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_concat" %}

{% hint style="warning" %}
`concat()` metodi mavjud arraylarni o'zgartirmaydi. U har doim yangi array qaytaradi.
{% endhint %}

`concat()` metodi har qancha argumentlar qabul qilishi mumkin:

{% code title="Uchta massivni birlashtirish" %}
```javascript
const arr1 = ["Cecilie", "Lone"];
const arr2 = ["Emil", "Tobias", "Linus"];
const arr3 = ["Robin", "Morgan"];
const myChildren = arr1.concat(arr2, arr3);
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_concat2" %}

`concat()` metodi argument sifatida stringlarni  ham qabul qilishi mumkin:

{% code title="Massivni qiymatlar bilan birlashtirish" %}
```javascript
const arr1 = ["Emil", "Tobias", "Linus"];
const myChildren = arr1.concat("Peter"); 
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_concat3" %}

### Arraylarni bitta qilib yuborish (Flattening)

Massivlarni tekislab yuborish deb massivning o'lchamini kamaytirish jarayoniga aytiladi.

`flat()` metodi ichma ich tuzilgan ma'lum bir ichki elementlar bilan yangi massiv yaratadi.

```javascript
const myArr = [[1,2],[3,4],[5,6]];
const newArr = myArr.flat(); 
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_flat" %}

### Brauzerning qo'llab quvvatlashi

`flat()` 2020-yil Yanvar oyidan boshlab barcha zamonaviy brauzerlarda qo'llab quvvatlanadi:

| Chrome 69 | Edge 79  | Firefox 62 | Safari 12 | Opera 56 |
| --------- | -------- | ---------- | --------- | -------- |
| Sep 2018  | Jan 2020 | Sep 2018   | Sep 2018  | Sep 2018 |

### Birlashtirish va kesish massivlari

`splice()` metodi arrayga yangi elementlar qo'shadi.

`slice()` metodi arrayning bir qismini ajratib oladi.

### Array splice()

`splice()` metodi arrayga yangi elementlar qo'shish uchun ishlatilishi mumkin:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 0, "Lemon", "Kiwi");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_splice" %}

Birinchi parametr (2) yangi element qo'shilishi kerak bo'lgan joyni belgilaydi.

Ikkinchi parametr (0) yangi qo'shilgan element ohiridan nechta elementni olib tashlash kerakligini belgilaydi.

Qolgan parametrlar ("Limon", "Kivi") qo'shiladigan yangi elementlarni belgilaydi.

`splice()` metodi o'chirilgan elementlar bilan massiv qaytaradi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(2, 2, "Lemon", "Kiwi");
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_splice_return" %}

### Elementlarni olib tashlash uchun splice() dan foydalaning

Parametrlarni oqilona sozlash orqali elementlarni arrayda "undefined" element qoldirmasdan olib tashlash uchun `splice()` dan foydalanishingiz mumkin:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
fruits.splice(0, 1);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_remove" %}

Birinchi parametr (0) yangi element qo'shilishi kerak bo'lgan joyni belgilaydi.

Ikkinchi parametr (1) nechta elementni olib tashlash kerakligini belgilaydi.

Boshqa parametrlar kiritilmaydi. Hech qanday yangi elementlar qo'shilmaydi.

### Arrayda slice()

`slice()` metodi arrayning bir qismini yangi arrayga ajratadi.

Ushbu misolda arrayni 1-elementi ("Orange")dan boshlanadigan qismini ajratib olish ko'rsatilgan.

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_slice1" %}

{% hint style="warning" %}
### Eslatma

`slice()` metodi yangi massiv yaratadi.

`slice()` metodi asl massivdan hech qanday elementni olib tashlamaydi.
{% endhint %}

Ushbu misolda massivning 3-elementi ("Apple")dan boshlanadigan qismini ajratib olish ko'rsatilgan.

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(3);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_slice3" %}

`slice()` metodi `slice(1, 3)` kabi ikkita argumentni qabul qilishi mumkin.

Keyin u elementlarni kiritilgan 1-argumentdan 2-argumentgacha bo'lgan oraliqdagi elementlarni tanlaydi.

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(1, 3);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_slice" %}

Agar birinchi misoldagi kabi 2-argument berilmasa, `slice()` metodining qolgan qismini ajratadi.

```javascript
const fruits = ["Banana", "Orange", "Lemon", "Apple", "Mango"];
const citrus = fruits.slice(2);
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_slice2" %}

### Avtomatik toString()

Agar primitiv qiymat kutilgan bo'lsa, JavaScript arrayni avtomatik tarzda vergul bilan ajratilgan stringga aylantiradi.

Bu har doim arrayni chiqarishga harakat qilganingizda shunday bo'ladi.

Ushbu ikki misol bir xil natijani qaytaradi:

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits.toString();
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_tostring" %}

```javascript
const fruits = ["Banana", "Orange", "Apple", "Mango"];
document.getElementById("demo").innerHTML = fruits;
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_array_automatic" %}

{% hint style="warning" %}
### Eslatma

Barcha obyektlarda `toString()` metodi mavjud.
{% endhint %}

### Arrayda eng katta va eng kichik qiymatlarni topish

Arrayda eng kata yoki eng kichik qiymatni topish uchun belgilangan funksiyalar yo'q.

Bu muammoni qanday qilib hal qilishni keyingi bo'limda bilib olasiz.

### Massivlarni saralash

Massivlari saralash keyingi bo'limda ko'rib chiqiladi.

{% hint style="warning" %}
### Massiv haqida to'liq ma'lumotnoma

Massiv haqida to'liq ma'lumotnomani ko'rish uchun bizning quyidagi sahifamizga o'ting:

[JavaScriptda massiv haqida to'liq ma'lumotnoma.](https://www.w3schools.com/jsref/jsref\_obj\_array.asp)

Ma'lumotnomada massivning barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
