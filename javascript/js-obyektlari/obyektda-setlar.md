# Obyektda Setlar

{% hint style="success" %}
Setlar unikal qiymatlar to'plamidir.

Har bir qiymat to'plamda faqat bir marta bo'lishi mumkin.

To'plam har qanday turdagi ma'lumotlarning istalgan qiymatini saqlashi mumkin.
{% endhint %}

### Set metodlari

| Metod     | Tavsif                                                          |
| --------- | --------------------------------------------------------------- |
| new Set() | Yangi to'plam yaratadi                                          |
| add()     | To'plamga yangi element qo'shadi                                |
| delete()  | To‘plamdan elementni olib tashlaydi                             |
| has()     | Agar qiymat mavjud bo'lsa, true qiymatini qaytaradi             |
| clear()   | To'plamdan barcha elementlarni olib tashlaydi                   |
| forEach() | Har bir element uchun callbackni chaqiradi                      |
| values()  | To'plamdagi barcha qiymatlar bilan birga iteratorni qaytaradi   |
| keys()    | values() bilan bir xil                                          |
| entries() | Toʻplamdagi \[qiymat, qiymat] juftligi bilan iterator qaytaradi |

| Xususiyat | Qiymat                                  |
| --------- | --------------------------------------- |
| size      | To'plamdagi elementlar sonini qaytaradi |

### To'plamni qanday yaratish kerak

JavaScriptda to'plamni quyidagicha yaratishingiz mumkin:

* Massivni `new Set()` ga o'tkazish orqali
* Yangi Set yarating va qiymatlarni qo'shish uchun `add()`dan foydalaning
* Yangi Set yarating va o'zgaruvchilarni qo'shish uchun `add()`dan foydalaning

### new Set() metodi

Massivni `new Set()` konstruktoriga uzating:

```
// Create a Set
const letters = new Set(["a","b","c"]);
```

To'plam yarating va literal qiymatlar qo'shing:

```
// Create a Set
const letters = new Set();

// Add Values to the Set
letters.add("a");
letters.add("b");
letters.add("c");
```

To'plam yarating va o'zgaruvchilar qo'shing:

```
// Create Variables
const a = "a";
const b = "b";
const c = "c";

// Create a Set
const letters = new Set();

// Add Variables to the Set
letters.add(a);
letters.add(b);
letters.add(c);
```

### add() metodi

```
letters.add("d");
letters.add("e");
```

Agar siz bir xil elementlarni qo'shsangiz, faqat birinchisi saqlanadi:

```
letters.add("a");
letters.add("b");
letters.add("c");
letters.add("c");
letters.add("c");
letters.add("c");
letters.add("c");
letters.add("c");
```

### forEach() metodi

`forEach()` metodi har bir Set elementi uchun funksiyani chaqiradi:

```
// Create a Set
const letters = new Set(["a","b","c"]);

// List all entries
let text = "";
letters.forEach (function(value) {
  text += value;
})
```

### values() metodi

`values()` metodi to'plamdagi barcha qiymatlarni o'z ichiga olgan Iterator obyektini qaytaradi:

```
letters.values()   // Returns [object Set Iterator]
```

Endi elementlarga murojaat qilish uchun Iterator obyektidan foydalanishingiz mumkin:

```
// Create an Iterator
const myIterator = letters.values();

// List all Values
let text = "";
for (const entry of myIterator) {
  text += entry;
}
```

### Keys() metodi

{% hint style="warning" %}
To'plamda kalitlar yo'q.

`keys()` `values()` bilan bir xil qiymat qaytaradi.

Bu toʻplamlarni Maplar bilan mos qiladi.
{% endhint %}

```
letters.keys()   // Returns [object Set Iterator]
```

### entries() metodi

{% hint style="warning" %}
To'plamda kalitlar yo'q.

`entries()`\[kalit, qiymat] juftligi oʻrniga \[qiymat, qiymat] juftligini qaytaradi.

Bu toʻplamlarni Maplar bilan mos qiladi:
{% endhint %}

```
// Create an Iterator
const myIterator = letters.entries();

// List all Entries
let text = "";
for (const entry of myIterator) {
  text += entry;
}
```

### To'plamlar obyektlardir

`typeof`  set uchun object qiymatini qaytaradi:

```
typeof letters;      // Returns object
```

`instanceof Set` set uchun `true` qiymatini qaytaradi:

```
letters instanceof Set;  // Returns true
```
