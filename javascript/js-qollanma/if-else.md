# If else

Shartli ifodalar turli shartlarga asoslangan turli harakatlarni bajarish uchun ishlatiladi.

### Shartli ifodalar

Ko'pincha kod yozganingizda, turli qarorlar uchun turli xil amallar bajarishni xohlaysiz.

Buni amalga oshirish uchun kodingizda shartli ifodalardan foydalanishingiz mumkin.

JavaScript-da quyidagi shartli ifodalar mavjud:

* Berilgan shart rost bo'lsa, bajariladigan kod bloki ishlashi uchun `if` dan foydalaning
* Agar shart noto'g'ri bo'lsa, bajariladigan kod blokini ishlatish uchun `else` dan foydalaning
* Agar birinchi shart noto'g'ri bo'lsa, boshqa shartni tekshirish maqsadida yangi shart kiritish uchun `else if` dan foydalaning
* Bajariladigan ko'plab muqobil kod bloklarini ishlashi uchun `switch` dan foydalaning

{% hint style="warning" %}
`switch` steytmenti keyingi bo'limda tushuntirilgan.
{% endhint %}

### if steytmenti

Agar shart rost bo'lsa, bajariladigan kod bloki ishlashi uchun `if` dan foydalanish

#### Sintaksis

```javascript
if (condition) {
  //  agar shart true bo'lsa, bajarilishi kerak bo'lgan kod blok
}
```

{% hint style="warning" %}
`if` kichik harflarda ekanligiga e'tibor bering. Uni katta harflar bilan (If yoki IF) yozish  natijasida xatolik yuzaga keladi.
{% endhint %}

{% code title="Agar soat 18:00 dan kichik bo'lsa, "Xayrli kun" tilash:" %}
```javascript
if (hour < 18) {
  greeting = "Good day";
}

// Salomlashish natijasi quyidagicha bo'ladi:
Good day
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_ifthen" %}

### else steytmenti

Agar shart noto'g'ri bo'lsa, bajariladigan kod blokini ishlatish uchun `else` dan foydalaning

```javascript
if (shart) {
  //  agar shart true bo'lsa, bajarilishi kerak bo'lgan kod blok
} else {
  //  agar shart false bo'lsa, bajarilishi kerak bo'lgan kod blok
}
```

{% code title="Agar soat 18 dan kichik bo'lsa, "Xayrli kun"  tun tilang aks holda "Xayrli kech" tilang:" %}
```javascript
if (hour < 18) {
  greeting = "Good day";
} else {
  greeting = "Good evening";
}

// Salomlashish natijasi quyidagicha bo'ladi:
Good evening
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_ifthenelse" %}

### else if steytmenti

Agar birinchi shart noto'g'ri bo'lsa, keyingi shartni tekshirish uchun `else if`  steytmentidan foydalaning.

#### Sintaksis

```javascript
if (condition1) {
  //  agar shart true bo'lsa, bajarilishi kerak bo'lgan kod blok
} else if (condition2) {
  //  agar condition1 false va condition2 true bo'lsa bajariladigan kod blok
} else {
  //  agar condition1 va condition2 false bo'lsa bajariladigan kod blok
}
```

{% code title="Agar soat 10:00 dan kamroq bo'lsa, "Xayrli tong" tilang, agar bo'lmasa, lekin vaqt 20:00 dan kam bo'lsa, "Xayrli kun" tabrikini, aks holda "Xayrli oqshom" ni yarating:" %}
```javascript
if (time < 10) {
  greeting = "Good morning";
} else if (time < 20) {
  greeting = "Good day";
} else {
  greeting = "Good evening";

// Salomlashish natijasi quyidagicha bo'ladi:
Good evening
```
{% endcode %}

{% embed url="https://www.w3schools.com/js/tryit.asp?filename=tryjs_elseif" %}
