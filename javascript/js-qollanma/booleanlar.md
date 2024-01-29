# Booleanlar

{% hint style="success" %}
JavaScript mantiqiy ikki qiymatdan birini ifodalaydi: **true** yoki **false** .
{% endhint %}

### Boolean qiymatlar

Ko'pincha, dasturlashda sizga ikkita qiymatdan faqat bittasi bo'lishi mumkin bo'lgan ma'lumotlar turi kerak bo'ladi, masalan

* HA / YO'Q
* ON / OFF
* ROST / YOLG'ON

Buning uchun JavaScript **boolean** ma'lumotlar turiga ega. U faqat **true** yoki **false** qiymatlarini qabul qilishi mumkin.

### Boolean() funktsiyasi

Expressionning (yoki o'zgaruvchi) to'g'ri yoki noto'g'riligini tekshirish uchun `Boolean()` funktsiyadan foydalanishingiz mumkin:

```
Boolean(10 > 9)
```

Yoki undan ham osonroq:

```
(10 > 9)
10 > 9
```

## Taqqoslash va shartlar

JS Comparisons bo'limida taqqoslash operatorlari haqida to'liq ma'lumot berilgan.

JS Conditions bo'limida shartli steytmentlar haqida toʻliq maʼlumot berilgan.

Mana bunga bir nechta misollar:

| Operator | Ta'rif     | Misol                |
| -------- | ---------- | -------------------- |
| ==       | ga teng    | if (day == "Monday") |
| >        | dan katta  | if (salary > 9000)   |
| <        | dan kichik | if (age < 18)        |

{% hint style="warning" %}
Expressionning boolean qiymati Javascriptning barcha taqqoslash va shartli holatlari uchun asos bo'ladi.
{% endhint %}

### Qiymati bor bo'lgan barcha narsa True

```
100

3.14

-15

"Hello"

"false"

7 + 1 + 3.14
```

### Qiymati bo'lmagan barcha narsa False

{% code title="0 ning boolean qiymati false:" %}
```
let x = 0;
Boolean(x);
```
{% endcode %}

{% code title="-0 ning boolean qiymati false:" %}
```
let x = -0;
Boolean(x);
```
{% endcode %}

{% code title=""" (bo'sh string) ning boolean qiymati  false:" %}
```
let x = "";
Boolean(x);
```
{% endcode %}

{% code title="Undefined ning boolean qiymati false:" %}
```
let x;
Boolean(x);
```
{% endcode %}

{% code title="null ning boolean qiymati false:" %}
```
let x = null;
Boolean(x);
```
{% endcode %}

{% code title="False ning boolean qiymati false:" %}
```
let x = false;
Boolean(x);
```
{% endcode %}

{% code title="NaN ning boolean qiymati false:" %}
```
let x = 10 / "Hallo";
Boolean(x);
```
{% endcode %}

### Booleanlarni obekt sifatida e'lon qilish

Odatda booleanlar literallardan yaratilgan primitiv qiymat hisoblanadi:

```
let x = false;
```

Ammo booleanlarni `new` kalit so'zi bilan obekt sifatida ham ifodalash mumkin:

```
let y = new Boolean(false);
```

```
let x = false;
let y = new Boolean(false);

// typeof x returns boolean
// typeof y returns object
```

{% hint style="warning" %}
Boolean obektlarini yaratmang.

`new` kalit so'zi kodni murakkablashtiradi va bajarish tezligini sekinlashtiradi.

Boolean obektlari kutilmagan natijalarga olib kelishi mumkin:
{% endhint %}

{% code title="== operatoridan foydalanganda x va y teng :" %}
```
let x = false;
let y = new Boolean(false);
```
{% endcode %}

{% code title="=== operatoridan foydalanganda x va y teng emas:" %}
```
let x = false;
let y = new Boolean(false);
```
{% endcode %}

{% hint style="warning" %}
(x==y) va (x===y) o'rtasidagi farqga e'tibor bering.
{% endhint %}

{% code title="(x == y) True yoki False ?" %}
```
let x = new Boolean(false);
let y = new Boolean(false);
```
{% endcode %}

{% code title="(x === y) True yoki False ?" %}
```
let x = new Boolean(false);
let y = new Boolean(false); 
```
{% endcode %}

{% hint style="warning" %}
Ikki obyektini solishtirish har doim false qiymat qaytaradi.
{% endhint %}

{% hint style="warning" %}
### Boolean haqida to'liq ma'lumotnoma

Boolean haqida to'liq ma'lumotnomani ko'rish uchun bizning [Boolean obekti haqida to'liq ma'lumotnoma ](https://www.w3schools.com/jsref/jsref\_obj\_boolean.asp)sahifamizga o'ting:

Ma'lumotnomada Booleanning barcha xususiyatlari va metodlar haqida ma'lumot va misollar keltirilgan.
{% endhint %}
