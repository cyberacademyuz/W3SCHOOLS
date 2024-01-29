# WEB History API

{% hint style="success" %}
**Web History API** `windows.history` obyektiga murojaat qilishning oson yo'lini taqdim qiladi.

window.history obyektida foydalanuvchi tashrif buyurgan URL manzillar mavjud.
{% endhint %}

Web History API barcha brauzerlarda qo'llab-quvvatlanadi:

| Chrome | Edge | Firefox | Safari | Opera |
| ------ | ---- | ------- | ------ | ----- |
| Ha     | Ha   | Ha      | Ha     | Ha    |

### History back() metodi

back() metodi bitta avvalgi URL manzilni `windows.history` roʻyxatiga yuklaydi.

Bu brauzeringizdagi "orqaga qaytish" tugmasini bosish bilan bir xil.

```
<button onclick="myFunction()">Go Back</button>

<script>
function myFunction() {
  window.history.back();
}
</script>
```

### History go() metodi

go() metodi berilgan qiymat asosida tarix roʻyxatidagi URL manzilni yuklaydi:

```
<button onclick="myFunction()">Go Back 2 Pages</button>

<script>
function myFunction() {
  window.history.go(-2);
}
</script>
```

### History obyektining xususiyatlari

| Xususiyat                                                                                                                                     | Ta'rif                                            |
| --------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------- |
| [length](https://www-w3schools-com.translate.goog/jsref/prop\_his\_length.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Tarix roʻyxatidagi URL manzillar sonini qaytaradi |

### History obyektining metodlari

| Metod                                                                                                                                            | Ta'rif                                                                         |
| ------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------ |
| [back()](https://www-w3schools-com.translate.goog/jsref/met\_his\_back.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)       | Tarix ro'yxatida joriy sahifan bitta oldingi sahifaning URL manzilini yuklaydi |
| [forward()](https://www-w3schools-com.translate.goog/jsref/met\_his\_forward.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp) | Tarix ro'yxatida mavjud bo'lsa joriy sahifadan keyingi URLni yuklaydi          |
| [go()](https://www-w3schools-com.translate.goog/jsref/met\_his\_go.asp?\_x\_tr\_sl=ru&\_x\_tr\_tl=uz&\_x\_tr\_hl=en&\_x\_tr\_pto=wapp)           | Berilgan qiymat asosida tarix ro'yxatidagi URLni yuklaydi                      |
