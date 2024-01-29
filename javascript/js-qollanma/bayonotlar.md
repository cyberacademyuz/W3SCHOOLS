# Bayonotlar

{% hint style="warning" %}
Dasturlash  sohasining o'zbek auditoriyasida bayonot so'zi keng tarqalmaganligi va dasturlash sohasiga tegishli terminlarni o'z nomi bilan atashlik yaxshiligi sababli bayonot so'zini steytment deb ataymiz.
{% endhint %}

```
let x, y, z;    // Steytment 1
x = 5;          // Steytment 2
y = 6;          // Steytment 3
z = x + y;      // Steytment 4
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_statements" %}

### JavaScript dasturlari

**Kompyuter dasturi** bu kompyuter tomonidan bajarilishi kerak bo'lgan ko'rsatmalar ro'yxatidir.

Dasturlash tilida ushbu dasturlash ko'rsatmalari **steytmentlar** deb ataladi.

**JavaScript dasturi** bu dasturlashdagi **bayonotlar** ro'yxatidir.

{% hint style="warning" %}
HTMLda JavaScript dasturlari veb-brauzer tomonidan amalga oshiriladi.
{% endhint %}

### JavaScript steytmentlari

JavaScript steytmentlari quyidagilardan iborat:

Qiymatlar, operatorlar, ifodalar, kalit so'zlar va izohlar.

Quyidagi steytment brauzerga id="demo" ga ega HTML elementining ichida "Salom Dolly" deb yozish kerakligini aytadi:

{% code title="Misol" %}
```javascript
document.getElementById("demo").innerHTML = "Hello Dolly."; 
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_statement" %}

JavaScript dasturlari ko'plab steytmentlarni o'z ichiga oladi.

Steytmentlar qanday yozilgan bo'lsa, birin-ketin bajariladi.

{% hint style="warning" %}
JavaScript dasturlari (va JavaScript steytmentlari) odatda JavaScript kodi deb ataladi.
{% endhint %}

## Nuqta vergul ;

Nuqta vergul javascript steytmentlarini ajratib turadi.

Har bir steytment ohiriga nuqta vergul qo'ying:

```
let a, b, c;  // Declare 3 variables
a = 5;        // Assign the value 5 to a
b = 6;        // Assign the value 6 to b
c = a + b;    // Assign the sum of a and b to c
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_statements_semicolon1" %}

Steymentlarni nuqta vergul bilan ajratganda ularning bir nechtasini bir qatorda yozish mumkin:

```
a = 5; b = 6; c = a + b; 
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_statements_semicolon2" %}

{% hint style="info" %}
Internetda nuqta-vergulsiz yozilgan kodlarni ko'rishingiz mumkin. Kodlarni nuqtali vergul bilan tugatish shart emas, lekin juda tavsiya qilinadi.
{% endhint %}

## Javascriptda bo'sh joylar

JavaScript bo'sh joylarga e'tibor bermaydi. Kodingizni o'qishga osonlashtirish uchun bo'sh joy qo'shishingiz mumkin.

Quyidagi kodlar bir xil ishlaydi:

```
let person = "Hege";
let person="Hege";
```

\= + - \* / kabi operatorlar atrofiga bo'sh joy qoldirish good practice hisoblanadi:

```
let x = y + z;
```

## Javascriptda qator uzunligi va qator tugashi

Kodning o'qishini yaxshilash uchun dasturchilar ko'pincha uzunroq kodning davomini 80ta belgidan keyin yangi qatordan yozishni yaxshi ko'radilar.

Agar JavaScript steytmenti bitta qatorga sig'masa, uni keyingi qatordan boshlash uchun eng yaxshi qism operatordan keyingi qism hisoblanadi:

```
document.getElementById("demo").innerHTML =
"Hello Dolly!";
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_statements_linebreak" %}

### JavaScript kod bloklari

Steytmentlarni kod bloklarda jingalak qavslar {...} orqali guruhlash mumkin.

Kod bloklarining maqsadi birgalikda bajarilishi kerak bo'lgan steytmentlarni ifodalash.

Bloklar ichida jamlangan steytmentlarni JavaScript funksiyalarining ichida ko'rishingiz mumkin:

```
function myFunction() {
  document.getElementById("demo1").innerHTML = "Hello Dolly!";
  document.getElementById("demo2").innerHTML = "How are you?";
}
```

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_statements_blocks" %}

{% hint style="warning" %}
Ushbu qo'llanmada biz kod bloklari uchun 2 ta bo'sh joydan foydalanganmiz.

Keyinchalik bu funksiyalar haqida ko'proq bilib olasiz.
{% endhint %}

## Javascript kalit so'zlari

JavaScript steytmentlari ko'pincha qanday amal bajarlishini ifodalash uchun biror bir **kalit so'z** bilan boshlanadi.

Biz keltirgan kalit so'zlar jadvalimiz JavaScriptdagi barcha kalit so'zlarning ro'yxatini beradi.

Pastda, siz o'rganadigan ba'zi kalit soʻzlar roʻyxati keltirilgan:

| Kalit so'z | Tavsif                                                                     |
| ---------- | -------------------------------------------------------------------------- |
| var        | O'zgaruvchi e'lon qiladi                                                   |
| let        | Blok o'zgaruvchisini e'lon qiladi                                          |
| const      | Blok o'zgarmas o'zgaruvchi e'lon qiladi                                    |
| if         | Shart bo'yicha bajarilishi kerak bo'lgan steytment blokini ifodalaydi      |
| switch     | Turli holatlarda bajarilishi kerak bo'lgan steytmentlar blokini ifodalaydi |
| for        | Loopda bajarilishi kerak bo'lgan steytmentlar blokini ifodalaydi           |
| function   | Funktsiya e'lon qiladi                                                     |
| return     | Funktsiyadan chiqadi                                                       |
| try        | Steytmentlar blokiga xatolarni qayta ishlashni amalga oshiradi             |

{% hint style="warning" %}
JavaScript kalit so'zlari standart so'zlardir. Standart so'zlarni o'zgaruvchi nomi sifatida ishlatib bo'lmaydi.
{% endhint %}
