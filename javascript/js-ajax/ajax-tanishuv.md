# AJAX Tanishuv

{% hint style="success" %}
AJAX - bu dasturchining orzusi, chunki siz:

* Sahifa yuklangandan keyin - web-serverdan ma'lumotlarni o'qishingiz mumkin
* Sahifani qayta yuklamasdan veb-sahifani yangilash mumkin
* Ma'lumotlarni web-serverga orqafonda yuborish mumkin
{% endhint %}

<figure><img src="../../.gitbook/assets/image (20).png" alt=""><figcaption></figcaption></figure>

### AJAX misolini tushuntirish

{% code title="HTML sahifa" %}
```
<!DOCTYPE html>
<html>
<body>

<div id="demo">
  <h2>Let AJAX change this text</h2>
  <button type="button" onclick="loadDoc()">Change Content</button>
</div>

</body>
</html>
```
{% endcode %}

HTML sahifada \<div> bo'limi va \<button> mavjud.

\<div> bo'limi serverdan ma'lumotlarni ko'rsatish uchun ishlatiladi.

\<button> (agar bosilsa) `loadDoc()` funksiyasini chaqiradi.

Funksiya veb-serverdan ma'lumotlarni so'raydi va ularni ko'rsatadi:

{% code title="loadDoc() funksiyasi" %}
```
function loadDoc() {
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {
    document.getElementById("demo").innerHTML = this.responseText;
    }
  xhttp.open("GET", "ajax_info.txt", true);
  xhttp.send();
}
```
{% endcode %}

### AJAX nima ?

AJAX = **A**synchronous **J**avaScript **A**nd **X**ML.

AJAX dasturlash tili emas.

AJAX faqat quyidagi kombinatsiyalardan foydalanadi:

* Brauzerning built-in `XMLHttpRequest` obyektidan (veb-serverdan ma'lumotlarni so'rash uchun)
* JavaScript va HTML DOMdan (ma'lumotlarni ko'rsatish yoki foydalanish uchun)

{% hint style="warning" %}
AJAX - nomi aldaydi. AJAX ilovalari ma'lumotlarni uzatish uchun XML dan foydalanishi mumkin, ammo ma'lumotlarni oddiy matn yoki JSON sifatida o'tkazish bir xil darajada keng tarqalgan.
{% endhint %}

AJAX veb-sahifalarni orqafondagi veb-server bilan ma'lumotlarni almashish orqali asinxron ravishda yangilanishiga imkon beradi. Bu butun sahifani qayta yuklamasdan, sahifa qismlarini yangilash mumkinligini anglatadi.

### AJAX qanday ishlaydi

![AJAX](https://www.w3schools.com/js/pic\_ajax.gif)

* 1\. Veb-sahifada hodisa yuz beradi (sahifa yuklanishi, tugma bosilishi)
* 2\. XMLHttpRequest obyekti JavaScript tomonidan yaratiladi
* 3\. XMLHttpRequest obyekti veb-serverga request yuboradi
* 4\. Server requestni qayta ishlaydi
* 5\. Server responseni veb-sahifaga yuboradi
* 6\. Response JavaScript tomonidan o'qiladi
* 7\. Sahifani yangilashi kabi harkat JavaScript tomonidan amalga oshiriladi

### Zamonaviy brauzerlar (Fetch API)

Zamonaviy brauzerlar XMLHttpRequest obyekti o'rniga Fetch API dan foydalanishi mumkin.

Fetch API interfeysi veb-brauzerga veb-serverlarga HTTP requestlarini yuborish imkonini beradi.

Agar siz `XMLHttpRequest` obyektidan foydalansangiz, Fetch xuddi shu ishni soddaroq tarzda amalga oshirishi mumkin.
