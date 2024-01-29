# Dizayn uchun qo'llanma

JavaScript loyihalaringiz uchun har doim bir xil kodlash qoidalaridan foydalaning.

## JavaScript kodlash konventsiyalari

Kodlash konventsiyalari dasturlash uchun dizayn ko'rsatmalaridir . Ular odatda quyidagilarni qamrab oladi:

* O'zgaruvchilar va funktsiyalar uchun nom berish va e'lon qilish qoidalari.
* Bo'sh joy, indentatsiya va izohlardan foydalanish qoidalari.
* Dasturlash amaliyoti va tamoyillari.

Kodlash konventsiyalari **xavfsiz sifat** deganidir:

* Kodni o'qishga osonlashishini yaxshilang
* Kodlarni saqlashni osonlashtiring

Kodlash konventsiyalari jamoalar rioya qilishi kerak bo'lgan hujjatlashtirilgan qoidalar bo'lishi mumkin yoki shunchaki sizning kod yozishdagi shaxsiy qoidalaringiz bo'lishi mumkin.

{% hint style="warning" %}
Bu sahifada W3Schools tomonidan ishlatiladigan umumiy JavaScript kod konventsiyalari tushuntirilgan.\
Bundan tashqari, "Best practice" va kodlash tuzoqlaridan qanday qochish kerakligini bilib olish uchun keyingi bo'limni o'qishingiz kerak.
{% endhint %}

### O'zgaruvchi nomlari

W3schools da biz o'zgaruvchilar va funksiya nomlari uchun **camelCase** dan foydalanamiz.

Barcha nomlar **harf** bilan boshlanadi.

Ushbu sahifaning pastki qismida siz identifikatorlarga nom berish qoidalari haqida ko'proq ma'lumotlarni topasiz.

```
firstName = "John";
lastName = "Doe";

price = 19.90;
tax = 0.20;

fullPrice = price + (price * tax);
```

### Operatorlar atrofidagi bo'sh joylar

Har doim operatorlar ( = + - \* / ) atrofida va verguldan keyin bo'sh joy qo'ying:

```
let x = y + z;
const myArray = ["Volvo", "Saab", "Fiat"];
```

### Kod indentatisyalari

Kod bloklarini ajraish uchun har doim 2 ta bo'sh joydan foydalaning:

{% code title="Funksiyalari:" %}
```
function toCelsius(fahrenheit) {
  return (5 / 9) * (fahrenheit - 32);
}
```
{% endcode %}

{% hint style="danger" %}
Indentatsiya uchun **tab**lardan foydalanmang. Turli code editorlar tablarni har hil joy tashlaydi.
{% endhint %}

### Steytment qoidalari

Oddiy steytmentlar uchun umumiy qoidalar:

* Har doim oddiy steytmentni nuqta-vergul bilan yakunlang.

