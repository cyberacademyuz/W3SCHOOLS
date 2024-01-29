# Xatolar

Ushbu boʻlimda ba'zi koʻp uchraydiga xatolar ko'rsatilgan.

### Tayinlash operatoridan tasodifan foydalanish

Agar dasturchi tasodifan if steytmentida taqqoslash operatori (==) o'rniga tayinlash operatoridan (=) foydalansa, JavaScript kodlari kutilmagan natijalarga olib kelishi mumkin.

Bu `if` steytmenti `false` qaytaradi, chunki `x` 10 ga teng emas:

```
let x = 0;
if (x == 10)
```

Bu if steytmenti true qaytarad, chunki 10 true:

```
let x = 0;
if (x = 10)
```

Bu if steytmenti false qaytaradi, chunki 0 false:

```
let x = 0;
if (x = 0)
```

{% hint style="warning" %}
Tayinlash har doim tayinlovning qiymatini qaytaradi.
{% endhint %}

### Taqqoslashdagi kamchilik

Oddiy taqqoslashda ma'lumot turi muhim qanday boʻlishi muhim emas. Bu if steytmenti true qaytaradi:

```
let x = 10;
let y = "10";
if (x == y)
```

Qatiy taqqoslashda, ma'lumot turi muhim hisoblanadi. Bu if steytmentifalse qaytaradi.

```
let x = 10;
let y = "10";
if (x === y)
```

`switch` steytmentlari qat'iy taqqoslashdan foydalanishini koʻpchilik unutib qoʻyadi:

Bu `switch case` alert ichidagi matnni ko'rsatadi:

```
let x = 10;
switch(x) {
  case 10: alert("Hello");
}
```

Bu `case switch`ogohlantirishni ko'rsatmaydi:

```
let x = 10;
switch(x) {
  case "10": alert("Hello");
}
```

### Qo'shish va konkatenatsiyada chalkashish

**Qoʻshish** bu raqamlar ustida arifmetik qoʻshish amali hisoblqnadi.

**Konkatenatsiya** esa stringlarni bir biriga ulash hisoblanadi.

Javascriptda bu ikki vazifa bir xil + belgisi bilan amalga oshiriladi.

Shu sababli, raqamni number sifatida qo'shish raqamni string sifatida qo'shishdan farq qiladi:

```
let x = 10;
x = 10 + 5;       // Now x is 15

let y = 10;
y += "5";        // Now y is "105"
```

Ikki o'zgaruvchini qo'shganda, natijani taxmin qilishingiz qiyin bo'lishi mumkin:

```
let x = 10;
let y = 5;
let z = x + y;     // Now z is 15

let x = 10;
let y = "5";
let z = x + y;     // Now z is "105"
```

### Floatlarning notoʻgʻri natijaga olib kelishi

JavaScript-dagi barcha raqamlar 64-bitli Floating Point raqamlar (Floats) sifatida saqlanadi.

Barcha dasturlash tillari, shu jumladan JavaScript ham, float qiymatlarini hisoblashda aniq qiymatni chiqara olmaydi:

```
let x = 0.1;
let y = 0.2;
let z = x + y            // the result in z will not be 0.3
```

Yuqoridagi muammoni hal qilish uchun u ko'paytirish va bo'lishga yordam beradi:

```
let z = (x * 10 + y * 10) / 10;       // z will be 0.3
```

### Stringlarni boʻlaklarga boʻlish

JavaScript sizga steytmentni ikki qatorga yozish imkonini beradi:

{% code title="1-misol:" %}
```
let x =
"Hello World!";
```
{% endcode %}

Biroq, string o'rtasidan steytmentni boʻlarga ajratish ishlamaydi:

{% code title="2-misol:" %}
```
let x = "Hello
World!";
```
{% endcode %}

Agar sizga steytmentdagi stringni ikki boʻlakka ajratish kerak bo'lsa, "backslash" (\\) dan foydalanishingiz kerak:

{% code title="3-misol:" %}
```
let x = "Hello \
World!";
```
{% endcode %}

### Nuqtali vergulni noto‘g‘ri joyga qo‘yish

Nuqtali vergulni notoʻgʻri joyga qoʻyish tufayli x-ning qiymati qanday boʻlishidan qat'iy nazar ushbu kod bloki bajariladi:

```
if (x == 19);
{
  // code block 
}
```

### Return kalit spzidagi kodni qatorlarga ajratish

Bu qator oxiridagi steytmentni avtomatik tarzda tugatish uchun JavaScriptning standart hatti harakatidir.

Shu sababli, quyidgi ikki misol bir xil natijani qaytaradi:

{% code title="1-misol:" %}
```
function myFunction(a) {
  let power = 10 
  return a * power
}
```
{% endcode %}

{% code title="2-misol:" %}
```
function myFunction(a) {
  let power = 10;
  return a * power;
}
```
{% endcode %}

Shuningdek JavaScript steytmentni ikki qatorga ajratish imkonini beradi.

Shu sababli, 3-misol ham xuddi shunday natija qaytaradi:

{% code title="3-misol:" %}
```
function myFunction(a) {
  let
  power = 10; 
  return a * power;
}
```
{% endcode %}

Ammo, agar siz return kalit soʻzidagi kodni ikkita qatorga ajratsangiz nima bo'ladi:

{% code title="4-misol:" %}
```
function myFunction(a) {
  let
  power = 10; 
  return
  a * power;
}
```
{% endcode %}

Funktsiya `undefined` qaytaradi.

Nega? Chunki JavaScript kodni 5-misoldagi kod kabi tushunadi:

{% code title="5-misol:" %}
```
function myFunction(a) {
  let
  power = 10; 
  return;
  a * power;
}
```
{% endcode %}

### Tushuntirish

Agar steytment quyidagi misoldakidek tugallanmagan boʻlsa:

```
let
```

Javascript keyingi qatorni oʻqish orqali steytmentni tugatib qoʻyishga harakat qiladi.

```
power = 10;
```

Ammo ushbu return to'liq bo'lgani uchun:

```
return
```

Javascript uni nuqtali vergul bilan yopadi:

```
return;
```

Buning sababi, JavaScript-da steytmentlarni nuqtali vergul bilan tugatish ixtiyoriy.

Javascript qator ohiridagi return steytmentini oʻzi yopadi, chunki u toʻliq shakldagi steytment hisoblanadi.

{% hint style="danger" %}
Return steytmentini hech qachon ikkiga ajratmang
{% endhint %}

### Array elemenetlarga ularning nomli indeksi bilan murojaat qilish

Ko'pgina dasturlash tillari nomli indekslarga ega massivlarni qo'llab-quvvatlaydi.

Nomli indekslarga ega massivlar assotsiativ massivlar (yoki xeshlar) deb ataladi.

JavaScript nomli indeksli massivlarni qo'llab-quvvatlamaydi.

JavaScript-da arraylar raqamli indekslardan foydalanadi.

```
const person = [];
person[0] = "John";
person[1] = "Doe";
person[2] = 46;
person.length;       // person.length will return 3
person[0];           // person[0] will return "John"
```

JavaScript-da obektlar nomli indekslardan foydalanadi.

Agar siz array elementlariga murojaat qilish uchun nomli indeksdan foydalansangiz, JavaScript arrayni obyektga aylantiradi.

Avtomatik tarzda obyektga aylantirilganidan keyin esa, array metodlari va xususiyatlari undefined qaytaradi yoki noto'g'ri natija beradi:

```
const person = [];
person["firstName"] = "John";
person["lastName"] = "Doe";
person["age"] = 46;
person.length;      // person.length will return 0
person[0];          // person[0] will return undefined
```

### Obyekt maʼlumotlarining ohirini vergul bilan tugatishh

ECMAScript 5 da obyekt va arraylarda vergullardan foydalanish mumkin.

{% code title="Obyektga misol:" %}
```
person = {firstName:"John", lastName:"Doe", age:46,}
```
{% endcode %}

{% code title="Arrayga misoli:" %}
```
points = [40, 100, 1, 5, 25, 10,];
```
{% endcode %}

{% hint style="danger" %}
OGOHLANTIRISH!!

Internet Explorer 8 da ishlamaydi.

JSON qoʻshimcha vergullarga ruxsat bermaydi.
{% endhint %}

{% code title="JSON:" %}
```
person = {"firstName":"John", "lastName":"Doe", "age":46}
```
{% endcode %}

{% code title="JSON:" %}
```
points = [40, 100, 1, 5, 25, 10];
```
{% endcode %}

### Undefined null emas

JavaScript obyektlari, o'zgaruvchilari, xususiyatlari va meodlari `undefined` bo'lishi mumkin.

Bundan tashqari, boʻm bo'sh obyektlar null qiymatiga ega bo'lishi mumkin.

Bu esa obyekt boʻsh yoki boʻsh emasligini tekshirishni biroz qiyinlashtiradi.

Obyekt mavjud yoki mavjudmasligini uning maʼlumot turini `undefined` ekanligini tekshirish orqali tekshirishingiz mumkin:

```
if (typeof myObj === "undefined") 
```

Lekin obyekt `null` yoki `null` emasligini tekshira olmaysiz, chunki obyekt `undefined` bo'lsa, bu xatoga olib keladi:

{% code title="Noto'g'ri:" %}
```
if (myObj === null) 
```
{% endcode %}

Ushbu muammoni hal qilish uchun obyekt `null` va `undefined` emasligini tekshirishingiz kerak.

Ammo bunda ham xatolik yuzaga kelishi mumkin:

{% code title="Noto'g'ri:" %}
```
if (myObj !== null && typeof myObj !== "undefined") 
```
{% endcode %}

Shu sababli, `null` emasligini tekshirishdan avval `undefined` emasligini tekshirishingiz kerak.

{% code title="To'g'ri:" %}
```
if (typeof myObj !== "undefined" && myObj !== null) 
```
{% endcode %}
