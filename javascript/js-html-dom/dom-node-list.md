# DOM Node list

### HTML DOM NodeList Obyekti

`NodeList` obyekti - bu hujjatdan olingan nodelar ro'yxati.

`NodeList` obyekti `HTMLCollection` obyekti bilan deyarli bir xil.

Ba'zi (eski) brauzerlar `getElementsByClassName()` kabi metodlar uchun HTMLCollection o'rniga NodeList obyektini qaytaradi.

Barcha brauzerlar `childNodes` xususiyati uchun NodeList obyektini qaytaradi.&#x20;

Ko'pgina brauzerlar `querySelectorAll()` metodi uchun NodeList obyektini qaytaradi.

Quyidagi kod hujjatdagi barcha `<p>` nodelarini tanlaydi:

```
const myNodeList = document.querySelectorAll("p");
```

NodeList-dagi elementlarga indeks raqami orqali murojaat qilish mumkin.

Ikkinchi \<p> node-iga murojaat qilish uchun quyidagilarni yozishingiz mumkin:

```
myNodeList[1]
```

Eslatma: indeks 0 dan boshlanadi.

### HTML DOM Node roʻyxatining uzunligi

`length` xususiyati nodelar ro'yxatidagi nodelar sonini ifodalaydi:

```
myNodelist.length
```

`length` xususiyati nodelar ro'yxatidagi nodelar bo'ylab harakatlanmoqchi bo'lganingizda foydali:

{% code title="Tugunlar roʻyxatidagi barcha <p> elementlarning rangini oʻzgartiring:" %}
```
const myNodelist = document.querySelectorAll("p");
for (let i = 0; i < myNodelist.length; i++) {
  myNodelist[i].style.color = "red";
}
```
{% endcode %}

### HTMLCollection va NodeList o'rtasidagi farq

NodeList va HTMLcollection bir xil narsa.

Ikkalasi ham hujjatdan olingan nodelarning (ya'ni elementlarning) massivga o'xshash ro'yxatidir. Nodelarga indeks raqamlari orqali murojaat qilish mumkin. Indeks 0 dan boshlanadi.

Har ikkisi ham roʻyxatdagi elementlar sonini qaytaruvchi `length` xususiyatiga ega.

`HTMLCollection` - bu hujjat elementlarining ro'yhati.

NodeList - bu hujjat nodelarining ro'yhati (element nodelari, atribut nodelari va matn nodelari).

HTMLCollection elementlariga ularning nomi, identifikatori yoki indeks raqami orqali murojaat qilishi mumkin.

NodeList elementlariga esa faqat ularning indeks raqami orqali murojaat qilish mumkin.

HTMLCollection har doim jonli ro'yhatdir. Misol: Agar siz DOM ro'yxatiga \<li> elementini qo'shsangiz, HTMLCollectiondagi ro'yxat ham o'zgaradi.

NodeList ko'pincha statik ro'yhat bo'ladi. Misol: Agar siz DOM ro'yxatiga \<li> elementini qo'shsangiz, NodeList ro'yxati o'zgarmaydi.

`getElementsByTagName()` va `getElementsByClassName()` metodlari jonli HTML to'plamini qaytaradi.

`querySelectorAll()` metodi statik NodeList qaytaradi.

`childNodes` xususiyati jonli NodeList qaytaradi.

{% hint style="warning" %}
### Massiv emas!

NodeList massiv kabi ko'rinishi mumkin, lekin massiv emas.

Siz NodeList orqali tskil qilishingiz va uning nodelariga indeks bo'yicha murojaat qilishingiz mumkin.

Biroq, NodeList-da `push()`, `pop()` yoki `join()` kabi massiv metodlaridan foydalana olmaysiz.
{% endhint %}
