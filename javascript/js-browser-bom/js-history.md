# JS History

`window.history` obyekti brauzer tarixini o'z ichiga oladi.

### window history

`window.history` obyekti `window` qo'shimchasisiz ham yozilishi mumkin.

Foydalanuvchilarning maxfiyligini himoya qilish uchun JavaScript-ning ushbu obyektga murojaat qilishiga ba'zi cheklovlar mavjud.

Uning ba'zi metodlari:

* `history.back()`- brauzerda orqaga qaytish bilan bir xil
* `history.forward()`- brauzerda oldinga o'tish bilan bir xil

### Window History back

`history.back()` metodi tarix ro'yxatidagi oldingi URL manzilini ochadi.

Bu brauzerdagi Orqaga tugmasini bosish bilan bir xil.

{% code title="Sahifada orqaga tugma yarating:" %}
```
<html>
<head>
<script>
function goBack() {
  window.history.back()
}
</script>
</head>
<body>

<input type="button" value="Back" onclick="goBack()">

</body>
</html>
```
{% endcode %}

Yuqoridagi kod natijasi quyidagicha bo'ladi:

### Window History Forward

`history.forward()` metodi tarix ro'yxatidagi keyingi URL manzilini ochadi.

Bu brauzerda "forward" tugmasini bosish bilan bir xil.

{% code title="Sahifada oldinga siljish tugmasi yarating:" %}
```
<html>
<head>
<script>
function goForward() {
  window.history.forward()
}
</script>
</head>
<body>

<input type="button" value="Forward" onclick="goForward()">

</body>
</html>
```
{% endcode %}

Yuqoridagi kod natijasi quyidagicha bo'ladi:
