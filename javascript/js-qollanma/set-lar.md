# Set-lar

{% hint style="success" %}
Set - bu unikal qiymatlar to'plami hisoblanadi

Har bir qiymat Set-da faqat bitta bo'lishi mumkin.
{% endhint %}

### Set-ning muhim metodlari

| Metod         | Ta'rif                                                   |
| ------------- | -------------------------------------------------------- |
| new Set()     | Yangi to'plam yaratadi                                   |
| add()         | To'plamga yangi element qo'shadi                         |
| delete()      | To‘plamdan elementni olib tashlaydi                      |
| has()         | To'plamda qiymat mavjud bo'lsa, true qiymatini qaytaradi |
| forEach()     | To'plamdagi har bir element uchun callbackni chaqiradi   |
| values()      | To'plamdagi barcha qiymatlar bilan iteratorni qaytaradi  |
| **Xususiyat** | **Tarif**                                                |
| size          | To'plamdagi elementlar sonini qaytaradi                  |

### To'plam qanday yaratiladi

To'plamni quyidagilar asosida yaratishingiz mumkin:

* Arrayni `new Set()` ga o'tkazish orqali
* Yangi to'plam yarating va unga qiymat qo'shish uchun `add()`dan foydalaning
* Yangi to'plam yarating va o'zgaruvchilarni qo'shish uchun `add()`dan foydalaning

### new Set() metodi

Massivni `new Set()` ga o'tkazing:

```javascript
// Create a Set
const letters = new Set(["a","b","c"]);
```

To'plam yarating va unga qiymat qo'shing:

```javascript
// To'plam yaratish
const letters = new Set();

// To'plamga qiymat qo'shish
letters.add("a");
letters.add("b");
letters.add("c");
```

To'plam yarating va unga o'zgaruvchilar qo'shing:

```javascript
// To'plam yaratish
const letters = new Set();

// O'zgaruvchilar yaratish
const a = "a";
const b = "b";
const c = "c";

// To'plamga o'zgaruvchilar qo'shish
letters.add(a);
letters.add(b);
letters.add(c);
```

### add() metodi

```javascript
letters.add("d");
letters.add("e");
```

Agar siz bir nechta bir xil elementlar qo'shsangiz, ularning faqat birinchisi saqlanadi:

```javascript
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

`forEach()` metodi har bir Set elementi uchun funktsiyani chaqiradi:

```javascript
// To'plam yaratish
const letters = new Set(["a","b","c"]);

// Barcha elementlarni ro'yhatlash
let text = "";
letters.forEach (function(value) {
  text += value;
})
```

### values() metodi

`values()` metodi to'plamdagi barcha qiymatlarni o'z ichiga olgan yangi iterator obektini qaytaradi:

```javascript
letters.values()   // [object Set Iterator] Qaytaradi
```

Endi elementlarga murojaat qilish uchun Iterator obyektidan foydalanishingiz mumkin:

```javascript
// List all Elements
let text = "";
for (const x of letters.values()) {
  text += x;
}
```
