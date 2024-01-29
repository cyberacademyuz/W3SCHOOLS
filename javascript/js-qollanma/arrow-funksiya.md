# Arrow funksiya

{% hint style="success" %}
Arrow funksiyalar ES6 da joriy qilingan.

Arrow funksiyani kichikroq sintaksisda yozishga imkon beradi:

let myFunction = (a, b) => a \* b;
{% endhint %}

{% code title="Arrow funksiyasiz funksiya yaratishz:" %}
```
hello = function() {
  return "Hello World!";
}
```
{% endcode %}

{% code title="Arrow funksiya yordamida:" %}
```
hello = () => {
  return "Hello World!";
}
```
{% endcode %}

U qisqaroq yoziladi! Agar funksiyada faqat bitta steytment bo'lsa va steytment qiymat qaytarsa, qavslar va return kalit so'zini olib tashlashingiz mumkin:&#x20;

{% code title="Arrow funksiyalar defaukt tarzda qiymat qaytaradi" %}
```
hello = () => "Hello World!";
```
{% endcode %}

{% hint style="warning" %}
**Eslatma:** Bu funksiya faqat bitta steytmentga ega bo'lsagina ishlaydi.
{% endhint %}

Agar parametrlardan foydalanmoqchi bo'lsangiz, ularni qavs ichida yozasiz:

{% code title="Parametrli arrow funksiyasi:" %}
```
hello = (val) => "Hello " + val;
```
{% endcode %}

Aslida, agar bitta parametrdan foydalansangiz, qavslardan foydalanmasangiz ham boʻladi.

{% code title="Qavssiz arrow funktsiya:" %}
```
hello = val => "Hello " + val;
```
{% endcode %}

### `this` o'zi nima ?

`this`dan foydalanish oddiy funksiyalarga nisbatan arrow funksiyada farqli qiladi.

Bir so'z bilan aytganda, this kalit so'zi arrow funksiyalari bilan qo'llanganda bog'lanish (binding) ga ega bo'lmaydi.

Odatiy funktsiyalarda this kalit so'zi function deb ataladigan obyektni ifodalaydi, bu window, hujjat, tugma yoki boshqa narsa bo'lishi mumkin.

Arrow funksiyalarida esa `this` kalit so'zi har doim arrow funksiya eʼlon qilingan obyektni ifodalaydi.

Buning farqini tushunish uchun quyidagi ikki misolni ko'rib chiqaylik.

Ikkala misol ham metodni ikki marta chaqiradi, birinchisi sahifa yuklanganida va foydalanuvchi tugmani yana bir marta bosganida.

Birinchi misolda oddiy funksiyadan, ikkinchi misolda esa arrow funksiyadan foydalanilgan.

Natija, birinchi misol ikki xil obektni (window va tugma) qaytarganini va ikkinchi misol esa window obyektini ikki marta qaytarganini koʻrsatadi, chunki window obyekti funksiyaning "egasi" hisoblqnadi.

{% code title="Odatdagi funksiyalarda  this kalit so'zi funksiyaga murojaat qilayotgan obyektni bildiradi:" %}
```
// Regular Function:
hello = function() {
  document.getElementById("demo").innerHTML += this;
}

// The window object calls the function:
window.addEventListener("load", hello);

// A button object calls the function:
document.getElementById("btn").addEventListener("click", hello);
```
{% endcode %}

{% code title="Arrow funksiyalarda esa this kalit so'zi ishlatilganda this shu arrow funksiyaning "egasi"ga murojaat qiladi." %}
```
// Arrow Function:
hello = () => {
  document.getElementById("demo").innerHTML += this;
}

// The window object calls the function:
window.addEventListener("load", hello);

// A button object calls the function:
document.getElementById("btn").addEventListener("click", hello);
```
{% endcode %}

Funksiyalar bilan ishlayotganingizda bu farqlarni yodda tuting. Ba'zan odatiy funktsiyalarning xatti-harakati siz xohlagan natijani berishi mumkun, agar unday boʻlmasa, arrow funksiyalaridan foydalaning.

### Brauzerning qo'llab-quvvatlashi

Quyidagi jadvalda brauzerlar qaysi versiyadan boshlab arrow funksiyalarni to'liq qo'llab-quvvatlashi ko'rsatilgan:

| Chrome    | Edge      | Firefox    | Safari    |           |
| --------- | --------- | ---------- | --------- | --------- |
| Chrome 45 | Edge 12   | Firefox 22 | Safari 10 | Opera 32  |
| Sep, 2015 | Jul, 2015 | May, 2013  | Sep, 2016 | Sep, 2015 |
