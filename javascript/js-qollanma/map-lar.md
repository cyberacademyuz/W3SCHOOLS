# Map-lar

{% hint style="success" %}
Map kalit-qiymat juftligini o'z ichiga oladi, undagi kalitlar har qanday turdagi ma'lumot turi bo'lishi mumkin.

Map keylarning haqiqiy tartibini eslab qoladi.
{% endhint %}

### Asosiy xarita usullari

| Metod      | Ta'rif                                                           |
| ---------- | ---------------------------------------------------------------- |
| new Map()  | Yangi Map yaratadi                                               |
| set()      | Xaritadagi kalit uchun qiymat beradi                             |
| get()      | Xaritadagi kalit uchun qiymat oladi                              |
| delete()   | Kalit tomonidan belgilangan Map elementini olib tashlaydi        |
| has()      | Map kalit mavjud bo'lsa, true qiymatini qaytaradi                |
| forEach()  | Mapdagi har bir kalit/qiymat juftligi uchun funksiyani chaqiradi |
| entires()  | Mapdagi \[kalit, qiymat] juftlari bilan iteratorni qaytaradi     |
| Xususiyati | Ta'rif                                                           |
| size       | Mapdagi elementlar sonini qaytaradi                              |

### Map qanday yaratiladi

Mapni quyidagilar asosisa yaratishingiz mumkin:

* Massivni `new Map()` g o'tkazish orqali
* Map yarating va `Map.set()`dan foydalaning

### new Map() metodi

Massivni `new Map()`ga o'tkazish orqali Map yaratishingiz mumkin:

```
// Create a Map
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);
```

### set() metodi

Mapga elementlarni `set()` metodi bilan qo'shishingiz mumkin:

```
// Create a Map
const fruits = new Map();

// Set Map Values
fruits.set("apples", 500);
fruits.set("bananas", 300);
fruits.set("oranges", 200);
```

`set()`metodi mavjud Map qiymatlarini o'zgartirish uchun ham ishlatilishi mumkin:

```
fruits.set("apples", 200);
```

### get() metodi

`get()` metodi Mapdagi kalit qiymatini oladi:

```
fruits.get("apples");    // Returns 500
```

### Size xususiyati

`size` xususiyati Mapdagi elementlar sonini qaytaradi:

```
fruits.size;
```

### Delete() metodi

`delete()` metodi Mapdagi elementni olib tashlaydi:

```
fruits.delete("apples");
```

### has() metodi

Mapda kalit  bo'lsa, `has()` metodi "true" qaytaradi:

```
fruits.has("apples");
```

#### Sinab ko'ring:

```
fruits.delete("apples");
fruits.has("apples")
```

### Obektlar va Maplar

**Obektlar va Maplar o'rtasidagi farqlar:**

| Obekt         |                                              | Map                                               |
| ------------- | -------------------------------------------- | ------------------------------------------------- |
| Iterable      | To'g'ridan-to'g'ri iteratsiya bo'lmaydi      | To'g'ridan-to'g'ri iteratsiya bo'ladi             |
| Size          | Size xususiyatiga ega bo'lmaydi              | Size xususiyatiga ega bo'ladi                     |
| Kalit turlari | Kalitlar string (yoki simvol) bo'lishi kerak | Kalitlar har qanday ma'lumot turi bo'lishi mumkin |
| Kalit tartibi | Kalitlar yaxshi tartiblanmagan               | Kalitlar tartibni kiritish orqali tartiblanadi    |
| Default-lar   | Standart kalitlarga ega                      | Standart kalitlarga ega emas                      |

***

### forEach() metodi

`forEach()` metodi Mapdagi har bir kalit/qiymat juftligi uchun funksiyani chaqiradi:

```
// List all entries
let text = "";
fruits.forEach (function(value, key) {
  text += key + ' = ' + value;
})
```

### entry() metodi

`entries()` metodi Mapdagi \[kalit, qiymatlar] bilan iterator obektini qaytaradi:

```
// List all entries
let text = "";
for (const x of fruits.entries()) {
  text += x;
}
```

### Brauzerning qo'llab-quvvatlashj

Maplar Internet Explorerdan tashqari barcha brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
