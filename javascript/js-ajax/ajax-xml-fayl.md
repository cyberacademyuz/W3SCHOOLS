# AJAX XML Fayl

AJAX, XML fayli bilan interaktiv aloqa uchun ishlatilishi mumkin.

### AJAX XML ga misol

Quyidagi misol veb-sahifa qanday qilib AJAX yordamida XML faylidan ma'lumot olishi mumkinligini ko'rsatadi:

<figure><img src="../../.gitbook/assets/image (35).png" alt=""><figcaption></figcaption></figure>

### Misolni tushuntirish

Foydalanuvchi yuqoridagi "CD haqida ma'lumot olish" tugmasini bosganida, `loadDoc()` funksiyasi bajariladi.

`loadDoc()` funktsisiya `XMLHttpRequest` obyektni yaratadi, server response-i tayyor bo'lganda bajariladigan funksiyani qo'shadi va so'rovni serverga yuboradi.

Server javobi tayyor bo'lgach, HTML jadvali quriladi, XML faylidan nodelar (elementlar) olinadi va nihoyat "demo" elementining XML ma'lumotlaridan tashkil topgan HTML jadvali yangilaydi:

```
function loadDoc() {
  const xhttp = new XMLHttpRequest();
  xhttp.onload = function() {myFunction(this);}
  xhttp.open("GET", "cd_catalog.xml");
  xhttp.send();
}
function myFunction(xml) {
  const xmlDoc = xml.responseXML;
  const x = xmlDoc.getElementsByTagName("CD");
  let table="<tr><th>Artist</th><th>Title</th></tr>";
  for (let i = 0; i <x.length; i++) {
    table += "<tr><td>" +
    x[i].getElementsByTagName("ARTIST")[0].childNodes[0].nodeValue +
    "</td><td>" +
    x[i].getElementsByTagName("TITLE")[0].childNodes[0].nodeValue +
    "</td></tr>";
  }
  document.getElementById("demo").innerHTML = table;
}
```

### XML fayli

Yuqoridagi misolda foydalanilgan XML fayli quyidagicha ko'rinadi: "[cd\_catalog.xml](https://www.w3schools.com/js/cd\_catalog.xml)".
