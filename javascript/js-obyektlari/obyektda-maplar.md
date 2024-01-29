# Obyektda Maplar

{% hint style="success" %}
Map kalit-qiymat juftligidan tashkil topadi, undagi kalitlarda har qanday ma'lumot turi bo'lishi mumkin.

Map kalitlarning qo'shish tartibini eslab qoladi.

Map mapning o'lchamini ifodalovchi xususiyatga ega.
{% endhint %}

### Xarita metodlari

| Metodlar    | Ta'rif                                                           |
| ----------- | ---------------------------------------------------------------- |
| new Map()   | Yangi Map obyektini yaratadi                                     |
| set()       | Mapdagi key uchun qiymat belgilaydi                              |
| get()       | Mapdagi key uchun qiymatni oladi                                 |
| clear()     | Mapdagi barcha elementlarni olib tashlaydi                       |
| delte()     | Key bilan belgilangan Map elementini olib tashlaydi              |
| has()       | Mapda kalit mavjud bo'lsa, true qiymatini qaytaradi              |
| forEach()   | Mapdagi har bir kalit/qiymat juftligi uchun callback chaqiradi   |
| entries()   | Mapdagi \[kalit, qiymat] jufligi bilan iterator obyekt qaytaradi |
| kalitlari() | Mapdagi kalitlar bilan iterator obyektini qaytaradi              |
| qiymatlar() | Mapdagi qiymatlarning iterator obyektini qaytaradi               |

| Xususiyat | Ta'rif                                |
| --------- | ------------------------------------- |
| size      | Map elementlaring miqdorini qaytaradi |

### Mapni qanday yaratish kerak

Siz Mapni quyidagilar bilan yaratishingiz mumkin:

* Massivni `new Map()` o'tkazish orqali
* Map yarating va `Map.set()` dan foydalaning.

### new Map()

Massivni `new Map()` konstruktoriga o'tkazish orqali Map yaratishingiz mumkin:

```
// Create a Map
const fruits = new Map([
  ["apples", 500],
  ["bananas", 300],
  ["oranges", 200]
]);
```

### Map.set()

Xaritaga elementlarni quyidagi `set()` metodi bilan qo'shishingiz mumkin:

```
// Create a Map
const fruits = new Map();

// Set Map Values
fruits.set("apples", 500);
fruits.set("bananas", 300);
fruits.set("oranges", 200);
```

`set()` metodi mavjud Map qiymatlarini o'zgartirish uchun ham ishlatilishi mumkin:

```
fruits.set("apples", 500);
```

### Map.get()

`get()` metodi mapdagi kalitning qiymatini oladi:

```
fruits.get("apples");    // Returns 500
```

### Map.size

`size` xususiyati mapdagi elementlar sonini qaytaradi:

```
fruits.size;
```

### Map.delete()

`delete()` metodi Map elementini olib tashlaydi:

```
fruits.delete("apples");
```

### Map.clear()

`clear()` metodi mapdagi barcha elementlarni olib tashlaydi:

```
fruits.clear();
```

### Map.has()

Agar mapda key bor bo'lsa, `has()` metodi  "true"  qaytaradi :

```
fruits.has("apples");
```

#### Buni sinab ko'ring:

```
fruits.delete("apples");
fruits.has("apples");
```

### Maplar obyektlardir

`typeof` object qaytaradi:

```
// Returns object:
typeof fruits;
```

`instanceof` Map true qaytaradi:

```
// Returns true:
fruits instanceof Map;
```

### Obyektlar va Maplar

**Obyektlari va Maplar o'rtasidagi farqlar:**

| Obyekt                                      | Map                                             |
| ------------------------------------------- | ----------------------------------------------- |
| To'g'ridan-to'g'ri takrorlanmaydi           | To'g'ridan-to'g'ri takrorlanadigan              |
| size xususiyati yo'q                        | size xususiyatiga ega                           |
| Keylari string (yoki simvol) bo'lishi kerak | Keylar har qanday ma'lumot turi bo'lishi mumkin |
| Keylar yaxshi tartiblanmagan                | Keylar kiritish orqali tartiblanadi             |
| Standart keylarga ega                       | Standart keylarga ega emas                      |

### Map.forEach()

`forEach()` metodi Mapdagi har bir kalit/qiymat juftligi uchun callbackni chaqiradi:

```
// List all entries
let text = "";
fruits.forEach (function(value, key) {
  text += key + ' = ' + value;
})
```

### Map.entries()

`entries()` metodi mapdagi \[kalit, qiymatlar] bilan iterator obyekt qaytaradi:

```
// List all entries
let text = "";
for (const x of fruits.entries()) {
  text += x;
}
```

### Map.keys()

`keys()` metodi mapdagi keylarga ega iterator obyekt qaytaradi:

```
// List all keys
let text = "";
for (const x of fruits.keys()) {
  text += x;
}
```

### Map.values()

`values()` metodi mapdagi qiymatlar bilan iterator obyekt qaytaradi:

```
// List all values
let text = "";
for (const x of fruits.values()) {
  text += x;
}
```

Mapdagi qiymatlarni yig'ish uchun `values()` metodidan foydalanishingiz mumkin:

```
// Sum all values
let total = 0;
for (const x of fruits.values()) {
  total += x;
}
```

### Obyektlardan key sifatida foydalanish

{% hint style="warning" %}
Obyektlarni key sifatida ishlatish imkoniyati mapning muhim xususiyatidir.
{% endhint %}

```
// Create Objects
const apples = {name: 'Apples'};
const bananas = {name: 'Bananas'};
const oranges = {name: 'Oranges'};

// Create a Map
const fruits = new Map();

// Add new Elements to the Map
fruits.set(apples, 500);
fruits.set(bananas, 300);
fruits.set(oranges, 200);

```

Esingizda bo'lsin: Key bu string ("olma") emas, balki obyekt (olma):

```
fruits.get("apples");  // Returns undefined
```

### Brauzerni qo'llab-quvvatlash

Maplar Internet Explorerdan tashqari barcha brauzerlarda qo'llab-quvvatlanadi:

|        |      |         |        |       |
| ------ | ---- | ------- | ------ | ----- |
| Chrome | Edge | Firefox | Safari | Opera |