```
const cars = ["Volvo", "Saab", "Fiat"];

const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

Murakkab steytmentlar uchun umumiy qoidalar:

* Birinchi qatorning oxiriga ochiladigan jingakaj qavsni **{** qo'ying.
* Ochiluvchi jingalak qavsdan oldin bitta bo'sh joy tashlang.
* Yopuvchi jingalak qavs **}** ni oldinga bo'sh joy qoldirmasdan yangi qatorga o'tkazing.
* Murakkab steytmentlarni nuqta-vergul bilan tugatmang.

{% code title="Funksiyalar:" %}
```
function toCelsius(fahrenheit) {
  return (5 / 9) * (fahrenheit - 32);
}
```
{% endcode %}

{% code title="Looplar:" %}
```
for (let i = 0; i < 5; i++) {
  x += i;
}
```
{% endcode %}

{% code title="Shartlar:" %}
```
if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}
```
{% endcode %}

### Obyekt qoidalari

Obyekt e'lon qilishning umumiy qoidalari:

* Ochiluvchi jingalak qavsni obyekt nomi bilan bir qatorda yozing.
* Har bir xususiyat va uning qiymati o'rtasida ikki nuqta bitta bo'sh joy qo'ying.
* Stringdan iborat qiymatlarni qo'shtirnoqlar bilan o'rang, raqamli qiymatlarni qo'shtirnoq ichiga olmang.
* Oxirgi xususiyat/qiymat juftligidan keyin vergul qo'ymang.
* Yopuvchi jingalak qavsning oldiga bo'sh joy qoldirmasdan yangi qatorga qo'ying.
* Obyektni har doim nuqta-vergul bilan yakunlang.

```
const person = {
  firstName: "John",
  lastName: "Doe",
  age: 50,
  eyeColor: "blue"
};
```

Qisqaroq  obektlarni zijlab bir qatorda, xususiyatlar orasidagi bo'sh joy qoldirish orqali yozish mumkin, masalan:

```
const person = {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"};
```

### Qator uzunligi <80

Kodni o'qishga oson bo'lishi uchun 80 belgidan ortiq stringdan foydalanmang.

Agar JavaScript steytmenti bir qatorga sig'masa, uni ikki bo'lish uchun kodning eng yaxshi qism biror operator yoki verguldan keyingi joydir.

```
document.getElementById("demo").innerHTML =
"Hello Dolly.";
```

### Nom berish qoidalari

Kodlaringiz uchun har doim bir xil nom berish konventsiyasidan foydalaning. Masalan:

* **CamelCase** sifatida yozilgan oʻzgaruvchi va funksiya nomlari
* **KATTA HARF** bilan yozilgan global o'zgaruvchilar (w3schoolsda bunday emas, lekin bu juda keng tarqalgan)
* **KATTA HARF** bilan yozilgan constanlar (PI kabi).

O'zgaruvchilar nomlarida **hyp-hen**lar , **camelCase** yoki **under\_scores** dan foydalanish kerakmi ?

Bu dasturchilar orasida ko'p muhokama qilinadigan savol hisoblanadi. Javob kimdan so'raganingizga bog'liq:

**HTML va CSSdagi chiziqlar:**

HTML5 atributlari data- dan boshlanishi mumkin (data-quantity, data-price).

CSS xususiyat nomlarida (font-size) chiziqdan foydalanadi.

{% hint style="danger" %}
Chiziqlar ayirish operatori bo'lganligi sababli o'zgaruvchi nomlarida xatolikka olib kelishi mumkin. JavaScript nomlarida chiziq qoʻyish mumkin emas.
{% endhint %}

**Pastki chiziq:**

Ko'pgina dasturchilar, ayniqsa, SQL ma'lumotlar bazalarida pastki chiziqdan foydalanishni afzal ko'radilar.

Pastki chiziq ko'pincha PHPda qo'llaniladi.

**PascalCase:**

PascalCase ko'pincha C dasturchilari tomonidan ko'p ishlatiladi.

**camel Case:**

camelCase JavaScript-ning o'zi, jQuery va boshqa JavaScript kutubxonalarida ko'p ishlatiladi.

{% hint style="danger" %}
Nomlarni $ belgisi bilan boshlamang. Bu ko'plab JavaScript kutubxonalari nomlari bilan ziddiyatga olib keladi.
{% endhint %}

### HTMLga javascriptni ulash

Tashqi fayllarni ulash uchun oddiy quyidagidej sintaksisdan foydalaning (type atributi shart emas):

```
<script src="myscript.js"></script>
```

### HTML elementlariga murojaat qilish

HTML kodlarini tartibsiz yozish natijasida JavaScript xatolari yuzaga kelishi mumkin.

Ushbu ikki JavaScript steytmenti har xil natija qaytaradi:

```
const obj = getElementById("Demo")

const obj = getElementById("demo")
```

Iloji bo'lsa, HTMLda ham bir xil nom berish konventsiyasidan (JavaScript kabi) foydalaning.

**HTMLda kod yozish dizayni bo'yicha qo'llanmaga tashrif buyuring.**

### Fayl kengaytmalari

HTML fayllari **.html** kengaytmasiga ega bo'lishi kerak ( **.htm** ham bo'lishi mumkin).

CSS fayllari **.css** kengaytmasiga ega bo'lishi kerak.

JavaScript fayllari **.js** kengaytmasiga ega boʻlishi kerak.

### Kichik harfda yozilgan fayl nomlaridan foydalaning

Ko'pgina veb-serverlar (Apache, Unix) fayl nomlari uchun katta-kichik harflarni turlicha qabul qiladi:

london.jpg fayliga London.jpg sifatida murojaat qilish mumkin emas.

Boshqa veb-serverlar (Microsoft, IIS) katta-kichik harflarga e'tibor qilinmaydi:

london.jpg ga London.jpg yoki london.jpg sifatida ham murojaat qilish mumkin.

Agar siz katta-kichik harflarni aralashtirib yozgan bo'lsangiz, juda sezgir bo'lishingiz kerak.

Agar katta-kichik harfga e'tibor qilmaydigan serverdan katta-kichik harfga e'tibor qiladigan serverga o'tsangiz, hatto kichik xatolar ham veb-saytingizni buzishi mumkin.

Ushbu muammolarni oldini olish uchun har doim fayl nomlarida kichik harflardan foydalaning.

### Ishlash

Kod yozish qoidalari kompyuterlar tomonidan qo'llanilmaydi. Qoidalar dasturning ishlashiga kam ta'sir qiladi.

Kichik skriptlarda indentatsiya va qo'shimcha bo'sh joylar muhim emas.

Yozilayotgan kod, o'qish uchun oson bo'lishi kerak. Katta dasturlarning kodlarini minimallashtirish kerak.
