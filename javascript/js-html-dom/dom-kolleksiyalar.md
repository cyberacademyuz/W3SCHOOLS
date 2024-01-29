# DOM Kolleksiyalar

### HTML to'plami obyekti

`getElementsByTagName()` metodi `HTMLCollection` obyektini qaytaradi.

`HTMLCollection` obyekti - HTML elementlarining massivga o'xshash ro'yxati (to'plami) hisoblanadi.

Quyidagi kod hujjatdagi barcha `<p>` elementlarini tanlaydi:

```
const myCollection = document.getElementsByTagName("p");
```

Ro'yhatdagi elementlarga indeks raqami orqali murojaat qilish mumkin.

Ikkinchi indeksdagi `<p>` ​​elementiga murojaat qilish uchun quyidagilarni yozishingiz mumkin:

```
myCollection[1]
```

Eslatma: indeks 0 dan boshlanadi.

### HTML HTMLCollection uzunligi

`length` xususiyati `HTMLCollection` elementidagi elementlar sonini belgilaydi:

```
myCollection.length
```

`length` xususiyati ro'yhatdagi elementlarni tskil qilmoqchi bo'lganingizda foydali hisoblanadi:

```
Barcha <p> elementlarning matn rangini o'zgartiring:
```

```
const myCollection = document.getElementsByTagName("p");
for (let i = 0; i < myCollection.length; i++) {
  myCollection[i].style.color = "red";
}
```

{% hint style="warning" %}
**HTMLCollection massiv EMAS!**

`HTMLCollection` massiv kabi ko'rinishi mumkin, lekin massiv emas.

Siz ro'yxat bo'ylab harkatlnishingiz va raqamlar bilan elementlarga murojaat qilishingiz mumkin (xuddi massiv kabi).

Biroq, HTMLCollection da `valueOf()`, `pop()`, `push()` yoki `join()` kabi massiv metodlaridan foydalana olmaysiz.
{% endhint %}
