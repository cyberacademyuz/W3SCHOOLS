# jQuery Traversing

Traversing o'zi nima?

"O'tish" degan ma'noni anglatuvchi jQuery traversing HTML elementlarini boshqa elementlarga munosabatiga qarab "topish" uchun ishlatiladi. Bu holat bitta elementni tanlashdan boshlanadi va toki siz xohlagan elementni topguncha davom etadi.

Quyidagi rasmda HTML sahifa shajara (DOM shajarasi) ko'rinishida tasvirlangan. jQuery traversing yordamida tanlangan (joriy) elementdan boshlab shajrada osongina yuqoriga (ancestors), pastga (descendants) va yon tomonga (siblinglar) harakat qilishingiz mumkin. Ushbu harakat "**DOM traversing**"  yoki "**move through**" ataladi.

<figure><img src="../../.gitbook/assets/img_travtree.png" alt=""><figcaption></figcaption></figure>

Illustratsiyani tushuntirish:

* `<div>` parent element hisoblanadi va u barcha bola elementlar uchun ancestor hisoblanadi.
* `<ul>` elementi esa ikkita `<li>` elementlarining parent elementi bo'lib, `<div>` elementining child elementi hisoblanadi.
* Chap tomondagi `<li>` ikkita `<span>` elementlarining parenti elementi bo'lib, `<ul>` elementining child elementi va `<div>` elementining descendanti hisoblanadi.
* `<span>` chap tomondagi `<li>` ning child elementi va `<ul>` hamda `<div>` elementlarining descendanti hisoblanadi.
* ikkala `<li>` elementlar **siblinglar** hisoblanadi (ularni otasi bitta).
* O'ng tomondagi `<li>` `<b>` elementining parent elementi bo'lib, `<ul>` elementining child elementi va `<div>` elementining descendanti hisoblanadi
* `<b>` o'ng tomondagi `<li>` ning child elementi va `<ul>` hamda `<div>` elementlarining descendanti hisoblanadi.

{% hint style="warning" %}
Ancestor - bu ota, bobo, katta bobo va boshqalar. \
Descendant - bu bola, nevara, chevara va boshqalar. \
Siblinglar -  bitta ota-onaga ega elementlarga aytiladi
{% endhint %}

### DOM Traversing <a href="#dom-traversing" id="dom-traversing"></a>

jQuery DOMda harakatlanishimiz uchun bir qancha turli metodlar taqdim qiladi.

Ushbu metodlarning eng kattasi bu tree-traversal hisoblanadi.

Keyingi bo'limlarda DOM shajarasida qanday qilib yuqoriga, pastga va yon tomonga harakatlanishni ko'rib chiqamiz.
