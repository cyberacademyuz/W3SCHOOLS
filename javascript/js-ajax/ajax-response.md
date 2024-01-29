# AJAX Response

### Server javob xususiyatlari

| Xususiyat    | Ta'rif                                        |
| ------------ | --------------------------------------------- |
| responseText | Response ma'lumotlarini string sifatida oling |
| responseXML  | Response ma'lumotlarini XML sifatida oling    |

### responseText xususiyati

`responseText` xususiyati serverning javobini string sifatida qaytaradi va undan mos ravishda foydalanishingiz mumkin:

```
document.getElementById("demo").innerHTML = xhttp.responseText;
```

### responseXML xususiyati

XMLHttpRequest obyekti built-in XML parseriga ega.

`responseXML` xususiyati serverning response-ini XML DOM obyekti sifatida qaytaradi.

Ushbu xususiyatdan foydalanib, response-ni XML DOM obyekti sifatida parse qilishingiz mumkin:

{% code title="cd_catalog.xml faylini so'rang va javobni parse qiling:" %}
```
const xmlDoc = xhttp.responseXML;
const x = xmlDoc.getElementsByTagName("ARTIST");

let txt = "";
for (let i = 0; i < x.length; i++) {
  txt += x[i].childNodes[0].nodeValue + "<br>";
}
document.getElementById("demo").innerHTML = txt;

xhttp.open("GET", "cd_catalog.xml");
xhttp.send();
```
{% endcode %}

### Server Response metodlari

| Metod                   | Ta'rif                                                   |
| ----------------------- | -------------------------------------------------------- |
| getResponseHeader()     | Server resursidan maxsus header ma'lumotlarini qaytaradi |
| getAllResponseHeaders() | Server resursidan barcha header ma'lumotlarini qaytaradi |

### getAllResponseHeaders() metodi

`getAllResponseHeaders()` metodi server response-idan barcha header ma'lumotlarini qaytaradi.

```
const xhttp = new XMLHttpRequest();
xhttp.onload = function() {
    document.getElementById("demo").innerHTML =
    this.getAllResponseHeaders();
}
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
```

### getResponseHeader() metodi&#x20;

`getResponseHeader()` metodi server response-idan ma'lum bir header ma'lumotlarini qaytaradi.

```
const xhttp = new XMLHttpRequest();
xhttp.onload = function() {
    document.getElementById("demo").innerHTML =
    this.getResponseHeader("Last-Modified");
}
xhttp.open("GET", "ajax_info.txt");
xhttp.send();
```
