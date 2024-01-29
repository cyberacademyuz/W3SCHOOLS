# ES6 Arrow funksiya

### Arrow funksiyalar

Arrow funksiyalari funksiya sintaksisini qisqaroq yozishga imkon beradi:

{% code title="Expression funksiya" %}
```jsx
hello = function() {
  return "Hello World!";
}
```
{% endcode %}

{% code title="Arrow funksiya" %}
```jsx
hello = () => {
  return "Hello World!";
}
```
{% endcode %}

Yanada qisqaroq bo'la oladi! Agar funktsiyada faqat bitta steytment bo'lsa va steytment qiymat qaytarsa, qavslar _va_ `return` kalit so'zidan foydalanmasligingiz mumkin:

Arrow funktsiyalar default tarzda qiymatni qaytaradi:

```jsx
hello = () => "Hello World!";
```

{% hint style="warning" %}
**Eslatma:** Bu funksiya faqat bitta steytmentga ega bo'lsagina ishlaydi.
{% endhint %}

Agar sizda parametrlar bo'lsa, ularni qavs ichida yozing:

{% code title="Parametrli arrow funksiya:" %}
```jsx
hello = (val) => "Hello " + val;
```
{% endcode %}

Aslida, agar faqat bitta parametr bo'lsa, qavslardan foydalanmasangiz ham bo'ladi:

{% code title="Qavssiz arrow funksiya:" %}
```jsx
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

Natija, birinchi misol ikki xil obektni (window va tugma) qaytarganini va ikkinchi misol esa window obyektini ikki marta qaytarganini koʻrsatadi.

{% code title="Odatdagi funksiyalarda  this kalit so'zi funksiyaga murojaat qilayotgan obyektni bildiradi:" %}
```jsx
class Header {
  constructor() {
    this.color = "Red";
  }

//Regular function:
  changeColor = function() {
    document.getElementById("demo").innerHTML += this;
  }
}

const myheader = new Header();

//The window object calls the function:
window.addEventListener("load", myheader.changeColor);

//A button object calls the function:
document.getElementById("btn").addEventListener("click", myheader.changeColor);
 
```
{% endcode %}

{% code title="Arrow funksiyalarda, esa this funksiyasini kim chaqirganidan qat'i nazar, Header obyektini ifodalaydi:" %}
```jsx
class Header {
  constructor() {
    this.color = "Red";
  }

//Arrow function:
  changeColor = () => {
    document.getElementById("demo").innerHTML += this;
  }
}

const myheader = new Header();


//The window object calls the function:
window.addEventListener("load", myheader.changeColor);

//A button object calls the function:
document.getElementById("btn").addEventListener("click", myheader.changeColor);
 
```
{% endcode %}

Funksiyalar bilan ishlayotganingizda bu farqlarni eslang. Ba'zan oddiy funksiyalar ham siz xohlagan ishni qila oladi, agar qila olmasa, arrow funktsiyalardan foydalaning.
