# JS Popup Alert

JavaScript-da uch xil popup oynalar mavjud: Ogohlantirish oynasi, Tasdiqlash oynasi va So'rov oynasi.

### Ogohlantirish oynasi

Agar ma'lumot foydalanuvchiga yetib borishiga ishonch hosil qilishni istasangiz, ogohlantirish oynasi tez-tez ishlatiladi.

Ogohlantirish oynasi ochilganda, foydalanuvchi davom etish uchun "OK" tugmasini bosishi kerak.

{% code title="Sintaksis" %}
```
window.alert("sometext");
```
{% endcode %}

`window.alert()` metodi window qo'shimchasisiz ham yozilishi mumkin.

```
alert("I am an alert box!");
```

### Tasdiqlash oynasi

Agar foydalanuvchi biror narsani tasdiqlashi yoki qabul qilishi kerak bo'lsa, ko'pincha tasdiqlash oynasi ishlatiladi.

Tasdiqlash oynasi ochilganda, foydalanuvchi davom etish uchun "OK" yoki "Bekor qilish" tugmasini bosishi kerak.

Agar foydalanuvchi "OK" tugmasini bosgan bo'lsa, oyna  **"true"** qaytaradi. Agar foydalanuvchi "Bekor qilish" tugmasini bosgan bo'lsa, oyna **"false"** ni qaytaradi.

{% code title="Sintaksis:" %}
```
window.confirm("sometext");
```
{% endcode %}

`window.confirm()` metodi window qo'shimchasisiz ham yozilishi mumkin.

```
if (confirm("Press a button!")) {
  txt = "You pressed OK!";
} else {
  txt = "You pressed Cancel!";
}
```

### So'rov oynasi

Agar foydalanuvchi sahifaga kirishdan oldin qiymat kiritishini xohlasangiz, ko'pincha so'rov oynasi ishlatiladi.

So'rov oynasi ochilganda, foydalanuvchi ma'lumot kiritgandan so'ng davom etish uchun "OK" yoki "Bekor qilish" tugmasini bosishi kerak bo'ladi.

Agar foydalanuvchi "OK" tugmasini bosgan bo'lsa, maydon kiritilgan ma'lumotni qaytaradi. Agar foydalanuvchi "Bekor qilish" tugmasini bosgan bo'lsa, maydon `null` qaytaradi.

{% code title="Sintaksis:" %}
```
window.prompt("sometext","defaultText");
```
{% endcode %}

`window.prompt()` metodi window qo'shinchasisiz ham yozilishi mumkin.

```
let person = prompt("Please enter your name", "Harry Potter");
let text;
if (person == null || person == "") {
  text = "User cancelled the prompt.";
} else {
  text = "Hello " + person + "! How are you today?";
}
```

### Qatorni bo'lish

Popup oynalarida qatorni bo'lib ko'rsatish uchun teskari chiziqdan keyin `n` belgisidan foydalaning.

```
alert("Hello\nHow are you?");
```
